#include <SFML/Graphics.hpp>  //Add it (download from SFML website)

//click left on mouse to dance

using namespace std;

int main()
{
    int width = 600,height = 800 , r = 50;
    sf::RenderWindow window(sf::VideoMode(width,height),"ULTRA",sf::Style::Titlebar   | sf::Style::Close);

    sf::CircleShape shape;
    sf::CircleShape shape1;
    sf::CircleShape shape2;
    sf::CircleShape shape3;
    sf::CircleShape shape4;

    shape.setRadius(r);
    shape1.setRadius(r);
    shape2.setRadius(r);
    shape3.setRadius(r);
    shape4.setRadius(r);

    shape.setFillColor(sf::Color::Red);
    shape1.setFillColor(sf::Color::Yellow);
    shape2.setFillColor(sf::Color::Green);
    shape3.setFillColor(sf::Color::Blue);
    shape4.setFillColor(sf::Color::Cyan);

    shape4.rotate(270);
    shape3.rotate(180);
    shape2.rotate(90);
    window.setMouseCursorVisible(false);
    int a,b,c=3;
    while(window.isOpen())
    {

        shape.setPosition(a,b);
        shape1.setPosition(a-100,b);
        shape2.setPosition(a+100,b-100);
        shape3.setPosition(a+200,b+100);
        shape4.setPosition(a,b+200);
        
        sf::Event event;
        while(window.pollEvent(event))
        {
            switch(event.type)
            {
            case sf::Event::Closed:
                window.close();
                break;
            case sf::Event::MouseMoved:
                a=sf::Mouse::getPosition(window).x - 50; b = sf::Mouse::getPosition(window).y -50;
                break;
            }
        }

        if(sf::Mouse::isButtonPressed(sf::Mouse::Left))
        {
            shape1.rotate(1);
            shape2.rotate(1);
            shape3.rotate(1);
            shape4.rotate(-1);
        }
        window.clear();
        window.draw(shape);
        window.draw(shape1);
        window.draw(shape2);
        window.draw(shape3);
        window.draw(shape4);
        window.display();
    }
}
