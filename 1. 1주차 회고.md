#### 1. 1주차 회고

이전에 프로젝트를 하면서 자바스크립트, 타입스크립트를 사용했지만, 당시에 이론이나 개념적인 부분을 공부하지 않고, 프로젝트 완성을 위한 무대뽀 코드 작성을 하다보니 많이 부족함을 느낄 수 있었다.

특히 제네릭...  타입스크립트를 사용할 때, interface나 type만 생각하고 있었는데 제네릭이 있었다는 것과 내가 아직 이 개념을 제대로 모르고 있었다는 걸 알았다.

더불어 유틸리티 타입(Partial, Pick, Omit...), 클로저(closure) 등등 새로 알게된 개념이 많았다.

자바스크립트 코드를 손가락으로 쳐본지 1년이 되가는 시점에서 백지상태에 처음부터 공부해야겠다는 생각을 했다. :( 

그 와중에 31일 이전에 정리한 수업 내용도 다 날아가 버렸다.

그래도 이전에 async나 promise등을 사용하면서 왜 사용해야 하는지, 왜 이렇게 되는거지? 라는 의문을 가지고 무작정 코드만 작성했다면, 그래도 어느정도의 이유를 알아갈 수 있었다.





자바스크립트 과제와 React를 이용한 기본 구현 과제를 하면서, 기초적인 부분은 쉽게 할 수 있었지만, 뭔가 응용을 하거나 CSS를 사용하는 것에 애를 많이 먹었다.



특히, 이전에 내가 사용하던 코드 방식을 잊고 수업에서 진행하는 방식을 몸에 익히는데 시간이 좀 걸릴 듯 싶다.



과제를 하면서 작성한 코드 중 일부다.

```typescript
import { MouseEventHandler, useState } from "react";

const Login = () => {
  const [email, setEmail] = useState("");
  const [password, setPassword] = useState("");

  const checkValue: MouseEventHandler<HTMLButtonElement> | undefined = () => {
    if (email.length == 0 || password.length == 0) {
      alert("빈칸을 채워주세요");
    }
  };

  return (
    <div
      style={{
        width: "375px",
        height: "434px",
        backgroundColor: "white",
        borderRadius: "8px",
        margin: "auto",
        paddingTop: "40px",
      }}
    >
      <div style={{ marginInline: "25px" }}>
        <h2 style={{ fontWeight: "bold", fontSize: "20px" }}>Login Into App</h2>
        <p style={{ marginBlock: "10px" }}>
          Please enter your details to continue.
        </p>
      </div>

      <form style={{ marginInline: "25px" }}>
        <input
          type="email"
          placeholder="someone@example.com"
          value={email}
          onChange={(e) => setEmail(e.target.value)}
          required
          style={{
            width: "325px",
            height: "44px",
            border: "1px solid #4F4F4F",
            borderRadius: "8px",
            marginBlock: "8px",
            padding: "16px",
          }}
        />
        <input
          type="password"
          placeholder="Enter Password"
          value={password}
          onChange={(e) => setPassword(e.target.value)}
          required
          style={{
            width: "325px",
            height: "44px",
            border: "1px solid #4F4F4F",
            borderRadius: "8px",
            marginBlock: "8px",
            padding: "16px",
          }}
        />
        <div style={{ display: "flex", alignItems: "center" }}>
          <input
            type="checkbox"
            required
            style={{ width: "20px", height: "20px", marginRight: "8px" }}
          />
          <label>
            I agree with <span style={{ fontWeight: "bold" }}>terms</span> and
            <span style={{ fontWeight: "bold" }}> policies</span>.
          </label>
        </div>
      </form>
      <div style={{ marginInline: "25px", marginBlock: "16px" }}>
        <button
          type="submit"
          style={{
            width: "325px",
            height: "44px",
            marginBlock: "8px",
            backgroundColor: "#4F4F4F",
            borderRadius: "8px",
            color: "white",
            fontSize: "14px",
          }}
          onClick={checkValue}
        >
          Log In
        </button>
        <button
          style={{
            width: "325px",
            height: "44px",
            marginBlock: "8px",
            borderRadius: "8px",
            border: "1px solid #4F4F4F",
            fontSize: "14px",
          }}
        >
          Go To Sign Up
        </button>
      </div>
    </div>
  );
};

export default Login;

```

역시 스타일을 tag에 직접 넣으니 가독성이 좋지 않다.

React를 사용하면서 정말 기초적으로 완성해야 하는 페이지.....

또, 페이지를 만들때 이런식으로 스타일을 적용하면 이후에 수정할 때나, 반응형으로 만들 때 좋지 않기 때문에 공부가 더 필요해 보인다.






























