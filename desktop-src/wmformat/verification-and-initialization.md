---
title: Verifica e inizializzazione
description: Verifica e inizializzazione
ms.assetid: e92abaa2-0bac-4c78-bda7-d118c4f5b332
keywords:
- Windows Media Format SDK, verifica
- Windows Media Format SDK, inizializzazione
- Digital Rights Management (DRM), verifica
- DRM (Digital Rights Management), verifica
- Digital Rights Management (DRM), inizializzazione
- DRM (Digital Rights Management), inizializzazione
- API estese del client DRM, verifica
- API estese client, verifica
- API estese del client DRM, inizializzazione
- API estese client, inizializzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59c54b56e0622fb65a1a57ae1909e0e6e64aaca6
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336377"
---
# <a name="verification-and-initialization"></a><span data-ttu-id="ff3ed-113">Verifica e inizializzazione</span><span class="sxs-lookup"><span data-stu-id="ff3ed-113">Verification and Initialization</span></span>

<span data-ttu-id="ff3ed-114">È necessario eseguire la procedura seguente per verificare che la transcrittografia sia consentita e inizializzare un oggetto che definirà il contenuto:</span><span class="sxs-lookup"><span data-stu-id="ff3ed-114">You should perform the following steps to verify that transcryption is allowed and to initialize an object that will decrypt the content:</span></span>

