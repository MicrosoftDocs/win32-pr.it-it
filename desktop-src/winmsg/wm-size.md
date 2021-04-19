---
Description: Inviato a una finestra dopo la modifica delle dimensioni.
ms.assetid: e3e14dcd-9236-48bd-a692-6985d8146f81
title: Messaggio WM_SIZE (winuser. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 04afafd3faafc4ea8c400472254dcf4ec4afa050
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333633"
---
# <a name="wm_size-message"></a>\_Messaggio dimensioni WM

Inviato a una finestra dopo la modifica delle dimensioni.

Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) .


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
| <span id="SIZE_MAXHIDE"></span><span id="size_maxhide"></span><dl> <dt>**Dimensioni \_ MAXHIDE**</dt> <dt>4</dt> </dl>       | Il messaggio viene inviato a tutte le finestre popup quando un'altra finestra è ingrandita.<br/>                              |
| <span id="SIZE_MAXIMIZED"></span><span id="size_maximized"></span><dl> <dt>**Dimensioni \_ Ingrandita**</dt> <dt>2</dt> </dl> | La finestra è stata ingrandita.<br/>                                                                          |
| <span id="SIZE_MAXSHOW"></span><span id="size_maxshow"></span><dl> <dt>**Dimensioni \_ MAXSHOW**</dt> <dt>3</dt> </dl>       | Il messaggio viene inviato a tutte le finestre popup quando un'altra finestra è stata ripristinata alle dimensioni precedenti.<br/>      |
| <span id="SIZE_MINIMIZED"></span><span id="size_minimized"></span><dl> <dt>**Dimensioni \_ RIDOTTO a icona**</dt> <dt>1</dt> </dl> | La finestra è stata ridotta a icona.<br/>                                                                          |
| <span id="SIZE_RESTORED"></span><span id="size_restored"></span><dl> <dt>**Dimensioni \_ RIPRISTINAto**</dt> <dt>0</dt> </dl>    | La finestra è stata ridimensionata, ma non è stata applicata la **\_ riduzione delle dimensioni** né il valore **\_ ingrandito delle dimensioni** .<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

La parola di ordine inferiore di *lParam* specifica la nuova larghezza dell'area client.

La parola di ordine superiore di *lParam* specifica la nuova altezza dell'area client.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **LRESULT**

Se un'applicazione elabora il messaggio, deve restituire zero.

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

Esempio di [esempi di Windows classico](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/DirectWrite/HelloWorld/SimpleText.cpp) in GitHub.

## <a name="remarks"></a>Commenti

Se per una finestra figlio viene chiamata la funzione [**SetScrollPos**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx) o [**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow) come risultato del messaggio di **\_ dimensioni WM** , il parametro *bRedraw* o *bRepaint* deve essere diverso da zero per fare in modo che la finestra venga ridisegnata.

Sebbene la larghezza e l'altezza di una finestra siano valori a 32 bit, il parametro *lParam* contiene solo i 16 bit di ogni ordine inferiore.

La funzione [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) invia i messaggi di **\_ dimensioni WM** e di **\_ spostamento WM** quando elabora il messaggio [**WM \_ WINDOWPOSCHANGED**](wm-windowposchanged.md) .
I messaggi WM **\_ size** e **WM \_ Move** non vengono inviati se un'applicazione gestisce il messaggio **WM \_ WINDOWPOSCHANGED** senza chiamare **DefWindowProc**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                                               |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                     |
| Intestazione<br/>                   | <dl> <dt>Winuser. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**MoveWindow**](/windows/win32/api/winuser/nf-winuser-movewindow)
</dt> <dt>

[**\_WINDOWPOSCHANGED WM**](wm-windowposchanged.md)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**SetScrollPos**](https://msdn.microsoft.com/library/Cc411085(v=MSDN.10).aspx)
</dt> </dl>

 

 
