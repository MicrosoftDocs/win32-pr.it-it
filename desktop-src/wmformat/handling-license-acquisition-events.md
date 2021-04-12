---
title: Gestione degli eventi di acquisizione delle licenze
description: Gestione degli eventi di acquisizione delle licenze
ms.assetid: e118bf09-1fa6-41b6-a6bb-3e8cb6097994
keywords:
- Windows Media Format SDK, gestione degli eventi di acquisizione delle licenze
- Windows Media Format SDK, eventi di acquisizione della licenza
- Formato di sistemi avanzati (ASF), gestione degli eventi di acquisizione delle licenze
- ASF (Advanced Systems Format), gestione degli eventi di acquisizione delle licenze
- ASF (Advanced Systems Format), eventi di acquisizione della licenza
- ASF (formato avanzato dei sistemi), eventi di acquisizione della licenza
- Digital Rights Management (DRM), gestione degli eventi di acquisizione delle licenze
- DRM (Digital Rights Management), gestione degli eventi di acquisizione delle licenze
- Digital Rights Management (DRM), eventi di acquisizione della licenza
- DRM (Digital Rights Management), eventi di acquisizione della licenza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5e31fd5b108f41d5b0925918fdf1c83764bcf7e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398588"
---
# <a name="handling-license-acquisition-events"></a><span data-ttu-id="a184b-113">Gestione degli eventi di acquisizione delle licenze</span><span class="sxs-lookup"><span data-stu-id="a184b-113">Handling License Acquisition Events</span></span>

<span data-ttu-id="a184b-114">Un'applicazione Reader abilitata per DRM, nel metodo [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback, gestisce i quattro eventi seguenti relativi al processo di acquisizione della licenza:</span><span class="sxs-lookup"><span data-stu-id="a184b-114">A DRM-enabled reader application, in its [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method, handles the following four events related to the license acquisition process:</span></span>

-   <span data-ttu-id="a184b-115">**\_stato della \_ firma \_ LICENSEURL di WMT**</span><span class="sxs-lookup"><span data-stu-id="a184b-115">**WMT\_LICENSEURL\_SIGNATURE\_STATE**</span></span>
-   <span data-ttu-id="a184b-116">**\_nessun \_ diritto di WMT**</span><span class="sxs-lookup"><span data-stu-id="a184b-116">**WMT\_NO\_RIGHTS**</span></span>
-   <span data-ttu-id="a184b-117">**WMT \_ No \_ Rights \_**</span><span class="sxs-lookup"><span data-stu-id="a184b-117">**WMT\_NO\_RIGHTS\_EX**</span></span>
-   <span data-ttu-id="a184b-118">**\_licenza di acquisizione WMT \_**</span><span class="sxs-lookup"><span data-stu-id="a184b-118">**WMT\_ACQUIRE\_LICENSE**</span></span>

<span data-ttu-id="a184b-119">**\_stato della \_ firma \_ LICENSEURL di WMT**</span><span class="sxs-lookup"><span data-stu-id="a184b-119">**WMT\_LICENSEURL\_SIGNATURE\_STATE**</span></span>

<span data-ttu-id="a184b-120">Quando il componente DRM rileva il contenuto protetto da DRM versione 7, cerca innanzitutto una licenza valida nel sistema locale.</span><span class="sxs-lookup"><span data-stu-id="a184b-120">When the DRM component detects content protected by DRM version 7, it first looks for a valid license on the local system.</span></span> <span data-ttu-id="a184b-121">Se non ne esiste alcuno, viene valutato l'URL di acquisizione della licenza nell'intestazione DRM del file e viene inviato un evento **\_ \_ \_ dello stato della firma WMT LICENSEURL** con *pValue* impostato su uno dei valori di [**\_ \_ attendibilità di WMT DRMLA**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_drmla_trust) , che indica se l'URL è attendibile, non attendibile o è stato manomesso.</span><span class="sxs-lookup"><span data-stu-id="a184b-121">If none exists, it then evaluates the license acquisition URL in the file's DRM header and sends a **WMT\_LICENSEURL\_SIGNATURE\_STATE** event with *pValue* set to one of the [**WMT\_DRMLA\_TRUST**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_drmla_trust) values, indicating whether the URL is trusted, untrusted, or has been tampered with.</span></span> <span data-ttu-id="a184b-122">Se l'URL non è attendibile, l'applicazione deve avvisare l'utente.</span><span class="sxs-lookup"><span data-stu-id="a184b-122">If the URL is not trusted, then the application should warn the user.</span></span> <span data-ttu-id="a184b-123">Se l'URL è stato manomesso, il file deve essere considerato danneggiato e l'applicazione non deve passare all'URL senza emettere un avviso sicuro per l'utente.</span><span class="sxs-lookup"><span data-stu-id="a184b-123">If the URL has been tampered with, then the file should be considered corrupted, and the application should not navigate to the URL without issuing a strong warning the user.</span></span>

