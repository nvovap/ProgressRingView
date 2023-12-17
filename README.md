# ProgressRingView



ProgressRingView is a SwiftUI.






## Examples

Here's some example code. 

```swift
import SwiftUI

struct ContentView: View {

    @State var progress = 0.0
    
    
    var body: some View {
        VStack {
            ZStack {
                ProgressRingView(progress: $progress, thickness: 30,
                                 width: 300,
                                 gradient: Gradient(colors: [.darkPurple, .lightPurple]))
                
                ProgressRingView(progress: $progress, thickness: 30,
                                 width: 235,
                                 gradient: Gradient(colors: [.darkYellow, .lightYellow]))
                
                ProgressRingView(progress: $progress,thickness: 30,
                                 width: 170,
                                 gradient: Gradient(colors: [.darkGreen, .lightGreen]))
            }
 

            HStack {
                Group {
                    Text("25%")
                        .font(.system(.headline, design: .rounded))
                        .onTapGesture {
                            progress = 0.25
                        }
                    
                    Text("50%")
                        .font(.system(.headline, design: .rounded))
                        .onTapGesture {
                            progress = 0.5
                        }
                    
                    Text("75%")
                        .font(.system(.headline, design: .rounded))
                        .onTapGesture {
                            progress = 0.75
                        }
                    
                    Text("100%")
                        .font(.system(.headline, design: .rounded))
                        .onTapGesture {
                            progress = 1.0
                        }
                }.padding()
                    .background(Color(.systemGray6))
                    .clipShape(RoundedRectangle(cornerRadius:  15.0, style: .continuous)
                    )
            }.padding()
        }
        .padding()
    }
}

#Preview {
    ContentView()
}
```

Y
## License

MIT License.

Copyright (c) 2021 Paul Hudson

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
