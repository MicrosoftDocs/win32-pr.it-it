---
description: Sincronizzazione dei comandi DVD
ms.assetid: 37e8f940-617d-43f6-92bd-aadccafe0059
title: Sincronizzazione dei comandi DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4d677c38363a0ab80f90f58498eeef24bdc29eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318352"
---
# <a name="synchronizing-dvd-commands"></a><span data-ttu-id="b190e-103">Sincronizzazione dei comandi DVD</span><span class="sxs-lookup"><span data-stu-id="b190e-103">Synchronizing DVD Commands</span></span>

<span data-ttu-id="b190e-104">I comandi DVD non vengono sempre completati immediatamente.</span><span class="sxs-lookup"><span data-stu-id="b190e-104">DVD commands do not always complete instantly.</span></span> <span data-ttu-id="b190e-105">Per questo motivo, alcuni dei metodi in [**IDVDControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) sono asincroni.</span><span class="sxs-lookup"><span data-stu-id="b190e-105">For this reason, some of the methods in [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) are asynchronous.</span></span> <span data-ttu-id="b190e-106">Sono inclusi i metodi di riproduzione, ad esempio **PlayTitle**, e i metodi di navigazione dei menu, ad esempio **ShowMenu** e **ReturnFromSubmenu**.</span><span class="sxs-lookup"><span data-stu-id="b190e-106">These include playback methods, such as **PlayTitle**, and menu navigation methods, such as **ShowMenu** and **ReturnFromSubmenu**.</span></span> <span data-ttu-id="b190e-107">Un metodo asincrono restituisce immediatamente un risultato, senza attendere il completamento del comando.</span><span class="sxs-lookup"><span data-stu-id="b190e-107">An asynchronous method returns immediately, without waiting for the command to complete.</span></span> <span data-ttu-id="b190e-108">Dopo la restituzione del metodo, altri eventi possono impedire il completamento del comando, anche se il metodo ha avuto esito positivo.</span><span class="sxs-lookup"><span data-stu-id="b190e-108">After the method returns, other events may prevent the command from completing, even if the method succeeded.</span></span> <span data-ttu-id="b190e-109">DirectShow offre diverse opzioni per la sincronizzazione dei comandi, che vanno da nessuna sincronizzazione alla sincronizzazione completa usando gli eventi del grafo del filtro.</span><span class="sxs-lookup"><span data-stu-id="b190e-109">DirectShow provides several options for synchronizing commands, ranging from no synchronization to full synchronization using filter graph events.</span></span>

<span data-ttu-id="b190e-110">Tutti i metodi asincroni hanno un parametro *dwFlags* e un parametro *ppCmd* .</span><span class="sxs-lookup"><span data-stu-id="b190e-110">All of the asynchronous methods have a *dwFlags* parameter and a *ppCmd* parameter.</span></span> <span data-ttu-id="b190e-111">Il parametro *dwFlags* specifica il comportamento di sincronizzazione e il parametro *ppCmd* restituisce un puntatore a un oggetto di sincronizzazione facoltativo.</span><span class="sxs-lookup"><span data-stu-id="b190e-111">The *dwFlags* parameter specifies the synchronization behavior, and the *ppCmd* parameter returns a pointer to an optional synchronization object.</span></span> <span data-ttu-id="b190e-112">Comportamenti diversi variano a seconda dei valori specificati per questi parametri.</span><span class="sxs-lookup"><span data-stu-id="b190e-112">Different behaviors result depending on what values you give for these parameters.</span></span>

<span data-ttu-id="b190e-113">**Nessuna sincronizzazione**</span><span class="sxs-lookup"><span data-stu-id="b190e-113">**No Synchronization**</span></span>

<span data-ttu-id="b190e-114">Per un'applicazione di riproduzione DVD di base, l'opzione migliore potrebbe essere semplicemente ignorare i problemi di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="b190e-114">For a basic DVD playback application, the best option may be simply to ignore synchronization issues.</span></span> <span data-ttu-id="b190e-115">Occasionalmente, un comando può avere esito negativo o l'interfaccia utente potrebbe essere leggermente in ritardo durante l'aggiornamento, ma questi errori saranno in ordine di frazioni di secondi.</span><span class="sxs-lookup"><span data-stu-id="b190e-115">Occasionally a command may fail or the UI might lag slightly when it updates, but these errors will be on the order of fractions of seconds.</span></span>

