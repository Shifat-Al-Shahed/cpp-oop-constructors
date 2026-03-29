#include <bits/stdc++.h>
using namespace std;
class phone
{
    string name, cpu;
    int ram, battery;

public:
    phone(string name = "NULL", int ram = 0, string cpu = "NULL", int battery = 0)
    {
        this->name = name;
        this->ram = ram;
        this->cpu = cpu;
        this->battery = battery;
    }
    phone(const phone &obj)
    {
        name = obj.name;
        ram = obj.ram;
        cpu = obj.cpu;
        battery = obj.battery;
    }
    void print_details();
};

void phone ::print_details()
{
    cout << "NAME : " << name << '\n' << "RAM : " << ram << " GB" << '\n';
    cout << "PROCESSOR : " << cpu << '\n' << "BATTERY : " << battery << " mAh" << '\n';
    cout << '\n';
}

signed main()
{
    phone mob1, mob2("Nokia", 8, "snapdragon", 5000);
    phone mob3(mob2);
    mob1.print_details(), mob2.print_details(), mob3.print_details();
    return 0;
}