1.  <span data-ttu-id="ff3ed-115">Se si dispone già dell'ID chiave per il contenuto, andare al passaggio 5.</span><span class="sxs-lookup"><span data-stu-id="ff3ed-115">If you already have the Key ID for the content, skip to step 5.</span></span>
2.  <span data-ttu-id="ff3ed-116">Chiamare la funzione [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor) per creare un oggetto dell'editor di metadati e ottenere un'istanza dell'interfaccia [**IWMMetadataEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor) di tale oggetto.</span><span class="sxs-lookup"><span data-stu-id="ff3ed-116">Call the [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor) function to create a metadata editor object and get an instance of that object's [**IWMMetadataEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor) interface.</span></span>
3.  <span data-ttu-id="ff3ed-117">Chiamare **IWMMetadataEditor:: QueryInterface** per ottenere un'istanza dell'interfaccia [**IWMDRMEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor) .</span><span class="sxs-lookup"><span data-stu-id="ff3ed-117">Call **IWMMetadataEditor::QueryInterface** to get an instance of the [**IWMDRMEditor**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor) interface.</span></span>
4.  <span data-ttu-id="ff3ed-118">Chiamare [**IWMDRMEditor:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmeditor-getdrmproperty) per ottenere la proprietà **DRM \_ DRMHeader \_ keyId** .</span><span class="sxs-lookup"><span data-stu-id="ff3ed-118">Call [**IWMDRMEditor::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmeditor-getdrmproperty) to get the **DRM\_DRMHeader\_KeyID** property.</span></span>
5.  <span data-ttu-id="ff3ed-119">Inizializzare le API estese del client Windows Media DRM chiamando la funzione [**WMDRMStartup**](wmdrmstartup.md) .</span><span class="sxs-lookup"><span data-stu-id="ff3ed-119">Initialize the Windows Media DRM Client Extended APIs by calling the [**WMDRMStartup**](wmdrmstartup.md) function.</span></span>
6.  <span data-ttu-id="ff3ed-120">Chiamare la funzione [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md) per creare un oggetto provider protetto e ottenere un'istanza dell'interfaccia [**IWMDRMProvider**](iwmdrmprovider.md) di tale oggetto.</span><span class="sxs-lookup"><span data-stu-id="ff3ed-120">Call the [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md) function to create a secure provider object and get an instance of that object's [**IWMDRMProvider**](iwmdrmprovider.md) interface.</span></span>
7.  <span data-ttu-id="ff3ed-121">Chiamare [**IWMDRMProvider:: CreateObject**](iwmdrmprovider-createobject.md) per creare un oggetto di gestione delle licenze e ottenere un'istanza della relativa interfaccia [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md) .</span><span class="sxs-lookup"><span data-stu-id="ff3ed-121">Call [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md) to create a license management object and get an instance of its [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md) interface.</span></span>
8.  <span data-ttu-id="ff3ed-122">Chiamare [**IWMDRMLicenseManagement:: CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md), passando l'ID chiave e il diritto che governa le azioni da intraprendere con il contenuto dopo che è stato transcripto.</span><span class="sxs-lookup"><span data-stu-id="ff3ed-122">Call [**IWMDRMLicenseManagement::CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md), passing in the Key ID and the right that governs the actions to be taken with the content after it is transcrypted.</span></span> <span data-ttu-id="ff3ed-123">Questa chiamata recupererà un'istanza dell'interfaccia [**IWMDRMLicense**](iwmdrmlicense.md) che può essere utilizzata per enumerare tutte le licenze corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="ff3ed-123">This call will retrieve an instance of the [**IWMDRMLicense**](iwmdrmlicense.md) interface that can be used to enumerate through any matching licenses.</span></span>
9.  <span data-ttu-id="ff3ed-124">Chiamare [**IWMDRMLicense:: Getinclusionname**](iwmdrmlicense-getinclusionlist.md) per recuperare l'elenco dei sistemi di protezione del contenuto (CPS) autorizzati come specificato dall'emittente della licenza.</span><span class="sxs-lookup"><span data-stu-id="ff3ed-124">Call [**IWMDRMLicense::GetInclusionList**](iwmdrmlicense-getinclusionlist.md) to retrieve the list of authorized content protection systems (CPS) as specified by the license issuer.</span></span>
10. <span data-ttu-id="ff3ed-125">Analizzare l'elenco di inclusione per verificare che il GUID del CPS di output sia consentito dalla licenza.</span><span class="sxs-lookup"><span data-stu-id="ff3ed-125">Parse the inclusion list to confirm that the GUID of the output CPS is allowed by the license.</span></span>
11. <span data-ttu-id="ff3ed-126">Se il GUID di esportazione desiderato non è presente nell'elenco di inclusione, chiamare [**IWMDRMLicense:: GetNext**](iwmdrmlicense-getnext.md) per ottenere la licenza applicabile successiva, se presente, e ripetere i passaggi 9 e 10.</span><span class="sxs-lookup"><span data-stu-id="ff3ed-126">If the desired export GUID is not in the inclusion list, call [**IWMDRMLicense::GetNext**](iwmdrmlicense-getnext.md) to get the next applicable license (if any) and repeat steps 9 and 10.</span></span> <span data-ttu-id="ff3ed-127">Se nessuna licenza dispone del GUID desiderato nell'elenco di inclusione, non è possibile eseguire l'esportazione.</span><span class="sxs-lookup"><span data-stu-id="ff3ed-127">If no license has the desired GUID in its inclusion list, the export cannot be performed.</span></span>
12. <span data-ttu-id="ff3ed-128">Chiamare [**IWMDRMLicense:: CreateSecureDecryptor**](iwmdrmlicense-createsecuredecryptor.md) per creare un oggetto di decrittografia.</span><span class="sxs-lookup"><span data-stu-id="ff3ed-128">Call [**IWMDRMLicense::CreateSecureDecryptor**](iwmdrmlicense-createsecuredecryptor.md) to create a decryptor object.</span></span> <span data-ttu-id="ff3ed-129">Passare il certificato dell'applicazione di esportazione.</span><span class="sxs-lookup"><span data-stu-id="ff3ed-129">Pass in the export application certificate.</span></span> <span data-ttu-id="ff3ed-130">Questa chiamata fornirà un puntatore a un'istanza dell'interfaccia [**IWMDRMDecrypt**](iwmdrmdecrypt.md) dell'oggetto di decrittografia e a un oggetto binario che contiene il valore di inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="ff3ed-130">This call will provide a pointer to an instance of the decryptor object's [**IWMDRMDecrypt**](iwmdrmdecrypt.md) interface and a binary object containing the seed.</span></span> <span data-ttu-id="ff3ed-131">In questo momento solo la costante **RC4 del \_ tipo di protezione \_ \_ DRM** di Windows Media è supportata come argomento al parametro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="ff3ed-131">Only the Windows Media **DRM\_PROTECTION\_TYPE\_RC4** constant is supported as an argument to the *dwFlags* parameter at this time.</span></span>
13. <span data-ttu-id="ff3ed-132">Usare lo schema di crittografia RSA OAEP per decrittografare il vettore di inizializzazione.</span><span class="sxs-lookup"><span data-stu-id="ff3ed-132">Use the RSA OAEP encryption scheme to decrypt the initialization vector.</span></span>
14. <span data-ttu-id="ff3ed-133">Utilizzare la libreria di analisi ASF fornita da Microsoft quando si immette il contratto di esportazione DRM di Windows Media, per individuare l'offset in byte per ogni payload.</span><span class="sxs-lookup"><span data-stu-id="ff3ed-133">Use the ASF parsing library provided by Microsoft when you enter into the Windows Media DRM export agreement, to locate the offset in bytes for each payload.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff3ed-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ff3ed-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff3ed-135">**Esportazione di contenuto compresso**</span><span class="sxs-lookup"><span data-stu-id="ff3ed-135">**Exporting Compressed Content**</span></span>](exporting-compressed-content.md)
</dt> </dl>

 

 




