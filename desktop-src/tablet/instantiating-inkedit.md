---
description: Questo argomento descrive i vari modi in cui è possibile creare un'istanza di un controllo InkEdit.
ms.assetid: 3ab0f10e-1a0d-4d0b-b5b2-69dc96570b33
title: Creazione di istanze di InkEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53df76fea92077e2d1dbfaea57213ad95cdccf91a4b40267cec02e28b887b984
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032019"
---
# <a name="instantiating-inkedit"></a>Creazione di istanze di InkEdit

Questo argomento descrive i vari modi in cui è possibile creare un'istanza di [un controllo InkEdit.](inkedit-control.md)

## <a name="visual-basic-net-and-c"></a>Visual Basic .NET e C\#

Se si utilizza Microsoft Visual Basic .NET o C, trascinare il controllo InkEdit dalla casella degli strumenti in Visual Studio al form o alla pagina in cui si vuole visualizzare \# il controllo. [](./inkedit-control.md)

## <a name="win32c"></a>Win32/C++

Il [controllo InkEdit](inkedit-control-reference.md) è una superclasse del controllo incorporabile OLE Rich Edit 4.5 Win32.

Le applicazioni Win32 creano un'istanza del controllo [InkEdit](inkedit-control-reference.md) chiamando [CreateWindow()](/windows/win32/api/winuser/nf-winuser-createwindowa) e passando INKEDIT come classe della finestra. INKEDIT è definito in InkEd.h. Dopo aver creato il controllo, è possibile "parlare" con il controllo con messaggi. I messaggi RICH Edit (EM) vengono passati da InkEdit a \_ Rich Edit inalterati. Sono disponibili tutte le \* funzionalità rich edit esistenti.

Per creare un [controllo InkEdit,](inkedit-control-reference.md) chiamare la [funzione CreateWindow()](/windows/win32/api/winuser/nf-winuser-createwindowa) specificando la classe della finestra InkEdit. Usare [LoadLibrary()](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) per registrare InkEd.dll. Specificare la costante definita da INKEDIT CLASS per il parametro della classe window e usare \_ gli stili della finestra come specificato negli esempi seguenti.

### <a name="instantiating-a-multiline-inkedit-control"></a>Creazione di un'istanza di un controllo InkEdit su più righe


```C++
//...
HMODULE s_hlib;    
s_hlib= LoadLibrary("InkEd.dll");
//...
m_hwndInkEdit = CreateWindowW(INKEDIT_CLASS, NULL,
WS_CHILD|WS_VISIBLE|WS_BORDER|ES_MULTILINE,
rt.left, rt.top, rt.right, rt.bottom,
m_hWnd, NULL, hInst, NULL);
```



### <a name="instantiating-a-single-line-inkedit-control"></a>Creazione di un'istanza Single-Line controllo InkEdit


```C++
//...
HMODULE s_hlib;    
s_hlib= LoadLibrary("InkEd.dll");
//...
m_hwndInkEdit = CreateWindowW(INKEDIT_CLASS, NULL,
WS_CHILD|WS_VISIBLE|WS_BORDER,
rt.left, rt.top, rt.right, rt.bottom,
m_hWnd, NULL, hInst, NULL);
```



> [!Note]  
> A differenza di RichEdit, è necessario chiamare [CoInitialize()](/windows/win32/api/objbase/nf-objbase-coinitialize) prima di creare il [controllo InkEdit.](inkedit-control-reference.md) Chiamare [CoUninitialize() quando](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) l'applicazione viene arrestata. Dopo aver chiamato CoUninitialize(), è necessario chiamare [FreeLibrary(s \_ hlib)](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) per decrementare il conteggio dei riferimenti InkEdit.dll file.

 

Se si usa lo stile della finestra [ \_ ES NOIME,](../controls/rich-edit-control-styles.md) il supporto delle correzioni predefinito non è disponibile. Se non si specifica una finestra padre, il controllo viene creato come finestra di primo livello e viene aggiunto lo stile SYSMENU WS. In questo modo viene disabilitato anche il supporto della correzione \_ predefinito.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Aggiunta di controlli input penna a un Project](adding-ink-controls-to-a-project.md)
</dt> </dl>

 

 