<span data-ttu-id="a184b-124">**\_nessun \_ diritto di WMT**</span><span class="sxs-lookup"><span data-stu-id="a184b-124">**WMT\_NO\_RIGHTS**</span></span>

<span data-ttu-id="a184b-125">L'evento **WMT \_ No \_ Rights** viene inviato solo per il contenuto DRM versione 1, il che significa che la licenza deve essere acquisita in modo non invisibile.</span><span class="sxs-lookup"><span data-stu-id="a184b-125">The **WMT\_NO\_RIGHTS** event is sent only for DRM version 1 content, which means that the license must be acquired non-silently.</span></span> <span data-ttu-id="a184b-126">In altre parole, l'utente deve passare a una pagina Web per acquisire una licenza.</span><span class="sxs-lookup"><span data-stu-id="a184b-126">In other words, the user must navigate to a Web page to acquire a license.</span></span> <span data-ttu-id="a184b-127">L'URL della pagina viene recuperato come stringa a caratteri wide con terminazione null dal parametro *pValue* nel metodo **OnStatus** .</span><span class="sxs-lookup"><span data-stu-id="a184b-127">The URL for the page is retrieved as a wide-character null-terminated string from the *pValue* parameter in the **OnStatus** method.</span></span>

<span data-ttu-id="a184b-128">Se appropriato, un'applicazione può semplificare l'esplorazione della pagina Web da parte dell'utente, aprendo Internet Explorer in un processo separato oppure ospitando il controllo Web browser.</span><span class="sxs-lookup"><span data-stu-id="a184b-128">If appropriate, an application can make it easier for the user to navigate to the Web page, either by opening up Internet Explorer in a separate process or else by hosting the Web Browser control.</span></span> <span data-ttu-id="a184b-129">Questa operazione non è tuttavia necessaria.</span><span class="sxs-lookup"><span data-stu-id="a184b-129">This is not required, however.</span></span> <span data-ttu-id="a184b-130">Come minimo, un'applicazione può semplicemente visualizzare l'URL dell'utente in una finestra di messaggio e richiedere di incollarlo nella barra degli indirizzi di Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="a184b-130">At the very least, an application could simply display the URL to the user in a message box and prompt them to paste it into the address bar of Internet Explorer.</span></span> <span data-ttu-id="a184b-131">Nell'esempio AudioPlayer viene illustrata la gestione corretta dell'evento **WMT \_ No \_ Rights** , tra cui come formattare la stringa URL e come utilizzare il metodo **CreateProcess** per aprire Internet Explorer e passare all'URL specificato.</span><span class="sxs-lookup"><span data-stu-id="a184b-131">The Audioplayer sample demonstrates proper handling of the **WMT\_NO\_RIGHTS** event, including how to format the URL string, and how to use the **CreateProcess** method to open Internet Explorer and navigate to the specified URL.</span></span>

<span data-ttu-id="a184b-132">Poiché l'applicazione non è in grado di sapere quando è stata acquistata una licenza di DRM versione 1, spetta all'utente tentare di aprire nuovamente il file dopo l'acquisizione della licenza.</span><span class="sxs-lookup"><span data-stu-id="a184b-132">Because the application has no way of knowing when a DRM version 1 license has been acquired, it is up to the user to attempt to open the file again after acquiring the license.</span></span>

