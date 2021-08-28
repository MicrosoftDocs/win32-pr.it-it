---
Description: Inviato a una finestra dopo che le dimensioni sono state modificate.
ms.assetid: e3e14dcd-9236-48bd-a692-6985d8146f81
title: WM_SIZE messaggio (Winuser.h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 473e4e63523c7b97968e54349e5882b7e589fc7238d717ccf96563b5ce93388e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119548221"
---
# <a name="wm_size-message"></a>Messaggio \_ WM SIZE

Inviato a una finestra dopo che le dimensioni sono state modificate.

Una finestra riceve questo messaggio tramite la [**relativa funzione WindowProc.**](/windows/win32/api/winuser/nf-winuser-defwindowproca)


```C++
#define WM_SIZE                         0x0005
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Tipo di ridimensionamento richiesto. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                   | Significato                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="SIZE_MAXHIDE"></span><span id="size_maxhide"></span><dl> <dt>**DIMENSIONI \_ MAXHIDE**</dt> <dt>4</dt> </dl>       | Il messaggio viene inviato a tutte le finestre popup quando un'altra finestra è ingrandita.<br/>                              |
| <span id="SIZE_MAXIMIZED"></span><span id="size_maximized"></span><dl> <dt>**DIMENSIONI \_ INGRANDITA**</dt> <dt>2</dt> </dl> | La finestra è stata ingrandita.<br/>                                                                          |
| <span id="SIZE_MAXSHOW"></span><span id="size_maxshow"></span><dl> <dt>**DIMENSIONI \_ MAXSHOW**</dt> <dt>3</dt> </dl>       | Il messaggio viene inviato a tutte le finestre popup quando un'altra finestra è stata ripristinata alle dimensioni precedenti.<br/>      |
| <span id="SIZE_MINIMIZED"></span><span id="size_minimized"></span><dl> <dt>**DIMENSIONI \_ RIDOTTO A ICONA**</dt> <dt>1</dt> </dl> | La finestra è stata ridotta a icona.<br/>                                                                          |
| <span id="SIZE_RESTORED"></span><span id="size_restored"></span><dl> <dt>**DIMENSIONI \_ RESTORED**</dt> <dt>0</dt> </dl>    | La finestra è stata ridimensionata, ma non viene applicato né il valore **SIZE \_ MINIMIZED** né **SIZE \_ MAXIMIZED.**<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

La parola più bassa di *lParam* specifica la nuova larghezza dell'area client.

La parola più alta di *lParam* specifica la nuova altezza dell'area client.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Se un'applicazione elabora questo messaggio, deve restituire zero.

## <a name="example"></a>Esempio

```cpp
/******************************************************************
*                                                                 *
*  SimpleText::OnResize                                           *
*                                                                 *
*  If the application receives a WM_SIZE message, this method     *
*  resize the render target appropriately.                        *
*                                                                 *
******************************************************************/

void SimpleText::OnResize(UINT width, UINT height)
{
    if (pRT_)
    {
        D2D1_SIZE_U size;
        size.width = width;
        size.height = height;
        pRT_->Resize(size);
    }
}

LRESULT CALLBACK SimpleText::WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam)
{
   
    SimpleText *pSimpleText = reinterpret_cast<SimpleText *>(
                ::GetWindowLongPtr(hwnd, GWLP_USERDATA));

    if (pSimpleText)
    {
        switch(message)
        {
        case WM_SIZE:
            {
                UINT width = LOWORD(lParam);
                UINT height = HIWORD(lParam);
                pSimpleText->OnResize(width, height);
            }
            return 0;

// ...

```

Esempio di [Windows esempi classici](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/DirectWrite/HelloWorld/SimpleText.cpp) in GitHub.

## <a name="remarks"></a>Commenti

Se la [**funzione SetScrollPos**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx) o [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) viene chiamata per una finestra figlio in seguito al messaggio **WM \_ SIZE,** il parametro *bRedraw* o *bRepaint* deve essere diverso da zero per fare in modo che la finestra venga ridisegnata.

Anche se la larghezza e l'altezza di una finestra sono valori a 32 bit, il *parametro lParam* contiene solo i 16 bit più bassi di ognuno.

La [**funzione DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) invia i **messaggi WM \_ SIZE** e **WM \_ MOVE** quando elabora il [**messaggio WM \_ WINDOWPOSCHANGED.**](wm-windowposchanged.md)
I **messaggi WM \_ SIZE** e **WM \_ MOVE** non vengono inviati se un'applicazione gestisce il messaggio **WM \_ WINDOWPOSCHANGED** senza **chiamare DefWindowProc.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**Movewindow**](/windows/win32/api/winuser/nf-winuser-movewindow)
</dt> <dt>

[**WM \_ WINDOWPOSCHANGED**](wm-windowposchanged.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**SetScrollPos**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx)
</dt> </dl>

 

 
