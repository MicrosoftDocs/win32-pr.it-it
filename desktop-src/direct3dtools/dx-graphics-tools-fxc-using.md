---
title: Compilazione offline
description: Lo strumento compilatore di effetti (fxc.exe) è progettato per la compilazione offline di shader HLSL.
ms.assetid: 56806335-a0c7-4247-b40d-ba93486a88ac
keywords:
- FXC, compilazione offline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e7c2bf96a24cb586a5d229a395cbf6dc0cb9ee1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729911"
---
# <a name="offline-compiling"></a><span data-ttu-id="8384e-104">Compilazione offline</span><span class="sxs-lookup"><span data-stu-id="8384e-104">Offline compiling</span></span>

<span data-ttu-id="8384e-105">Lo strumento compilatore di effetti (fxc.exe) è progettato per la compilazione offline di shader HLSL.</span><span class="sxs-lookup"><span data-stu-id="8384e-105">The effect-compiler tool (fxc.exe) is designed for offline compilation of HLSL shaders.</span></span>

## <a name="compiling-with-the-current-compiler"></a><span data-ttu-id="8384e-106">Compilazione con il compilatore corrente</span><span class="sxs-lookup"><span data-stu-id="8384e-106">Compiling with the current compiler</span></span>

<span data-ttu-id="8384e-107">I modelli shader supportati dal compilatore corrente sono visualizzati nei [profili](dx-graphics-tools-fxc-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="8384e-107">The shader models supported by the current compiler are shown in [Profiles](dx-graphics-tools-fxc-syntax.md).</span></span> <span data-ttu-id="8384e-108">Questo esempio compila un pixel shader per la destinazione del modello shader 5,1.</span><span class="sxs-lookup"><span data-stu-id="8384e-108">This example compiles a pixel shader for the shader model 5.1 target.</span></span>

```
fxc /T ps_5_1 /Fo PixelShader1.fxc PixelShader1.hlsl
```

<span data-ttu-id="8384e-109">In questo esempio:</span><span class="sxs-lookup"><span data-stu-id="8384e-109">In this example:</span></span>

-   <span data-ttu-id="8384e-110">PS \_ 5 \_ 1 è il profilo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="8384e-110">ps\_5\_1 is the target profile.</span></span>
-   <span data-ttu-id="8384e-111">PixelShader1. fxc è il file oggetto di output contenente lo shader compilato.</span><span class="sxs-lookup"><span data-stu-id="8384e-111">PixelShader1.fxc is the output object file containing the compiled shader.</span></span>
-   <span data-ttu-id="8384e-112">PixelShader1. HLSL è l'origine.</span><span class="sxs-lookup"><span data-stu-id="8384e-112">PixelShader1.hlsl is the source.</span></span>

```
fxc /Od /Zi /T ps_5_1 /Fo PixelShader1.fxc PixelShader1.hlsl
```

<span data-ttu-id="8384e-113">Le opzioni di debug includono opzioni aggiuntive per disabilitare le ottimizzazioni del compilatore (od) e abilitare le informazioni di debug (Zi), ad esempio i numeri di riga e i simboli.</span><span class="sxs-lookup"><span data-stu-id="8384e-113">The debug options include additional options to disable compiler optimizations (Od) and enable debug information (Zi) like line numbers and symbols.</span></span>

<span data-ttu-id="8384e-114">Per un elenco completo delle opzioni della riga di comando, vedere la pagina relativa alla [sintassi](dx-graphics-tools-fxc-syntax.md) .</span><span class="sxs-lookup"><span data-stu-id="8384e-114">For a full listing of the command-line options, see the [Syntax](dx-graphics-tools-fxc-syntax.md) page.</span></span>

## <a name="compiling-with-the-legacy-compiler"></a><span data-ttu-id="8384e-115">Compilazione con il compilatore legacy</span><span class="sxs-lookup"><span data-stu-id="8384e-115">Compiling with the legacy compiler</span></span>

<span data-ttu-id="8384e-116">A partire da Direct3D 10, alcuni modelli di shader non sono più supportati.</span><span class="sxs-lookup"><span data-stu-id="8384e-116">Beginning with Direct3D 10, some shader models are no longer supported.</span></span> <span data-ttu-id="8384e-117">Sono inclusi pixel shader modelli: PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3 e PS \_ 1 \_ 4 che supportano risorse molto limitate e che dipendono da hardware.</span><span class="sxs-lookup"><span data-stu-id="8384e-117">These include pixel shader models: ps\_1\_1, ps\_1\_2, ps\_1\_3, and ps\_1\_4 which support very limited resources and are dependent on hardware.</span></span> <span data-ttu-id="8384e-118">Il compilatore è stato riprogettato con il modello di shader 2 (o versione successiva), che consente una maggiore efficienza con la compilazione.</span><span class="sxs-lookup"><span data-stu-id="8384e-118">The compiler has been redesigned with shader model 2 (or greater) which allows for greater efficiencies with compilation.</span></span> <span data-ttu-id="8384e-119">Naturalmente, sarà necessario che l'utente sia in esecuzione su hardware che supporta i modelli shader 2 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="8384e-119">This of course will require that you are running on hardware that supports shader models 2 and greater.</span></span>

<span data-ttu-id="8384e-120">Si noti inoltre che è necessario consultare le note sulla versione dell'SDK associate alla versione del compilatore FXC per il comportamento interessato dall'opzione/GEC.</span><span class="sxs-lookup"><span data-stu-id="8384e-120">Also note that you should consult the SDK release notes associated with your version of the FXC compiler for behavior affected by the /Gec switch.</span></span>

## <a name="using-the-effect-compiler-tool-in-a-subprocess"></a><span data-ttu-id="8384e-121">Uso dello strumento di compilazione degli effetti in un sottoprocesso</span><span class="sxs-lookup"><span data-stu-id="8384e-121">Using the effect-compiler tool in a subprocess</span></span>

<span data-ttu-id="8384e-122">Se fxc.exe viene generato come sottoprocesso da un'applicazione, è importante assicurarsi che l'applicazione controlli e legga tutti i dati nelle pipe di output o di errore passati alla funzione CreateProcess.</span><span class="sxs-lookup"><span data-stu-id="8384e-122">If fxc.exe is spawned as a subprocess by an application it is important to ensure that the application checks for and reads any data in output or error pipes passed to the CreateProcess function.</span></span> <span data-ttu-id="8384e-123">Se l'applicazione attende solo il completamento del sottoprocesso e una delle pipe diventa completa, il sottoprocesso non viene mai completato.</span><span class="sxs-lookup"><span data-stu-id="8384e-123">If the application only waits for the subprocess to finish and one of the pipes becomes full the subprocess will never finish.</span></span>

<span data-ttu-id="8384e-124">Nell'esempio di codice seguente viene illustrato l'attesa di un sottoprocesso e la lettura delle pipe di output e di errore associate al sottoprocesso.</span><span class="sxs-lookup"><span data-stu-id="8384e-124">The following example code illustrates waiting on a subprocess and reading the output and error pipes attached to the subprocess.</span></span> <span data-ttu-id="8384e-125">Il contenuto della `WaitHandles` matrice corrisponde agli handle per il sottoprocesso, alla pipe per stdout e alla pipe per stderr.</span><span class="sxs-lookup"><span data-stu-id="8384e-125">The contents of the `WaitHandles` array correspond to handles for the subprocess, the pipe for stdout and the pipe for stderr.</span></span>

```cpp
HANDLE WaitHandles[] = {
  piProcInfo.hProcess, hReadOutPipe, hReadErrorPipe
};

const DWORD BUFSIZE = 4096;
BYTE buff[BUFSIZE];

while (1)
{
    DWORD dwBytesRead, dwBytesAvailable;

    dwWaitResult = WaitForMultipleObjects(3, WaitHandles, FALSE, 60000L);

    // Read from the pipes...
    while (PeekNamedPipe(hReadOutPipe, NULL, 0, NULL, &dwBytesAvailable, NULL) && dwBytesAvailable)
    {
        ReadFile(hReadOutPipe, buff, BUFSIZE - 1, &dwBytesRead, 0);
        streamOut << std::string((char*)buff, (size_t)dwBytesRead);
    }
    while (PeekNamedPipe(hReadErrorPipe, NULL, 0, NULL, &dwBytesAvailable, NULL) && dwBytesAvailable)
    {
        ReadFile(hReadErrorPipe, buff, BUFSIZE - 1, &dwBytesRead, 0);
        streamError << std::string((char*)buff, (size_t)dwBytesRead);
    }

    // Process is done, or we timed out:
    if (dwWaitResult == WAIT_OBJECT_0 || dwWaitResult == WAIT_TIMEOUT)
        break;
}
```

<span data-ttu-id="8384e-126">Per ulteriori informazioni sulla generazione di un processo, vedere la pagina di riferimento per [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span><span class="sxs-lookup"><span data-stu-id="8384e-126">For additional information on spawning a process see the reference page for [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8384e-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8384e-127">Related topics</span></span>

* [<span data-ttu-id="8384e-128">Effect-strumento compilatore</span><span class="sxs-lookup"><span data-stu-id="8384e-128">Effect-Compiler Tool</span></span>](fxc.md)