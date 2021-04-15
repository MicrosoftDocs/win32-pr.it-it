---
title: Protezione dei file con DRM versione 1
description: Protezione dei file con DRM versione 1
ms.assetid: 91de1c20-e926-4ff6-b0cd-e90fc9cbaad2
keywords:
- Windows Media Format SDK, creazione di file protetti
- Windows Media Format SDK, file protetti
- ASF (Advanced Systems Format), creazione di file protetti
- ASF (Advanced Systems Format), creazione di file protetti
- ASF (Advanced Systems Format), file protetti
- ASF (Advanced Systems Format), file protetti
- Formato Advanced Systems (ASF), WMStubDRM. lib
- ASF (formato avanzato dei sistemi), WMStubDRM. lib
- WMStubDRM. lib, creazione di file protetti
- WMStubDRM. lib, file protetti
- Digital Rights Management (DRM), WMStubDRM. lib
- DRM (Digital Rights Management), WMStubDRM. lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3e4d1ae9c0d3835c20f75b4e61c262a85a26f4
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "104336650"
---
# <a name="protecting-files-with-drm-version-1"></a><span data-ttu-id="17b2b-115">Protezione dei file con DRM versione 1</span><span class="sxs-lookup"><span data-stu-id="17b2b-115">Protecting Files with DRM Version 1</span></span>

<span data-ttu-id="17b2b-116">Quando viene applicato questo tipo di protezione, viene generata una licenza DRM versione 1 che è valida solo nel computer da cui è stata effettuata la richiesta di licenza.</span><span class="sxs-lookup"><span data-stu-id="17b2b-116">When this kind of protection is applied, a DRM version 1 license is generated that is valid only on the machine from which the license request was made.</span></span> <span data-ttu-id="17b2b-117">Poiché non è impostato alcun valore di inizializzazione chiave o chiave, non è possibile generare licenze portabili per il contenuto protetto mediante questa tecnica.</span><span class="sxs-lookup"><span data-stu-id="17b2b-117">Because no key or key seed is set, there is no way to generate portable licenses for content protected using this technique.</span></span> <span data-ttu-id="17b2b-118">Tuttavia, quando si usa Windows Media Format SDK 7,1 o versione successiva, le licenze sono recuperabili dal servizio migrazione licenze Microsoft.</span><span class="sxs-lookup"><span data-stu-id="17b2b-118">However, when using the Windows Media Format SDK 7.1 or later, the licenses are recoverable at the Microsoft License Migration service.</span></span>

<span data-ttu-id="17b2b-119">Per proteggere i file ASF usando DRM versione 1, seguire questa procedura:</span><span class="sxs-lookup"><span data-stu-id="17b2b-119">To protect ASF files using DRM version 1, perform the following steps:</span></span>

