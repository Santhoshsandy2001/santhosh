
from file import File
from random import choice


class Main:

    def __init__(self):

        # The file_handler object will be used to read and write to files.
        self.file_handler = File()

        login_menu_is_running = True

        while login_menu_is_running:

            print('1 - Sign up')
            print('2 - Login')

            menu_choice = input('\nEnter menu option: ')

            login_menu_is_running = False

            if menu_choice == '1':
                self.signup()
            elif menu_choice == '2':
                self.login()
            else:
                print('Please choose a number from the menu.')
                login_menu_is_running = True

        menu_is_running = True

        while menu_is_running:

            print('\n1 - Add a new student to the system.')
            print('2 - Display a student\'s details.')
            print('3 - Edit a students details.')
            print('4 - Log out.')

            menu_choice = input('\nEnter menu option: ')

            if menu_choice == '1':
                self.add_student()

            elif menu_choice == '2':
                self.print_student_details()

            elif menu_choice == '3':
