# Yesno
api for yesno.wtf random answer generate
# main
```cpp
#include "Yesno.h"
#include <iostream>

int main() {
   Yesno api;

    auto answer = api.YesOrNo().then([](json::value result) {
        std::cout << "Search results: " << result.serialize() << std::endl;
    });
    answer.wait();
    
    return 0;
}
```

# Launch (your script)
```
g++ -std=c++11 -o main main.cpp -lcpprest -lssl -lcrypto -lpthread -lboost_system -lboost_chrono -lboost_thread
./main
```