<span data-ttu-id="b190e-116">Per eseguire un comando senza sincronizzazione, impostare il flag del flag di comando DVD \_ \_ \_ None nel parametro *dwFlags* e impostare il parametro *ppCmd* su **null**:</span><span class="sxs-lookup"><span data-stu-id="b190e-116">To issue a command with no synchronization, set the DVD\_CMD\_FLAG\_None flag in the *dwFlags* parameter and set the *ppCmd* parameter to **NULL**:</span></span>


```C++
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_None, NULL);
```



<span data-ttu-id="b190e-117">**Processi bloccati**</span><span class="sxs-lookup"><span data-stu-id="b190e-117">**Blocking**</span></span>

<span data-ttu-id="b190e-118">Se si imposta il \_ \_ flag di blocco del flag CMD del DVD EC \_ \_ nel parametro *dwFlags* , il metodo si blocca fino al completamento del comando:</span><span class="sxs-lookup"><span data-stu-id="b190e-118">If you set the EC\_DVD\_CMD\_FLAG\_Block flag in the *dwFlags* parameter, the method blocks until the command completes:</span></span>


```C++
hr = pDVDControl2->PlayTitle(uTitle, EC_DVD_CMD_FLAG_Block, NULL);
```



<span data-ttu-id="b190e-119">In effetti, questo flag converte un metodo asincrono in un metodo sincrono.</span><span class="sxs-lookup"><span data-stu-id="b190e-119">In effect, this flag turns an asynchronous method into a synchronous method.</span></span> <span data-ttu-id="b190e-120">Lo svantaggio è che l'interfaccia utente si blocca se si chiama il metodo dal thread dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b190e-120">The drawback is that your UI blocks if you call the method from the application thread.</span></span>

<span data-ttu-id="b190e-121">**Oggetto di sincronizzazione**</span><span class="sxs-lookup"><span data-stu-id="b190e-121">**Synchronization Object**</span></span>

<span data-ttu-id="b190e-122">Tutti i metodi asincroni possono restituire un oggetto di sincronizzazione, che può essere usato per attendere l'avvio o la fine del comando.</span><span class="sxs-lookup"><span data-stu-id="b190e-122">All of the asynchronous methods can return a synchronization object, which you can use to wait for the command to start or end.</span></span> <span data-ttu-id="b190e-123">Per ottenere questo oggetto, passare l'indirizzo di un puntatore [**IDvdCmd**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) nel parametro *ppCmd* :</span><span class="sxs-lookup"><span data-stu-id="b190e-123">To get this object, pass the address of an [**IDvdCmd**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) pointer in the *ppCmd* parameter:</span></span>


```C++
IDvdCmd *pCmdObj = NULL;
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_None, &pCmdObj);
```



<span data-ttu-id="b190e-124">Se il metodo ha esito positivo, restituisce un nuovo oggetto **IDvdCmd** .</span><span class="sxs-lookup"><span data-stu-id="b190e-124">If the method succeeds, it returns a new **IDvdCmd** object.</span></span> <span data-ttu-id="b190e-125">Il metodo [**IDvdCmd:: WaitForStart**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforstart) si blocca fino all'inizio del comando e il metodo [**IDvdCmd:: WaitForEnd**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforend) si blocca fino alla fine del comando.</span><span class="sxs-lookup"><span data-stu-id="b190e-125">The [**IDvdCmd::WaitForStart**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforstart) method blocks until the command begins, and the [**IDvdCmd::WaitForEnd**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforend) method blocks until the command ends.</span></span> <span data-ttu-id="b190e-126">Il valore restituito indica lo stato del comando.</span><span class="sxs-lookup"><span data-stu-id="b190e-126">The return value indicates the status of the command.</span></span>

<span data-ttu-id="b190e-127">Dal punto di vista funzionale, il codice seguente equivale all'impostazione del \_ flag di blocco del flag CMD del DVD EC \_ \_ \_ , illustrato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="b190e-127">The following code is functionally equivalent to setting the EC\_DVD\_CMD\_FLAG\_Block flag, shown previously.</span></span>


```C++
IDvdCmd *pCmdObj = NULL;
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_None, &pCmdObj);
if (SUCCEEDED(hr))
{
    // Use pCmdObj to wait for the command to complete.
    hr = pCmdObj->WaitToEnd();
    pCmdObj->Release();
}
```