<span data-ttu-id="a184b-133">Questo stesso processo di acquisizione della licenza non invisibile all'utente può essere usato anche per le licenze della versione 7, ma in questo caso l'applicazione può chiamare prima [**IWMDRMReader:: MonitorLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition).</span><span class="sxs-lookup"><span data-stu-id="a184b-133">This same non-silent license acquisition process can also be used for version 7 licenses, but in this case the application can first call [**IWMDRMReader::MonitorLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition).</span></span> <span data-ttu-id="a184b-134">Questo metodo provocherà ripetutamente il controllo dell'archivio licenze locale fino a quando non viene trovata la licenza per il nuovo file.</span><span class="sxs-lookup"><span data-stu-id="a184b-134">This method will cause the local license store to be checked repeatedly until the license for the new file is found.</span></span> <span data-ttu-id="a184b-135">A questo punto, l'applicazione riceverà un evento **WMT \_ acquire \_ License** .</span><span class="sxs-lookup"><span data-stu-id="a184b-135">At that point, the application will receive a **WMT\_ACQUIRE\_LICENSE** event.</span></span> <span data-ttu-id="a184b-136">Per tutte le licenze della versione 7, è consigliabile che le applicazioni forniscano agli utenti la possibilità di ottenere le licenze in modo invisibile o non invisibile all'utente.</span><span class="sxs-lookup"><span data-stu-id="a184b-136">For all version 7 licenses, it is recommended that applications give users the option to obtain licenses silently or non-silently.</span></span>

<span data-ttu-id="a184b-137">**WMT \_ No \_ Rights \_**</span><span class="sxs-lookup"><span data-stu-id="a184b-137">**WMT\_NO\_RIGHTS\_EX**</span></span>

<span data-ttu-id="a184b-138">Il **WMT \_ No \_ Rights \_ ex** evento indica che il contenuto è protetto da DRM versione 7 e pertanto il processo di acquisizione della licenza può procedere in modo invisibile all'utente o non automatico.</span><span class="sxs-lookup"><span data-stu-id="a184b-138">The **WMT\_NO\_RIGHTS\_EX** event indicates that the content is protected by DRM version 7, and therefore the license acquisition process can proceed either silently or non-silently.</span></span> <span data-ttu-id="a184b-139">In generale, l'acquisizione di licenze Silent è più utile per gli utenti finali, anche se alcune persone preferiscono acquisire tutte le licenze in modo non invisibile.</span><span class="sxs-lookup"><span data-stu-id="a184b-139">In general, silent license acquisition is more convenient for end users, although some people prefer to acquire all licenses non-silently.</span></span> <span data-ttu-id="a184b-140">Quando l'acquisizione della licenza richiede che l'utente invii informazioni di pagamento o personali, il processo deve sempre essere eseguito in modo non invisibile.</span><span class="sxs-lookup"><span data-stu-id="a184b-140">When license acquisition requires the user to submit payment or personal information, the process should always be performed non-silently.</span></span> <span data-ttu-id="a184b-141">L'acquisizione della licenza non invisibile all'utente è descritta in precedenza sotto l'intestazione **WMT \_ No \_ Rights** .</span><span class="sxs-lookup"><span data-stu-id="a184b-141">Non-silent license acquisition is described above under the **WMT\_NO\_RIGHTS** heading.</span></span> <span data-ttu-id="a184b-142">L'acquisizione invisibile all'utente procede come segue:</span><span class="sxs-lookup"><span data-stu-id="a184b-142">Silent acquisition proceeds as follows:</span></span>

