---
description: Implementazione di IWICBitmapCodecProgressNotification (decodificatore)
ms.assetid: 686b0875-c7ec-45ee-bd3e-94bfd9e5dcda
title: Implementazione di IWICBitmapCodecProgressNotification (decodificatore)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f92f05f02e77886d96d794be3f974c1eb0eed9dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312970"
---
# <a name="implementing-iwicbitmapcodecprogressnotification-decoder"></a><span data-ttu-id="82c29-103">Implementazione di IWICBitmapCodecProgressNotification (decodificatore)</span><span class="sxs-lookup"><span data-stu-id="82c29-103">Implementing IWICBitmapCodecProgressNotification (Decoder)</span></span>

## <a name="iwicbitmapcodecprogressnotification"></a><span data-ttu-id="82c29-104">IWICBitmapCodecProgressNotification</span><span class="sxs-lookup"><span data-stu-id="82c29-104">IWICBitmapCodecProgressNotification</span></span>

<span data-ttu-id="82c29-105">Quando un codec sta eseguendo un'operazione di I/O, ad esempio [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) su un'immagine di grandi dimensioni, il completamento potrebbe richiedere alcuni secondi o persino minuti.</span><span class="sxs-lookup"><span data-stu-id="82c29-105">When a codec is performing an I/O operation such as [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) on a large image, it may take several seconds or even minutes to complete.</span></span> <span data-ttu-id="82c29-106">Quando gli utenti finali non sono in grado di interrompere un'operazione a esecuzione prolungata, potrebbero ritenere che l'applicazione sia bloccata.</span><span class="sxs-lookup"><span data-stu-id="82c29-106">When end users are unable to interrupt a long-running operation, they may think the application has hung.</span></span> <span data-ttu-id="82c29-107">Spesso gli utenti chiudono un'applicazione o addirittura riavviano i computer, nel tentativo di riottenere il controllo del computer quando un'applicazione non risponde.</span><span class="sxs-lookup"><span data-stu-id="82c29-107">Users will often close an application, or even restart their computers, in an attempt to regain control of their computer when an application becomes unresponsive.</span></span>

<span data-ttu-id="82c29-108">Questa interfaccia consente a un'applicazione di specificare una funzione di callback che il codec può chiamare a intervalli specificati per notificare al chiamante lo stato di avanzamento dell'operazione corrente.</span><span class="sxs-lookup"><span data-stu-id="82c29-108">This interface enables an application to specify a callback function that the codec can call at specified intervals to notify the caller of the progress of the current operation.</span></span> <span data-ttu-id="82c29-109">L'applicazione può utilizzare questa funzione di callback per visualizzare un'indicazione dello stato di avanzamento nell'interfaccia utente per notificare all'utente lo stato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="82c29-109">The application can use this callback function to display an indication of progress in the user interface to notify the user of the status of the operation.</span></span> <span data-ttu-id="82c29-110">Se un utente fa clic sul pulsante **Annulla** nella finestra di dialogo **stato** , l'applicazione restituisce **WINCODEC \_ Err \_ interrotto** dalla funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="82c29-110">If a user clicks the **Cancel** button on the **Progress** dialog box, the application returns **WINCODEC\_ERR\_ABORTED** from the callback function.</span></span> <span data-ttu-id="82c29-111">Quando si verifica questo problema, il codec deve annullare l'operazione specificata e propagare questo **HRESULT** al chiamante del metodo che stava eseguendo l'operazione.</span><span class="sxs-lookup"><span data-stu-id="82c29-111">When this happens, the codec must cancel the specified operation and propagate this **HRESULT** back to the caller of the method that was performing the operation.</span></span>

<span data-ttu-id="82c29-112">Questa interfaccia deve essere implementata nella classe decodificatore a livello di contenitore.</span><span class="sxs-lookup"><span data-stu-id="82c29-112">This interface should be implemented on your container-level decoder class.</span></span>