1.  <span data-ttu-id="17b2b-120">Collegare il file WMStubDRM. lib al progetto e, se necessario, scollegare wmvcore. lib.</span><span class="sxs-lookup"><span data-stu-id="17b2b-120">Link the WMStubDRM.lib file to your project and, if necessary, unlink wmvcore.lib.</span></span>
2.  <span data-ttu-id="17b2b-121">Chiamare la funzione [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) per creare il writer.</span><span class="sxs-lookup"><span data-stu-id="17b2b-121">Call the [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) function to create the writer.</span></span> <span data-ttu-id="17b2b-122">Il primo argomento è riservato e deve essere impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="17b2b-122">The first argument is reserved and must be set to **NULL**.</span></span>
3.  <span data-ttu-id="17b2b-123">Impostare un profilo per il writer da utilizzare chiamando [**IWMWriter:: seprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) o [**IWMWriter:: SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid).</span><span class="sxs-lookup"><span data-stu-id="17b2b-123">Set a profile for the writer to use by calling [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) or [**IWMWriter::SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid).</span></span> <span data-ttu-id="17b2b-124">Prima di impostare gli attributi DRM, è necessario impostare un profilo nel writer.</span><span class="sxs-lookup"><span data-stu-id="17b2b-124">You must set a profile in the writer before setting any DRM attributes.</span></span> <span data-ttu-id="17b2b-125">Il DRM è supportato solo per i profili che usano i codec Windows Media Audio o Windows Media Video.</span><span class="sxs-lookup"><span data-stu-id="17b2b-125">DRM is supported only for profiles that use the Windows Media Audio or Windows Media Video codecs.</span></span>
4.  <span data-ttu-id="17b2b-126">Utilizzando il metodo [**IWMHeaderInfo:: SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) , impostare le proprietà DRM seguenti.</span><span class="sxs-lookup"><span data-stu-id="17b2b-126">Using the [**IWMHeaderInfo::SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) method, set the following DRM properties.</span></span> <span data-ttu-id="17b2b-127">La proprietà **utilizza \_ DRM** indica ai componenti DRM di proteggere il contenuto utilizzando DRM versione 1.</span><span class="sxs-lookup"><span data-stu-id="17b2b-127">The **Use\_DRM** property instructs the DRM components to protect the content using DRM version 1.</span></span> <span data-ttu-id="17b2b-128">La **proprietà \_ flag DRM** specifica i diritti da includere nella licenza locale che verrà creata per il contenuto.</span><span class="sxs-lookup"><span data-stu-id="17b2b-128">The **DRM\_Flags** property specifies the rights to be included in the local license that will be created for the content.</span></span> <span data-ttu-id="17b2b-129">Il valore del **\_ livello di DRM** è archiviato anche nella licenza. specifica il livello minimo necessario per accedere al contenuto.</span><span class="sxs-lookup"><span data-stu-id="17b2b-129">The **DRM\_LEVEL** value is also stored in the license; it specifies the minimum level required to access the content.</span></span> <span data-ttu-id="17b2b-130">150 è il livello consigliato per il contenuto DRM versione 1.</span><span class="sxs-lookup"><span data-stu-id="17b2b-130">150 is the recommended level for DRM version 1 content.</span></span>

    | <span data-ttu-id="17b2b-131">Attributo</span><span class="sxs-lookup"><span data-stu-id="17b2b-131">Attribute</span></span>      | <span data-ttu-id="17b2b-132">Valore</span><span class="sxs-lookup"><span data-stu-id="17b2b-132">Value</span></span>                                                                                       |
    |----------------|---------------------------------------------------------------------------------------------|
    | <span data-ttu-id="17b2b-133">**USA \_ DRM**</span><span class="sxs-lookup"><span data-stu-id="17b2b-133">**Use\_DRM**</span></span>   | <span data-ttu-id="17b2b-134">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="17b2b-134">**TRUE**</span></span>                                                                                    |
    | <span data-ttu-id="17b2b-135">**\_Flag DRM**</span><span class="sxs-lookup"><span data-stu-id="17b2b-135">**DRM\_Flags**</span></span> | <span data-ttu-id="17b2b-136">WMT \_ right \_ playback \| WMT \_ right \_ copy \_ to \_ non \_ SDMI \_ Device \| WMT \_ right \_ copy \_ to \_ CD</span><span class="sxs-lookup"><span data-stu-id="17b2b-136">WMT\_RIGHT\_PLAYBACK \| WMT\_RIGHT\_COPY\_TO\_NON\_SDMI\_DEVICE \| WMT\_RIGHT\_COPY\_TO\_CD</span></span> |
    | <span data-ttu-id="17b2b-137">**\_livello DRM**</span><span class="sxs-lookup"><span data-stu-id="17b2b-137">**DRM\_LEVEL**</span></span> | <span data-ttu-id="17b2b-138">150</span><span class="sxs-lookup"><span data-stu-id="17b2b-138">150</span></span>                                                                                         |

    

     

<span data-ttu-id="17b2b-139">Nell'esempio di codice seguente viene illustrato come creare un writer abilitato per DRM per DRM versione 1 e impostare le proprietà DRM.</span><span class="sxs-lookup"><span data-stu-id="17b2b-139">The following example code shows how to create a DRM-enabled writer for DRM version 1 and set the DRM properties.</span></span> <span data-ttu-id="17b2b-140">Il controllo degli errori è stato omesso per chiarire la causa.</span><span class="sxs-lookup"><span data-stu-id="17b2b-140">Error checking has been omitted for the sake of clarify.</span></span>


```C++
BOOL  fUseDRM    = TRUE;
// These are the rights we will apply to the file. See WMT_RIGHTS for
// the full set of possible rights.

DWORD dwDRMFlags = WMT_RIGHT_PLAYBACK | 
                   WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE | 
                   WMT_RIGHT_COPY_TO_CD;

// Set the minimum required DRM level low enough
// to allow older players to access the content.
DWORD dwDRMLevel = 150;

IWMDRMWriter*  pWMDRMWriter  = NULL;
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a writer object.
hr = WMCreateWriter( NULL, &pWMDRMWriter);

// Obtain the IWMHeaderInfo interface.
hr = pWMDRMWriter -> QueryInterface(IID_IWMHeaderInfo, 
                                   (void**) &pWMHeaderInfo);

// Tell the SDK runtime to protect the file using DRM version 1.
hr= pWMHeaderInfo-> SetAttribute(0,
                                 g_wszWMUse_DRM,
                                 WMT_TYPE_BOOL,
                                 (BYTE*)&fUseDRM,
                                 sizeof(BOOL));

// Specify the rights that will be stored in the local license that is
// created automatically for the content.
hr= pWMHeaderInfo->SetAttribute( 0,
                                 g_wszWMDRM_Flags, 
                                 WMT_TYPE_DWORD,
                                 (BYTE *)&dwDRMFlags,
                                 sizeof(DWORD) );

// Set the DRM_Level attribute in the file's DRM header.
hr= pWMHeaderInfo->SetAttribute( 0,
                                 g_wszWMDRM_Level, 
                                 WMT_TYPE_DWORD,
                                 (BYTE *)&dwDRMLevel,
                                 sizeof(DWORD) );
```



 

 