1.  <span data-ttu-id="a184b-143">Eseguire il cast del parametro *pValue* a una struttura di [**dati di \_ \_ licenza \_ WM Get**](wm-get-license-data.md) e archiviare la struttura nel caso in cui sia necessaria in un secondo momento per l'acquisizione della licenza non invisibile all'utente.</span><span class="sxs-lookup"><span data-stu-id="a184b-143">Cast the *pValue* parameter to a [**WM\_GET\_LICENSE\_DATA**](wm-get-license-data.md) structure and store the structure in case it is needed later for non-silent license acquisition.</span></span>
2.  <span data-ttu-id="a184b-144">Chiamare **QueryInterface** sull'oggetto Reader per ottenere l'interfaccia [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) .</span><span class="sxs-lookup"><span data-stu-id="a184b-144">Call **QueryInterface** on the reader object to obtain the [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) interface.</span></span>
3.  <span data-ttu-id="a184b-145">Chiamare [**IWMDRMReader:: AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) e specificare 0x1 nel parametro *dwFlags* per indicare l'acquisizione della lingua invisibile all'utente.</span><span class="sxs-lookup"><span data-stu-id="a184b-145">Call [**IWMDRMReader::AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) and specify 0x1 in the *dwFlags* parameter to indicate silent language acquisition.</span></span> <span data-ttu-id="a184b-146">Si tratta di una chiamata asincrona che restituisce immediatamente un risultato.</span><span class="sxs-lookup"><span data-stu-id="a184b-146">This is an asynchronous call that returns immediately.</span></span>
4.  <span data-ttu-id="a184b-147">Attendere l'evento **WMT \_ acquire \_ License** .</span><span class="sxs-lookup"><span data-stu-id="a184b-147">Wait for the **WMT\_ACQUIRE\_LICENSE** event.</span></span>

<span data-ttu-id="a184b-148">**\_licenza di acquisizione WMT \_**</span><span class="sxs-lookup"><span data-stu-id="a184b-148">**WMT\_ACQUIRE\_LICENSE**</span></span>

<span data-ttu-id="a184b-149">L'evento **WMT \_ acquisisce \_ License** viene inviato al termine del processo di acquisizione della licenza per una licenza DRM versione 7.</span><span class="sxs-lookup"><span data-stu-id="a184b-149">The **WMT\_ACQUIRE\_LICENSE** event is sent after the license acquisition process is completed for a DRM version 7 license.</span></span> <span data-ttu-id="a184b-150">[**IWMDRMReader:: AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) fa sì che questo evento venga inviato per l'acquisizione invisibile all'utente e [**MonitorLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition) ne causa l'invio per l'acquisizione non invisibile all'utente.</span><span class="sxs-lookup"><span data-stu-id="a184b-150">[**IWMDRMReader::AcquireLicense**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-acquirelicense) causes this event to be sent for silent acquisition, and [**MonitorLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-monitorlicenseacquisition) causes it to be sent for non-silent acquisition.</span></span> <span data-ttu-id="a184b-151">Nel gestore eventi, eseguire il cast di *pValue* a un puntatore a una struttura di [**dati di \_ \_ licenza \_ WM Get**](wm-get-license-data.md) ed esaminare il membro **HR** per determinare se la licenza è stata acquisita correttamente.</span><span class="sxs-lookup"><span data-stu-id="a184b-151">In your event handler, cast *pValue* to a pointer to a [**WM\_GET\_LICENSE\_DATA**](wm-get-license-data.md) structure and examine the **hr** member to determine whether the license was successfully acquired.</span></span> <span data-ttu-id="a184b-152">Se **HR** è uguale a NS \_ E \_ DRM \_ No \_ Rights, indica che la licenza deve essere acquisita in modo non invisibile.</span><span class="sxs-lookup"><span data-stu-id="a184b-152">If **hr** equals NS\_E\_DRM\_NO\_RIGHTS, it indicates that the license must be acquired non-silently.</span></span> <span data-ttu-id="a184b-153">Le applicazioni devono consentire agli utenti di annullare il processo di acquisizione delle licenze in qualsiasi momento.</span><span class="sxs-lookup"><span data-stu-id="a184b-153">Applications should enable users to cancel the license acquisition process at any time.</span></span> <span data-ttu-id="a184b-154">Questa operazione viene eseguita chiamando [**IWMDRMReader:: CancelLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancellicenseacquisition).</span><span class="sxs-lookup"><span data-stu-id="a184b-154">This is done by calling [**IWMDRMReader::CancelLicenseAcquisition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-cancellicenseacquisition).</span></span> <span data-ttu-id="a184b-155">La chiamata a questo metodo invierà un evento **WMT \_ acquire \_ License** con un valore **HRESULT** di NS \_ S \_ DRM \_ acquire \_ annullato.</span><span class="sxs-lookup"><span data-stu-id="a184b-155">Calling this method will send a **WMT\_ACQUIRE\_LICENSE** event with an **HRESULT** value of NS\_S\_DRM\_ACQUIRE\_CANCELLED.</span></span>