<span data-ttu-id="b190e-128">In questo caso, il metodo **PlayTitle** non viene bloccato, ma l'applicazione viene bloccata chiamando **WaitForEnd**.</span><span class="sxs-lookup"><span data-stu-id="b190e-128">In this case, the **PlayTitle** method does not block, but the application blocks by calling **WaitForEnd**.</span></span>

<span data-ttu-id="b190e-129">**Eventi dello stato del comando**</span><span class="sxs-lookup"><span data-stu-id="b190e-129">**Command Status Events**</span></span>

<span data-ttu-id="b190e-130">Se si imposta il flag SendEvents del DVD del \_ \_ flag CMD \_ nel parametro *dwFlags* , il navigatore DVD invia un evento di [**\_ \_ \_ avvio cmd del DVD EC**](ec-dvd-cmd-start.md) quando il comando inizia e un evento di [**\_ \_ \_ fine del cmd DVD EC**](ec-dvd-cmd-end.md) quando il comando termina.</span><span class="sxs-lookup"><span data-stu-id="b190e-130">If you set the DVD\_CMD\_FLAG\_SendEvents flag in the *dwFlags* parameter, the DVD Navigator sends an [**EC\_DVD\_CMD\_START**](ec-dvd-cmd-start.md) event when the command begins and an [**EC\_DVD\_CMD\_END**](ec-dvd-cmd-end.md) event when the command ends.</span></span>

<span data-ttu-id="b190e-131">Il parametro *lParam2* dell'evento è il valore restituito HRESULT per il comando.</span><span class="sxs-lookup"><span data-stu-id="b190e-131">The event's *lParam2* parameter is the HRESULT return value for the command.</span></span> <span data-ttu-id="b190e-132">Il parametro *lParam1* dell'evento fornisce un modo per ottenere l'oggetto di sincronizzazione per il comando.</span><span class="sxs-lookup"><span data-stu-id="b190e-132">The event's *lParam1* parameter provides a way get the synchronization object for the command.</span></span> <span data-ttu-id="b190e-133">Se si passa *lParam1* al metodo [**IDvdInfo2:: GetCmdFromEvent**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) , il metodo restituisce un puntatore all'interfaccia **IDvdCmd** dell'oggetto di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="b190e-133">If you pass *lParam1* to the [**IDvdInfo2::GetCmdFromEvent**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) method, the method returns a pointer to the synchronization object's **IDvdCmd** interface.</span></span> <span data-ttu-id="b190e-134">È possibile usare questa interfaccia per attendere il completamento del comando, come descritto in precedenza.</span><span class="sxs-lookup"><span data-stu-id="b190e-134">You can use this interface to wait for completion of the command, as described earlier.</span></span> <span data-ttu-id="b190e-135">Tuttavia, se è stato passato **null** per il parametro *PpCmd* nel metodo **IDVDControl2** originale, il navigatore DVD non creerà un oggetto di sincronizzazione e **GetCmdFromEvent** restituirà e \_ avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="b190e-135">However, if you passed **NULL** for the *ppCmd* parameter in the original **IDvdControl2** method, the DVD Navigator does not create a synchronization object, and **GetCmdFromEvent** returns E\_FAIL.</span></span>

<span data-ttu-id="b190e-136">Nel codice seguente viene illustrato come utilizzare gli eventi di stato del comando senza alcun oggetto di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="b190e-136">The following code shows how to use command status events with no synchronization object.</span></span>


```C++
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_SendEvents, NULL);

// In your event handling code:
switch (lEvent)
{
   case EC_DVD_CMD_END:
       HRESULT hr2 = (HRESULT)lParam2;
       /* ... */ 
       break;
}
```



<span data-ttu-id="b190e-137">Si noti che senza un oggetto di sincronizzazione, non è possibile stabilire quale comando è associato all'evento.</span><span class="sxs-lookup"><span data-stu-id="b190e-137">Note that without a synchronization object, you cannot tell which command is associated with the event.</span></span> <span data-ttu-id="b190e-138">Nel codice seguente viene illustrato come utilizzare gli eventi con l'oggetto di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="b190e-138">The following code shows how to use events with the synchronization object.</span></span> <span data-ttu-id="b190e-139">L'idea è archiviare gli oggetti di sincronizzazione in un elenco e quindi confrontare i puntatori a oggetti quando si ottiene l'evento di [**\_ \_ \_ inizio**](ec-dvd-cmd-start.md) del cmd di DVD EC o del [**\_ \_ cmd \_**](ec-dvd-cmd-end.md) .</span><span class="sxs-lookup"><span data-stu-id="b190e-139">The idea is to store the synchronization objects in a list and then compare object pointers when you get the [**EC\_DVD\_CMD\_START**](ec-dvd-cmd-start.md) or [**EC\_DVD\_CMD\_END**](ec-dvd-cmd-end.md) event.</span></span>


