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
# <a name="instantiating-inkedit"></a><span data-ttu-id="2d5e8-103">Creazione di un'istanza di InkEdit</span><span class="sxs-lookup"><span data-stu-id="2d5e8-103">Instantiating InkEdit</span></span>

<span data-ttu-id="2d5e8-104">In questo argomento vengono descritti i vari modi in cui è possibile creare un'istanza di un controllo [InkEdit](inkedit-control.md) .</span><span class="sxs-lookup"><span data-stu-id="2d5e8-104">This topic describes the various ways that you can instantiate an [InkEdit](inkedit-control.md) control.</span></span>

## <a name="visual-basic-net-and-c"></a><span data-ttu-id="2d5e8-105">Visual Basic .NET e C\#</span><span class="sxs-lookup"><span data-stu-id="2d5e8-105">Visual Basic .NET and C\#</span></span>

<span data-ttu-id="2d5e8-106">Se si utilizza Microsoft Visual Basic .NET o C \# , trascinare il controllo [InkEdit](./inkedit-control.md) dalla casella degli strumenti in Visual Studio nel form o nella pagina in cui si desidera visualizzare il controllo.</span><span class="sxs-lookup"><span data-stu-id="2d5e8-106">If you are working with Microsoft Visual Basic .NET or C\#, drag the [InkEdit](./inkedit-control.md) control from the Toolbox in Visual Studio to the form or page where you want the control to appear.</span></span>

## <a name="win32c"></a><span data-ttu-id="2d5e8-107">Win32/C++</span><span class="sxs-lookup"><span data-stu-id="2d5e8-107">Win32/C++</span></span>

<span data-ttu-id="2d5e8-108">Il controllo [InkEdit](inkedit-control-reference.md) è una superclasse del controllo Rich Edit 4,5 OLE incorporabile di Win32.</span><span class="sxs-lookup"><span data-stu-id="2d5e8-108">The [InkEdit](inkedit-control-reference.md) control is a superclass of the Rich Edit 4.5 Win32 OLE embeddable control.</span></span>

<span data-ttu-id="2d5e8-109">Le applicazioni Win32 creano un'istanza del controllo [InkEdit](inkedit-control-reference.md) chiamando [CreateWindow ()](/windows/win32/api/winuser/nf-winuser-createwindowa) e passando InkEdit come classe della finestra.</span><span class="sxs-lookup"><span data-stu-id="2d5e8-109">Win32 applications instantiate the [InkEdit](inkedit-control-reference.md) control by calling [CreateWindow()](/windows/win32/api/winuser/nf-winuser-createwindowa) and passing INKEDIT as the window class.</span></span> <span data-ttu-id="2d5e8-110">INKEDIT è definito in inchiostrate. h.</span><span class="sxs-lookup"><span data-stu-id="2d5e8-110">INKEDIT is defined in InkEd.h.</span></span> <span data-ttu-id="2d5e8-111">Una volta creato il controllo, è possibile "comunicare" con il controllo con i messaggi.</span><span class="sxs-lookup"><span data-stu-id="2d5e8-111">After the control is created, you can "talk" to the control with messages.</span></span> <span data-ttu-id="2d5e8-112">I messaggi Rich Edit (EM \_ \* ) vengono passati da InkEdit a Rich Edit non modificati; tutte le funzionalità di modifica avanzate sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="2d5e8-112">Rich Edit messages (EM\_\*) are passed from InkEdit to Rich Edit unaltered; all of the existing Rich Edit functionality is available.</span></span>

<span data-ttu-id="2d5e8-113">Per creare un controllo [InkEdit](inkedit-control-reference.md) , chiamare la funzione [CreateWindow ()](/windows/win32/api/winuser/nf-winuser-createwindowa) specificando la classe della finestra InkEdit.</span><span class="sxs-lookup"><span data-stu-id="2d5e8-113">To create an [InkEdit](inkedit-control-reference.md) control, call the [CreateWindow()](/windows/win32/api/winuser/nf-winuser-createwindowa) function, specifying the InkEdit window class.</span></span> <span data-ttu-id="2d5e8-114">Usare [LoadLibrary ()](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) per registrare InkEd.dll.</span><span class="sxs-lookup"><span data-stu-id="2d5e8-114">Use [LoadLibrary()](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) to register InkEd.dll.</span></span> <span data-ttu-id="2d5e8-115">Specificare la \_ costante definita dalla classe INKEDIT per il parametro della classe della finestra e utilizzare gli stili della finestra come specificato negli esempi seguenti.</span><span class="sxs-lookup"><span data-stu-id="2d5e8-115">Specify the INKEDIT\_CLASS defined constant for the window class parameter and use the window styles as specified in the following examples.</span></span>

### <a name="instantiating-a-multiline-inkedit-control"></a><span data-ttu-id="2d5e8-116">Creazione di un'istanza di un controllo InkEdit su più righe</span><span class="sxs-lookup"><span data-stu-id="2d5e8-116">Instantiating a Multiline InkEdit Control</span></span>


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



### <a name="instantiating-a-single-line-inkedit-control"></a><span data-ttu-id="2d5e8-117">Creazione di un'istanza di un controllo Single-Line InkEdit</span><span class="sxs-lookup"><span data-stu-id="2d5e8-117">Instantiating a Single-Line InkEdit Control</span></span>


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
> <span data-ttu-id="2d5e8-118">A differenza di RichEdit, è necessario assicurarsi di chiamare [CoInitialize ()](/windows/win32/api/objbase/nf-objbase-coinitialize) prima di creare il controllo [InkEdit](inkedit-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="2d5e8-118">Unlike with RichEdit, you must be sure to call [CoInitialize()](/windows/win32/api/objbase/nf-objbase-coinitialize) before creating the [InkEdit](inkedit-control-reference.md) control.</span></span> <span data-ttu-id="2d5e8-119">Chiamare [CoUninitialize ()](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) quando l'applicazione viene arrestata.</span><span class="sxs-lookup"><span data-stu-id="2d5e8-119">Call [CoUninitialize()](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) when your application shuts down.</span></span> <span data-ttu-id="2d5e8-120">Dopo la chiamata a CoUninitialize (), è necessario chiamare [FreeLibrary (s \_ hLib)](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) per decrementare il conteggio dei riferimenti sul file InkEdit.dll.</span><span class="sxs-lookup"><span data-stu-id="2d5e8-120">After calling CoUninitialize(), you must call [FreeLibrary(s\_hlib)](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) to decrement the reference count on the InkEdit.dll file.</span></span>

 

<span data-ttu-id="2d5e8-121">Se si usa lo stile della finestra [es \_ Claudio](../controls/rich-edit-control-styles.md) , il supporto predefinito per la correzione non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="2d5e8-121">If you use the [ES\_NOIME](../controls/rich-edit-control-styles.md) window style, the built-in correction support is not available.</span></span> <span data-ttu-id="2d5e8-122">Se non si specifica una finestra padre, il controllo viene creato come finestra di primo livello e \_ viene aggiunto lo stile WS SYSMENU. viene inoltre disabilitato il supporto per la correzione incorporata.</span><span class="sxs-lookup"><span data-stu-id="2d5e8-122">If you don't specify a parent window, the control is created as a top-level window and the WS\_SYSMENU style is added; this also disables the built-in correction support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d5e8-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2d5e8-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d5e8-124">Aggiunta di controlli Ink a un progetto</span><span class="sxs-lookup"><span data-stu-id="2d5e8-124">Adding Ink Controls to a Project</span></span>](adding-ink-controls-to-a-project.md)
</dt> </dl>

 

 
