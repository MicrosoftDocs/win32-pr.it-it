---
description: In questo argomento vengono descritti i vari modi in cui è possibile creare un'istanza di un controllo InkEdit.
ms.assetid: 3ab0f10e-1a0d-4d0b-b5b2-69dc96570b33
title: Creazione di un'istanza di InkEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bde7e94566b076a4d9d6f6928fc08199ee71fa19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485196"
---
# <a name="instantiating-inkedit"></a>Creazione di un'istanza di InkEdit

In questo argomento vengono descritti i vari modi in cui è possibile creare un'istanza di un controllo [InkEdit](inkedit-control.md) .

## <a name="visual-basic-net-and-c"></a>Visual Basic .NET e C\#

Se si utilizza Microsoft Visual Basic .NET o C \# , trascinare il controllo [InkEdit](./inkedit-control.md) dalla casella degli strumenti in Visual Studio nel form o nella pagina in cui si desidera visualizzare il controllo.

## <a name="win32c"></a>Win32/C++

Il controllo [InkEdit](inkedit-control-reference.md) è una superclasse del controllo Rich Edit 4,5 OLE incorporabile di Win32.

Le applicazioni Win32 creano un'istanza del controllo [InkEdit](inkedit-control-reference.md) chiamando [CreateWindow ()](/windows/win32/api/winuser/nf-winuser-createwindowa) e passando InkEdit come classe della finestra. INKEDIT è definito in inchiostrate. h. Una volta creato il controllo, è possibile "comunicare" con il controllo con i messaggi. I messaggi Rich Edit (EM \_ \* ) vengono passati da InkEdit a Rich Edit non modificati; tutte le funzionalità di modifica avanzate sono disponibili.

Per creare un controllo [InkEdit](inkedit-control-reference.md) , chiamare la funzione [CreateWindow ()](/windows/win32/api/winuser/nf-winuser-createwindowa) specificando la classe della finestra InkEdit. Usare [LoadLibrary ()](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) per registrare InkEd.dll. Specificare la \_ costante definita dalla classe INKEDIT per il parametro della classe della finestra e utilizzare gli stili della finestra come specificato negli esempi seguenti.

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



### <a name="instantiating-a-single-line-inkedit-control"></a>Creazione di un'istanza di un controllo Single-Line InkEdit


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
> A differenza di RichEdit, è necessario assicurarsi di chiamare [CoInitialize ()](/windows/win32/api/objbase/nf-objbase-coinitialize) prima di creare il controllo [InkEdit](inkedit-control-reference.md) . Chiamare [CoUninitialize ()](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) quando l'applicazione viene arrestata. Dopo la chiamata a CoUninitialize (), è necessario chiamare [FreeLibrary (s \_ hLib)](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) per decrementare il conteggio dei riferimenti sul file InkEdit.dll.

 

Se si usa lo stile della finestra [es \_ Claudio](../controls/rich-edit-control-styles.md) , il supporto predefinito per la correzione non è disponibile. Se non si specifica una finestra padre, il controllo viene creato come finestra di primo livello e \_ viene aggiunto lo stile WS SYSMENU. viene inoltre disabilitato il supporto per la correzione incorporata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Aggiunta di controlli Ink a un progetto](adding-ink-controls-to-a-project.md)
</dt> </dl>

 

 
