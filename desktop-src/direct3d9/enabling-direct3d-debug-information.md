---
description: Si sta provando a trovare altre informazioni sugli oggetti Direct3D durante il debug? Ad esempio, lo screenshot seguente mostra ciò che viene visualizzato in genere quando si esamina un'interfaccia Direct3D nella finestra espressioni di controllo.
ms.assetid: 365451f8-e93e-4cc4-b688-2e668518c245
title: Abilitazione di informazioni di debug Direct3D (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17bb46cf8658d0417d021faa6bdbefd10822d1dd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123354"
---
# <a name="enabling-direct3d-debug-information-direct3d-9"></a><span data-ttu-id="43bde-104">Abilitazione di informazioni di debug Direct3D (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="43bde-104">Enabling Direct3D Debug Information (Direct3D 9)</span></span>

<span data-ttu-id="43bde-105">Si sta provando a trovare altre informazioni sugli oggetti Direct3D durante il debug?</span><span class="sxs-lookup"><span data-stu-id="43bde-105">Are you trying to find out more information about Direct3D objects during debug?</span></span> <span data-ttu-id="43bde-106">Ad esempio, lo screenshot seguente mostra ciò che viene visualizzato in genere quando si esamina un'interfaccia Direct3D nella finestra espressioni di controllo.</span><span class="sxs-lookup"><span data-stu-id="43bde-106">For instance, the following screen shot shows what you typically see when you look at a Direct3D interface in the watch window.</span></span>

![Screenshot di un'interfaccia Direct3D nella finestra espressioni di controllo](images/d3d-debug-info1.png)

<span data-ttu-id="43bde-108">È possibile abilitare gli oggetti di debug di base in modo che un oggetto con mirroring che contiene tutte le proprietà dell'oggetto possa essere visualizzato nella finestra espressioni di controllo.</span><span class="sxs-lookup"><span data-stu-id="43bde-108">You can enable the core debug objects so that a mirrored object which contains all of the properties of the object can be viewed in the watch window.</span></span> <span data-ttu-id="43bde-109">È sufficiente includere i seguenti elementi \# define nel codice prima del file d3d9. h:</span><span class="sxs-lookup"><span data-stu-id="43bde-109">Simply include the following \#define in your code before the D3D9.h file:</span></span>


```
#define D3D_DEBUG_INFO
```



<span data-ttu-id="43bde-110">Per abilitare le informazioni di debug, è \# necessario compilare l'oggetto define prima del file d3d9. h (qualsiasi programma che usa DXUT consentirà automaticamente le \_ \_ informazioni di debug di D3D quando il programma viene compilato per il debug).</span><span class="sxs-lookup"><span data-stu-id="43bde-110">To enable debug information, the \#define must get built before the D3D9.h file (Any program using DXUT will automatically enable D3D\_DEBUG\_INFO when the program is compiled for debug).</span></span> <span data-ttu-id="43bde-111">Se si esegue un esempio di SDK, è possibile visualizzarlo in DXStdAfx. h, che ha effetto su tutti gli esempi di C++.</span><span class="sxs-lookup"><span data-stu-id="43bde-111">If you are running a SDK sample, you can see this in DXStdAfx.h (which affects all the C++ samples).</span></span> <span data-ttu-id="43bde-112">È anche necessario eseguire debug Direct3D Runtime, che può essere abilitato dal pannello di controllo, se necessario.</span><span class="sxs-lookup"><span data-stu-id="43bde-112">You must also be running the debug Direct3D runtime (which can be enabled from the Control Panel if necessary).</span></span>

<span data-ttu-id="43bde-113">Di seguito è riportato un esempio che usa l' [esempio BasicHLSL](https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="43bde-113">Here's an example using the [BasicHLSL Sample](https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx).</span></span>

1.  <span data-ttu-id="43bde-114">Aggiungere la \# definizione al file Dxstdafx. h prima della riga 37.</span><span class="sxs-lookup"><span data-stu-id="43bde-114">Add the \#define to the Dxstdafx.h file before line 37.</span></span>
2.  <span data-ttu-id="43bde-115">Compilare un progetto di debug.</span><span class="sxs-lookup"><span data-stu-id="43bde-115">Build a debug project.</span></span>
3.  <span data-ttu-id="43bde-116">Impostare un punto di interruzione alla riga 307 in BasicHLSL. cpp</span><span class="sxs-lookup"><span data-stu-id="43bde-116">Set a breakpoint at line 307 in BasicHLSL.cpp</span></span>
4.  <span data-ttu-id="43bde-117">Eseguire il debugger.</span><span class="sxs-lookup"><span data-stu-id="43bde-117">Run the debugger.</span></span>

<span data-ttu-id="43bde-118">Lo screenshot seguente mostra il tipo di informazioni dettagliate che è possibile ottenere su un oggetto trama Direct3D dalla finestra espressioni di controllo.</span><span class="sxs-lookup"><span data-stu-id="43bde-118">The following screen shot shows the kind of detailed information you can get about a Direct3D texture object from the watch window.</span></span>

![Screenshot di un oggetto trama Direct3D nella finestra espressioni di controllo](images/d3d-debug-info2.png)

> [!Note]
>
> <span data-ttu-id="43bde-120">I nomi delle proprietà dell'oggetto sono visibili e i valori sono corretti solo quando il runtime di debug è abilitato.</span><span class="sxs-lookup"><span data-stu-id="43bde-120">The object property names are visible and the values are correct only when the debug runtime is enabled.</span></span> <span data-ttu-id="43bde-121">Quando si esegue il runtime di vendita al dettaglio, i valori non sono validi.</span><span class="sxs-lookup"><span data-stu-id="43bde-121">When running against the retail runtime, the values are invalid.</span></span>

 

## <a name="use-the-call-stack-for-extended-debug"></a><span data-ttu-id="43bde-122">Usare lo stack di chiamate per il debug esteso</span><span class="sxs-lookup"><span data-stu-id="43bde-122">Use the Call Stack for Extended Debug</span></span>

<span data-ttu-id="43bde-123">Con il debug Direct3D abilitato, è anche possibile esaminare uno stack di chiamate ogni volta che viene creato un oggetto.</span><span class="sxs-lookup"><span data-stu-id="43bde-123">With Direct3D debug enabled, you can also look at a call stack each time an object is created.</span></span> <span data-ttu-id="43bde-124">Questa operazione renderà l'applicazione molto lenta, ma può essere usata per verificare la presenza di perdite di risorse.</span><span class="sxs-lookup"><span data-stu-id="43bde-124">This will make your application very slow, but can be used to check for resource leaks.</span></span> <span data-ttu-id="43bde-125">Per scrivere lo stack di chiamate, impostare la seguente chiave del registro di sistema su 1:</span><span class="sxs-lookup"><span data-stu-id="43bde-125">To write out the call stack, set the following registry key to 1:</span></span>


```
\\HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Direct3D\\
D3D9Debugging\\EnableCreationStack
```



<span data-ttu-id="43bde-126">La compilazione dell'applicazione con il debug abilitato consente di accedere a questa variabile aggiuntiva:</span><span class="sxs-lookup"><span data-stu-id="43bde-126">Building your application with debug enabled will give you access to this additional variable:</span></span>


```
  LPCWSTR CreationCallStack;
```



<span data-ttu-id="43bde-127">Questa variabile archivia lo stack di chiamate ogni volta che viene creato un oggetto.</span><span class="sxs-lookup"><span data-stu-id="43bde-127">This variable will store the call stack each time that an object is created.</span></span> <span data-ttu-id="43bde-128">Questa operazione renderà l'applicazione molto lenta, ma può essere usata per eseguire il debug delle perdite di risorse.</span><span class="sxs-lookup"><span data-stu-id="43bde-128">This will make your application very slow, but can be used to debug resource leaks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="43bde-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="43bde-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43bde-130">Suggerimenti per la programmazione</span><span class="sxs-lookup"><span data-stu-id="43bde-130">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 