```C++
interface IWICBitmapCodecProgressNotification : public IUnknown
{
    HRESULT RegisterProgressNotification ( 
        PFNProgressNotification pfnProgressNotification,
        LPVOID pvData,
        DWORD dwProgressFlags );
}
```



-   [<span data-ttu-id="82c29-113">RegisterProgressNotification</span><span class="sxs-lookup"><span data-stu-id="82c29-113">RegisterProgressNotification</span></span>](#registerprogressnotification)
-   [<span data-ttu-id="82c29-114">PFNProgressNotification</span><span class="sxs-lookup"><span data-stu-id="82c29-114">PFNProgressNotification</span></span>](#pfnprogressnotification)

### <a name="registerprogressnotification"></a><span data-ttu-id="82c29-115">RegisterProgressNotification</span><span class="sxs-lookup"><span data-stu-id="82c29-115">RegisterProgressNotification</span></span>

<span data-ttu-id="82c29-116">[**RegisterProgressNotification**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification) viene richiamato da un'applicazione per registrare una funzione di callback che il codec può chiamare a intervalli specificati.</span><span class="sxs-lookup"><span data-stu-id="82c29-116">[**RegisterProgressNotification**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification) is invoked by an application to register a callback function that the codec can call at specified intervals.</span></span> <span data-ttu-id="82c29-117">Il primo parametro, *pfnProgressNotification*, è un puntatore alla funzione di callback che il codec deve chiamare a intervalli regolari.</span><span class="sxs-lookup"><span data-stu-id="82c29-117">The first parameter, *pfnProgressNotification*, is a pointer to the callback function that the codec should call at regular intervals.</span></span>

<span data-ttu-id="82c29-118">Il parametro *pvData* punta a un oggetto che il chiamante desidera che il codec passi di nuovo alla funzione di callback ogni volta che viene richiamata la funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="82c29-118">The *pvData* parameter points to some object that the caller wants the codec to pass back to the callback function whenever the callback function is invoked.</span></span> <span data-ttu-id="82c29-119">Questo oggetto può essere qualsiasi elemento e non ha un significato particolare per il codec.</span><span class="sxs-lookup"><span data-stu-id="82c29-119">This object may be anything at all and has no particular significance to the codec.</span></span>

<span data-ttu-id="82c29-120">Il parametro *dwProgressFlags* specifica quando il codec deve chiamare la funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="82c29-120">The *dwProgressFlags* parameter specifies when the codec should call the callback function.</span></span> <span data-ttu-id="82c29-121">Una funzione OR può essere eseguita con due enumerazioni per questo parametro.</span><span class="sxs-lookup"><span data-stu-id="82c29-121">An OR function can be performed with two enumerations for this parameter.</span></span> <span data-ttu-id="82c29-122">L'enumerazione [**WICProgressOperation**](/windows/desktop/api/Wincodec/ne-wincodec-wicprogressoperation) specifica se chiamare la funzione di callback durante la decodifica (**WICProgressOperationCopyPixels**), la codifica (**WICProgerssOperationWritePixels**) o entrambe (**WICProgressOperationAll**).</span><span class="sxs-lookup"><span data-stu-id="82c29-122">The [**WICProgressOperation**](/windows/desktop/api/Wincodec/ne-wincodec-wicprogressoperation) enum specifies whether to call the callback function during decoding (**WICProgressOperationCopyPixels**), encoding (**WICProgerssOperationWritePixels**), or both (**WICProgressOperationAll**).</span></span>


```C++
enum WICProgressOperation
{
   WICProgressOperationCopyPixels,
   WICProgerssOperationWritePixels,
   WICProgressOperationAll      
};
```



<span data-ttu-id="82c29-123">Il codec deve chiamare la funzione di callback a intervalli regolari durante l'operazione, ma il chiamante può specificare determinati requisiti.</span><span class="sxs-lookup"><span data-stu-id="82c29-123">The codec should call the callback function at regular intervals throughout the operation, but the caller may specify certain requirements.</span></span> <span data-ttu-id="82c29-124">L'enumerazione [**WICProgressNotification**](/windows/desktop/api/Wincodec/ne-wincodec-wicprogressnotification) indica in quale punto dell'operazione chiamare la funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="82c29-124">The [**WICProgressNotification**](/windows/desktop/api/Wincodec/ne-wincodec-wicprogressnotification) enum indicates at which point in the operation to call the callback function.</span></span> <span data-ttu-id="82c29-125">Se il chiamante specifica **WICProgressNotificationBegin**, è necessario chiamarlo all'inizio dell'operazione (0,0).</span><span class="sxs-lookup"><span data-stu-id="82c29-125">If the caller specifies **WICProgressNotificationBegin**, you must call it at the beginning of the operation (0.0).</span></span> <span data-ttu-id="82c29-126">Se il chiamante non specifica questo, è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="82c29-126">If the caller does not specify this, it is optional.</span></span> <span data-ttu-id="82c29-127">Analogamente, se il chiamante specifica **WICProgerssNotificationEnd**, è necessario chiamarlo al termine dell'operazione (1,0).</span><span class="sxs-lookup"><span data-stu-id="82c29-127">Likewise, if the caller specifies **WICProgerssNotificationEnd**, you must call it when the operation is completed (1.0).</span></span> <span data-ttu-id="82c29-128">Se il chiamante specifica **WICProgressNotificationAll**, è necessario chiamarlo all'inizio e alla fine, così come a intervalli regolari durante l'operazione.</span><span class="sxs-lookup"><span data-stu-id="82c29-128">If the caller specifies **WICProgressNotificationAll**, you must call it at the beginning and end, as well as at regular intervals throughout the operation.</span></span> <span data-ttu-id="82c29-129">Il chiamante può inoltre specificare **WICProgerssNotificationFrequent**, che indica che si desidera richiamarli a intervalli frequenti, ad esempio dopo ogni paio di righe di analisi.</span><span class="sxs-lookup"><span data-stu-id="82c29-129">The caller may also specify **WICProgerssNotificationFrequent**, which indicates that they want to be called back at frequent intervals, perhaps after every couple of scan lines.</span></span> <span data-ttu-id="82c29-130">Un chiamante utilizzerà in genere questo flag solo per un'immagine di grandi dimensioni. In caso contrario, è in genere necessario richiamare a intervalli di circa il 10% di incrementi del numero totale di righe di analisi da elaborare.</span><span class="sxs-lookup"><span data-stu-id="82c29-130">(A caller will usually use this flag only for a very large image.) Otherwise, you should usually call back at intervals of approximately 10 percent increments of the total number of scan lines to be processed.</span></span>


```C++
enum WICProgressNotification
{
   WICProgressNotificationBegin,
   WICProgerssNotificationEnd,
   WICProgerssNotificationFrequent,
   WICProgressNotificationAll
};
```



<span data-ttu-id="82c29-131">È possibile registrare una sola funzione di callback alla volta per un'istanza specifica del codificatore o del codificatore.</span><span class="sxs-lookup"><span data-stu-id="82c29-131">Only one callback function at a time can be registered for a specific decoder or encoder instance.</span></span> <span data-ttu-id="82c29-132">Se un'applicazione chiama [**RegisterProgressNotification**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification) più di una volta, sostituire la funzione di callback precedentemente registrata con quella nuova.</span><span class="sxs-lookup"><span data-stu-id="82c29-132">If an application calls [**RegisterProgressNotification**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecprogressnotification-registerprogressnotification) more than once, replace the previously registered callback function with the new one.</span></span> <span data-ttu-id="82c29-133">Per annullare una registrazione di callback, un chiamante imposterà il parametro *pfnProgressNotification* su **null**.</span><span class="sxs-lookup"><span data-stu-id="82c29-133">To cancel a callback registration, a caller will set the *pfnProgressNotification* parameter to **NULL**.</span></span>

### <a name="pfnprogressnotification"></a><span data-ttu-id="82c29-134">PFNProgressNotification</span><span class="sxs-lookup"><span data-stu-id="82c29-134">PFNProgressNotification</span></span>

<span data-ttu-id="82c29-135">[**PFNProgressNotification**](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification) è la funzione di callback con la firma seguente.</span><span class="sxs-lookup"><span data-stu-id="82c29-135">[**PFNProgressNotification**](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification) is the callback function with the following signature.</span></span>


```C++
typedef HRESULT (*PFNProgressNotification) ( 
   LPVOID pvData,
   ULONG uFrameNum,
   WICProgressOperation operation,
   double dblProgress );
```



<span data-ttu-id="82c29-136">Quando si richiama la funzione di callback, usare il parametro *pvData* per passare di nuovo lo stesso *pvData* specificato dall'applicazione al momento della registrazione della funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="82c29-136">When you invoke the callback function, use the *pvData* parameter to pass back the same *pvData* that the application specified when it registered the callback function.</span></span>

<span data-ttu-id="82c29-137">Il parametro *uFrameNum* deve indicare l'indice del frame in fase di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="82c29-137">The *uFrameNum* parameter should indicate the index of the frame that is being processed.</span></span>

<span data-ttu-id="82c29-138">Impostare il parametro Operation su **WICProgressOperationCopyPixels** durante la decodifica e **WICProgressOperationWritePixels** durante la codifica.</span><span class="sxs-lookup"><span data-stu-id="82c29-138">Set the operation parameter to **WICProgressOperationCopyPixels** when decoding and **WICProgressOperationWritePixels** when encoding.</span></span>

<span data-ttu-id="82c29-139">Il parametro *dblProgress* deve essere un numero compreso tra 0,0 (inizio dell'operazione) e 1,0 (il completamento dell'operazione).</span><span class="sxs-lookup"><span data-stu-id="82c29-139">The *dblProgress* parameter should be a number between 0.0 (the beginning of the operation) and 1.0 (the completion of the operation).</span></span> <span data-ttu-id="82c29-140">Il valore deve riflettere la proporzione di righe di analisi già elaborate rispetto al numero totale di righe di analisi da elaborare.</span><span class="sxs-lookup"><span data-stu-id="82c29-140">The value should reflect the proportion of scan lines already processed relative to the total number of scan lines to be processed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="82c29-141">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="82c29-141">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="82c29-142">**Riferimento**</span><span class="sxs-lookup"><span data-stu-id="82c29-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="82c29-143">**ProgressNotificationCallback**</span><span class="sxs-lookup"><span data-stu-id="82c29-143">**ProgressNotificationCallback**</span></span>](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification)
</dt> <dt>

[<span data-ttu-id="82c29-144">**IWICBitmapCodecProgressNotification**</span><span class="sxs-lookup"><span data-stu-id="82c29-144">**IWICBitmapCodecProgressNotification**</span></span>](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecprogressnotification)
</dt> <dt>

<span data-ttu-id="82c29-145">**Informazioni concettuali**</span><span class="sxs-lookup"><span data-stu-id="82c29-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="82c29-146">Implementazione di IWICBitmapDecoder</span><span class="sxs-lookup"><span data-stu-id="82c29-146">Implementing IWICBitmapDecoder</span></span>](-wic-imp-iwicbitmapdecoder.md)
</dt> <dt>

[<span data-ttu-id="82c29-147">Implementazione di IWICBitmapSource</span><span class="sxs-lookup"><span data-stu-id="82c29-147">Implementing IWICBitmapSource</span></span>](-wic-imp-iwicbitmapsource.md)
</dt> <dt>

[<span data-ttu-id="82c29-148">Come scrivere un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="82c29-148">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="82c29-149">Panoramica del componente imaging Windows</span><span class="sxs-lookup"><span data-stu-id="82c29-149">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