<span data-ttu-id="a184b-156">Se **HR** corrisponde alla \_ licenza DRM di NS S \_ \_ \_ acquistata, la licenza è stata acquisita e l'applicazione può provare a riprodurre il file oppure copiarla in un dispositivo o eseguire qualsiasi azione per cui aveva richiesto diritti.</span><span class="sxs-lookup"><span data-stu-id="a184b-156">If **hr** equals NS\_S\_DRM\_LICENSE\_ACQUIRED, then the license has been acquired and the application can attempt to play the file, or copy it to a device or perform whatever action it had requested rights for.</span></span>

<span data-ttu-id="a184b-157">In Windows XP è stato introdotto un nuovo codice di errore: NS \_ E \_ DRM \_ License \_ NOTACQUIRED.</span><span class="sxs-lookup"><span data-stu-id="a184b-157">On Windows XP, a new error code was introduced: NS\_E\_DRM\_LICENSE\_NOTACQUIRED.</span></span> <span data-ttu-id="a184b-158">Questo codice di errore viene generato ogni volta che i componenti di runtime di Windows Media Format in Windows XP non riescono ad acquisire una licenza durante l'acquisizione di una licenza invisibile all'utente o non interattiva.</span><span class="sxs-lookup"><span data-stu-id="a184b-158">This error code is generated whenever the Windows Media Format run-time components on Windows XP fail to acquire a license during silent or non-silent license acquisition.</span></span> <span data-ttu-id="a184b-159">In altre piattaforme, l' \_ \_ errore dell'archivio licenze NS E DRM viene in \_ \_ \_ genere restituito quando l'acquisizione della licenza ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="a184b-159">On other platforms, NS\_E\_DRM\_LICENSE\_STORE\_ERROR is usually returned when license acquisition fails.</span></span> <span data-ttu-id="a184b-160">Il nuovo codice di errore è destinato a distinguere gli errori di acquisizione della licenza da altre condizioni di errore in cui \_ \_ \_ viene generato l'errore dell'archivio licenze NS E DRM \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a184b-160">The new error code is intended to distinguish license acquisition failure from other failure conditions where NS\_E\_DRM\_LICENSE\_STORE\_ERROR is generated.</span></span>

<span data-ttu-id="a184b-161">Il metodo consigliato per gestire questi errori quando vengono restituiti dopo che è stato eseguito un tentativo di acquisizione di una licenza invisibile all'utente nel seguente frammento di codice:</span><span class="sxs-lookup"><span data-stu-id="a184b-161">The recommended way to handle these errors when they are returned after a silent license acquisition attempt is shown in the following code snippet:</span></span>


```C++
if( hrStatus == NS_E_DRM_LICENSE_NOTACQUIRED || 
    hrStatus == NS_E_DRM_LICENSE_STORE_ERROR )
{
  // Attempt non-silent license acquisition.
}
else if( hrStatus == NS_E_DRM_NEEDS_INDIVIDUALIZATION )
{
  // Individualize and then retry.
}
else if( FAILED(hrStatus) )
{
  // Display a helpful error message.
}
else
{
  // Success. Play content.
}
```



> [!Note]  
> <span data-ttu-id="a184b-162">Il DRM non è supportato dalla versione basata su x64 di questo SDK.</span><span class="sxs-lookup"><span data-stu-id="a184b-162">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a184b-163">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a184b-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a184b-164">**Lettura di file protetti**</span><span class="sxs-lookup"><span data-stu-id="a184b-164">**Reading Protected Files**</span></span>](reading-protected-files.md)
</dt> </dl>

 

 