```C++
IDvdCmd *pCmdObj = NULL;
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_SendEvents, &pCmdObj);
if (SUCCEEDED(hr)) 
{
    // Store pCmdObj in a list of pending commands.
}

// In your event handling code:
switch (lEvent)
{
case EC_DVD_CMD_END:
   {
       IDvdCmd *pObj = NULL;
       hr = pDvdInfo2->GetCmdFromEvent(lParam, &pObj);
       if (SUCCEEDED(hr)) 
       {
           // Find this object in your list by comparing IUnknown
           // pointers. Assume the following function is defined in 
           // your application:
           IDvdCmd *pPendingObj = GetPendingCommandFromList(pObj); 
           if (pPendingObj)
           {
               // Update UI accordingly (not shown). 
               pPendingObj->Release();
           }
           pObj->Release();
       }
    }
    break;
} 
```



<span data-ttu-id="b190e-140">**Scaricamento dei buffer di DVD Navigator**</span><span class="sxs-lookup"><span data-stu-id="b190e-140">**Flushing the DVD Navigator's Buffers**</span></span>

<span data-ttu-id="b190e-141">Durante la riproduzione, il navigatore DVD memorizza nel buffer i dati video.</span><span class="sxs-lookup"><span data-stu-id="b190e-141">During playback, the DVD Navigator buffers video data.</span></span> <span data-ttu-id="b190e-142">La quantità di dati memorizzati nel buffer varia.</span><span class="sxs-lookup"><span data-stu-id="b190e-142">The amount of buffered data varies.</span></span> <span data-ttu-id="b190e-143">Quando lo strumento di spostamento DVD passa a una nuova parte di video, i dati già presenti nella pipeline non vengono persi, quindi la transizione è trasparente.</span><span class="sxs-lookup"><span data-stu-id="b190e-143">When the DVD Navigator switches to a new piece of video, data already in the pipeline is not lost, so the transition is seamless.</span></span> <span data-ttu-id="b190e-144">Per impostazione predefinita, quando il navigatore DVD emette un comando, non Scarica i dati già presenti nella pipeline.</span><span class="sxs-lookup"><span data-stu-id="b190e-144">By default, when the DVD Navigator issues a command, it does not flush data already in the pipeline.</span></span> <span data-ttu-id="b190e-145">Di conseguenza, potrebbe verificarsi una certa latenza prima che sia possibile visualizzare l'effetto del comando, a seconda della quantità di dati memorizzati nel buffer.</span><span class="sxs-lookup"><span data-stu-id="b190e-145">As a result, there may be some latency before you can see the effect of the command, depending on how much data is buffered.</span></span> <span data-ttu-id="b190e-146">Per aumentare la velocità di risposta, è possibile forzare lo scaricamento del navigatore DVD impostando il \_ \_ flag di scaricamento del flag di comando DVD \_ .</span><span class="sxs-lookup"><span data-stu-id="b190e-146">To increase the responsiveness, you can force the DVD Navigator to flush by setting the DVD\_CMD\_FLAG\_Flush flag.</span></span>


```C++
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_Flush, NULL);
```



<span data-ttu-id="b190e-147">Questo flag può essere combinato con uno qualsiasi dei flag descritti in precedenza, usando un operatore OR bit per bit.</span><span class="sxs-lookup"><span data-stu-id="b190e-147">This flag can be combined with any of the flags described previously, using a bitwise OR.</span></span> <span data-ttu-id="b190e-148">Un effetto collaterale dello scaricamento è che è possibile che alcuni video vadano persi, quindi non usare questo flag se è necessario garantire che non vi siano gap nel video.</span><span class="sxs-lookup"><span data-stu-id="b190e-148">A side effect of flushing is that some video may be lost, so do not use this flag if you need to guarantee there are no gaps in the video.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b190e-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b190e-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b190e-150">Applicazioni DVD</span><span class="sxs-lookup"><span data-stu-id="b190e-150">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



