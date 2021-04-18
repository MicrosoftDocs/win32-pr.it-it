---
description: Questo argomento elenca le categorie comuni di problemi che possono verificarsi durante la scrittura di applicazioni Direct3D e come evitarli.
ms.assetid: 27b87f0f-7118-4252-b6e8-6ea18a9399e4
title: Risoluzione dei problemi (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6726e761dd8c15e2da18e6c370472a73e82cef0b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304359"
---
# <a name="troubleshooting-direct3d-9"></a><span data-ttu-id="25cd6-103">Risoluzione dei problemi (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="25cd6-103">Troubleshooting (Direct3D 9)</span></span>

<span data-ttu-id="25cd6-104">Questo argomento elenca le categorie comuni di problemi che possono verificarsi durante la scrittura di applicazioni Direct3D e come evitarli.</span><span class="sxs-lookup"><span data-stu-id="25cd6-104">This topic lists common categories of problems that you might encounter when writing Direct3D applications, and how to prevent them.</span></span>

## <a name="device-creation"></a><span data-ttu-id="25cd6-105">Creazione del dispositivo</span><span class="sxs-lookup"><span data-stu-id="25cd6-105">Device Creation</span></span>

<span data-ttu-id="25cd6-106">Se l'applicazione non riesce durante la creazione del dispositivo, verificare gli errori comuni seguenti.</span><span class="sxs-lookup"><span data-stu-id="25cd6-106">If your application fails during device creation, check for the following common errors.</span></span>

-   <span data-ttu-id="25cd6-107">Assicurarsi di controllare le funzionalità del dispositivo, in particolare le profondità di rendering.</span><span class="sxs-lookup"><span data-stu-id="25cd6-107">Make sure you check the device capabilities, particularly the render depths.</span></span>
-   <span data-ttu-id="25cd6-108">Esaminare il codice di errore.</span><span class="sxs-lookup"><span data-stu-id="25cd6-108">Examine the error code.</span></span> <span data-ttu-id="25cd6-109">\_OUTOFVIDEOMEMORY D3DERR è sempre possibile.</span><span class="sxs-lookup"><span data-stu-id="25cd6-109">D3DERR\_OUTOFVIDEOMEMORY is always possible.</span></span>
-   <span data-ttu-id="25cd6-110">Usare le librerie di collegamento dinamico (dll) di debug di DirectX ed esaminare i messaggi di output nel debugger.</span><span class="sxs-lookup"><span data-stu-id="25cd6-110">Use the debug DirectX dynamic-link libraries (DLLs) and review output messages under the debugger.</span></span>

## <a name="using-lit-vertices"></a><span data-ttu-id="25cd6-111">Uso di vertici illuminati</span><span class="sxs-lookup"><span data-stu-id="25cd6-111">Using Lit Vertices</span></span>

<span data-ttu-id="25cd6-112">Le applicazioni che usano i vertici illuminati devono disabilitare il motore di illuminazione Direct3D impostando lo \_ stato di rendering dell'illuminazione D3DRS su **false**.</span><span class="sxs-lookup"><span data-stu-id="25cd6-112">Applications that use lit vertices should disable the Direct3D lighting engine by setting the D3DRS\_LIGHTING render state to **FALSE**.</span></span> <span data-ttu-id="25cd6-113">Per impostazione predefinita, quando l'illuminazione è abilitata, il sistema imposta il colore per qualsiasi vertice che non contiene un vettore normale a 0 (nero), anche se il vertice di input contiene un valore di colore diverso da zero.</span><span class="sxs-lookup"><span data-stu-id="25cd6-113">By default, when lighting is enabled, the system sets the color for any vertex that doesn't contain a normal vector to 0 (black), even if the input vertex contained a nonzero color value.</span></span> <span data-ttu-id="25cd6-114">Poiché i vertici illuminati non sono, per loro natura, contengono una normale del vertice, le informazioni sui colori passate a Direct3D vengono perse durante il rendering se il motore di illuminazione è abilitato.</span><span class="sxs-lookup"><span data-stu-id="25cd6-114">Because lit-vertices don't, by their nature, contain a vertex normal, any color information passed to Direct3D is lost during rendering if the lighting engine is enabled.</span></span>

<span data-ttu-id="25cd6-115">Ovviamente, il colore del vertice è importante per qualsiasi applicazione che esegue la propria illuminazione.</span><span class="sxs-lookup"><span data-stu-id="25cd6-115">Obviously, vertex color is important to any application that performs its own lighting.</span></span> <span data-ttu-id="25cd6-116">Per impedire al sistema di imporre i valori predefiniti, assicurarsi di impostare D3DRS \_ Lighting su **false**.</span><span class="sxs-lookup"><span data-stu-id="25cd6-116">To prevent the system from imposing the default values, make sure you set D3DRS\_LIGHTING to **FALSE**.</span></span>

<span data-ttu-id="25cd6-117">Se l'applicazione è in esecuzione ma non è visibile, verificare gli errori comuni seguenti.</span><span class="sxs-lookup"><span data-stu-id="25cd6-117">If your application runs but nothing is visible, check for the following common errors.</span></span>

-   <span data-ttu-id="25cd6-118">Assicurarsi che i triangoli non siano degenerati.</span><span class="sxs-lookup"><span data-stu-id="25cd6-118">Ensure that your triangles are not degenerate.</span></span>
-   <span data-ttu-id="25cd6-119">Assicurarsi che i triangoli non vengano abbattuti.</span><span class="sxs-lookup"><span data-stu-id="25cd6-119">Ensure that your triangles are not being culled.</span></span>
-   <span data-ttu-id="25cd6-120">Assicurarsi che le trasformazioni siano coerenti internamente.</span><span class="sxs-lookup"><span data-stu-id="25cd6-120">Make sure that your transformations are internally consistent.</span></span>
-   <span data-ttu-id="25cd6-121">Controllare le impostazioni del viewport per assicurarsi che consentano di visualizzare i triangoli.</span><span class="sxs-lookup"><span data-stu-id="25cd6-121">Check the viewport settings to be sure they allow your triangles to be seen.</span></span>

## <a name="debugging"></a><span data-ttu-id="25cd6-122">Debug</span><span class="sxs-lookup"><span data-stu-id="25cd6-122">Debugging</span></span>

<span data-ttu-id="25cd6-123">Il debug di un'applicazione Direct3D può risultare complesso.</span><span class="sxs-lookup"><span data-stu-id="25cd6-123">Debugging a Direct3D application can be challenging.</span></span> <span data-ttu-id="25cd6-124">Provare le tecniche seguenti, oltre a controllare tutti i valori restituiti, un suggerimento particolarmente importante nella programmazione Direct3D, che dipende da implementazioni hardware molto diverse.</span><span class="sxs-lookup"><span data-stu-id="25cd6-124">Try the following techniques, in addition to checking all the return values - a particularly important piece of advice in Direct3D programming, which is dependent on very different hardware implementations.</span></span>

-   <span data-ttu-id="25cd6-125">Passa a debug di dll.</span><span class="sxs-lookup"><span data-stu-id="25cd6-125">Switch to debug DLLs.</span></span>
-   <span data-ttu-id="25cd6-126">Forzare un dispositivo solo software, disattivando l'accelerazione hardware anche quando è disponibile.</span><span class="sxs-lookup"><span data-stu-id="25cd6-126">Force a software-only device, turning off hardware acceleration even when it is available.</span></span>
-   <span data-ttu-id="25cd6-127">Forzare le superfici nella memoria di sistema.</span><span class="sxs-lookup"><span data-stu-id="25cd6-127">Force surfaces into system memory.</span></span>
-   <span data-ttu-id="25cd6-128">Creare un'opzione per l'esecuzione in una finestra, in modo che sia possibile utilizzare un debugger integrato.</span><span class="sxs-lookup"><span data-stu-id="25cd6-128">Create an option to run in a window, so that you can use an integrated debugger.</span></span>

<span data-ttu-id="25cd6-129">La seconda e la terza opzione in questo elenco consentono di evitare il blocco Win16 che può altrimenti causare il blocco del debugger.</span><span class="sxs-lookup"><span data-stu-id="25cd6-129">The second and third options in this list can help you avoid the Win16 lock which can otherwise cause your debugger to hang.</span></span>

<span data-ttu-id="25cd6-130">Provare anche ad aggiungere le voci seguenti a Win.ini.</span><span class="sxs-lookup"><span data-stu-id="25cd6-130">Also, try adding the following entries to Win.ini.</span></span>


```
[Direct3D] 
debug=3 
[DirectDraw] 
debug=3 
```



## <a name="borland-floating-point-initialization"></a><span data-ttu-id="25cd6-131">Inizializzazione Floating-Point Borland</span><span class="sxs-lookup"><span data-stu-id="25cd6-131">Borland Floating-Point Initialization</span></span>

<span data-ttu-id="25cd6-132">I compilatori di Borland segnalano eccezioni a virgola mobile in modo non compatibile con Direct3D.</span><span class="sxs-lookup"><span data-stu-id="25cd6-132">Compilers from Borland report floating-point exceptions in a manner that is incompatible with Direct3D.</span></span> <span data-ttu-id="25cd6-133">Per risolvere questo problema, includere un \_ gestore di eccezioni matherr come il seguente:</span><span class="sxs-lookup"><span data-stu-id="25cd6-133">To solve this problem, include a \_matherr exception handler like the following:</span></span>


```
// Borland floating point initialization 
#include <math.h>
#include <float.h>

void initfp(void)
{
    // Disable floating point exceptions
    _control87(MCW_EM,MCW_EM);
}

int _matherr(struct _exception  *e)
{
    e;               // Dummy reference to catch the warning
    return 1;        // Error has been handled
}
```



## <a name="parameter-validation"></a><span data-ttu-id="25cd6-134">Convalida dei parametri</span><span class="sxs-lookup"><span data-stu-id="25cd6-134">Parameter Validation</span></span>

<span data-ttu-id="25cd6-135">Per motivi di prestazioni, la versione di debug del tempo di esecuzione di Direct3D immediate Mode esegue una maggiore convalida dei parametri rispetto alla versione finale, che talvolta non esegue alcuna convalida.</span><span class="sxs-lookup"><span data-stu-id="25cd6-135">For performance reasons, the debug version of the Direct3D Immediate Mode run time performs more parameter validation than the retail version, which sometimes performs no validation at all.</span></span> <span data-ttu-id="25cd6-136">Ciò consente alle applicazioni di eseguire il debug affidabile con il componente runtime di debug più lento prima di utilizzare la versione definitiva più veloce per l'ottimizzazione delle prestazioni e la versione finale.</span><span class="sxs-lookup"><span data-stu-id="25cd6-136">This enables applications to perform robust debugging with the slower debug run-time component before using the faster retail version for performance tuning and final release.</span></span>

<span data-ttu-id="25cd6-137">Sebbene diversi metodi in modalità immediata Direct3D impongano limiti sui valori che possono accettare, questi limiti vengono spesso controllati e applicati solo dalla versione di debug del runtime di esecuzione in modalità immediata Direct3D.</span><span class="sxs-lookup"><span data-stu-id="25cd6-137">Although several Direct3D Immediate Mode methods impose limits on the values that they can accept, these limits are often only checked and enforced by the debug version of the Direct3D Immediate Mode run time.</span></span> <span data-ttu-id="25cd6-138">Le applicazioni devono essere conformi a questi limiti, oppure possono verificarsi risultati imprevedibili e non desiderabili durante l'esecuzione nella versione finale di Direct3D.</span><span class="sxs-lookup"><span data-stu-id="25cd6-138">Applications must conform to these limits, or unpredictable and undesirable results can occur when running on the retail version of Direct3D.</span></span> <span data-ttu-id="25cd6-139">Ad esempio, il metodo [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) accetta un parametro (primitiveCount) che indica il numero di primitive di cui il metodo eseguirà il rendering.</span><span class="sxs-lookup"><span data-stu-id="25cd6-139">For example, the [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) method accepts a parameter (PrimitiveCount) that indicates the number of primitives that the method will render.</span></span> <span data-ttu-id="25cd6-140">Il metodo può accettare solo valori compresi tra 0 e D3DMAXNUMPRIMITIVES.</span><span class="sxs-lookup"><span data-stu-id="25cd6-140">The method can only accept values between 0 and D3DMAXNUMPRIMITIVES.</span></span> <span data-ttu-id="25cd6-141">Nella versione di debug di Direct3D, se si passano più di D3DMAXNUMPRIMITIVES primitive, il metodo ha esito negativo correttamente, stampa un messaggio di errore nel log degli errori e restituisce un valore di errore all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="25cd6-141">In the debug version of Direct3D, if you pass more than D3DMAXNUMPRIMITIVES primitives, the method fails gracefully, printing an error message to the error log, and returning an error value to your application.</span></span> <span data-ttu-id="25cd6-142">Viceversa, se l'applicazione esegue lo stesso errore quando viene eseguita con la versione definitiva del runtime, il comportamento non è definito.</span><span class="sxs-lookup"><span data-stu-id="25cd6-142">Conversely, if your application makes the same error when it is running with the retail version of the run time, behavior is undefined.</span></span> <span data-ttu-id="25cd6-143">Per motivi di prestazioni, il metodo non convalida i parametri, causando un comportamento imprevedibile e completamente situazionale quando non sono validi.</span><span class="sxs-lookup"><span data-stu-id="25cd6-143">For performance reasons, the method does not validate the parameters, resulting in unpredictable and completely situational behavior when they are not valid.</span></span> <span data-ttu-id="25cd6-144">In alcuni casi la chiamata potrebbe funzionare e in altri casi potrebbe causare un errore di memoria in Direct3D.</span><span class="sxs-lookup"><span data-stu-id="25cd6-144">In some cases the call might work, and in other cases it might cause a memory fault in Direct3D.</span></span> <span data-ttu-id="25cd6-145">Se una chiamata non valida funziona costantemente con una particolare configurazione hardware e una versione di DirectX, non c'è alcuna garanzia che continuerà a funzionare su altro hardware o con versioni successive di DirectX.</span><span class="sxs-lookup"><span data-stu-id="25cd6-145">If an invalid call consistently works with a particular hardware configuration and DirectX version, there is no guarantee that it will continue to function on other hardware or with later releases of DirectX.</span></span>

<span data-ttu-id="25cd6-146">Se l'applicazione rileva errori inspiegabili durante l'esecuzione con il file di runtime Direct3D per la vendita al dettaglio, testare la versione di debug e osservare attentamente i casi in cui l'applicazione passa parametri non validi.</span><span class="sxs-lookup"><span data-stu-id="25cd6-146">If your application encounters unexplained failures when running with the retail Direct3D run-time file, test against the debug version and look closely for cases where your application passes invalid parameters.</span></span> <span data-ttu-id="25cd6-147">Usare l'applet del pannello di controllo DirectX, passare al runtime di debug, se necessario, e selezionare l'opzione "Interrompi in D3DError".</span><span class="sxs-lookup"><span data-stu-id="25cd6-147">Use the DirectX control panel applet, switch to the debug runtime if necessary, and check the "Break on D3DError" option.</span></span> <span data-ttu-id="25cd6-148">Questa opzione impone al runtime di usare il metodo DebugBreak di Windows per forzare l'arresto dell'applicazione quando viene rilevato un bug dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="25cd6-148">This option will force the runtime to use the Windows DebugBreak method in order to force the application to stop when an application bug is detected.</span></span>

## <a name="related-topics"></a><span data-ttu-id="25cd6-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="25cd6-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25cd6-150">Suggerimenti per la programmazione</span><span class="sxs-lookup"><span data-stu-id="25cd6-150">Programming Tips</span></span>](programming-tips.md)
</dt> </dl>

 

 
