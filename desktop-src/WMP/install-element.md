---
title: Elemento install
description: Si noti che questa sezione descrive la funzionalità progettata per l'uso da parte degli archivi online. L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato. L'elemento install specifica i valori usati da Windows Media Player per installare un archivio online.
ms.assetid: 9a5e15ee-ec36-48d3-a1c2-bf20b6d2da48
keywords:
- Installare gli elementi di Windows Media Player
topic_type:
- apiref
api_name:
- Install Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bba56240651f789b45c18b006b16e5e07b10676e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325444"
---
# <a name="install-element"></a><span data-ttu-id="99617-106">Elemento install</span><span class="sxs-lookup"><span data-stu-id="99617-106">Install Element</span></span>

> [!Note]  
> <span data-ttu-id="99617-107">In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online.</span><span class="sxs-lookup"><span data-stu-id="99617-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="99617-108">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="99617-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="99617-109">L'elemento **Install** specifica i valori usati da Windows Media Player per installare un archivio online.</span><span class="sxs-lookup"><span data-stu-id="99617-109">The **Install** element specifies values used by Windows Media Player to install an online store.</span></span>

``` syntax
<Install
    EULAURL = "URL"
    CodeURL = "URL"
    PrivacyInfoURL = "URL"
    InstallApp = "filename"
    InstallData = "commandline"
    CatalogURL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="99617-110">Attributi</span><span class="sxs-lookup"><span data-stu-id="99617-110">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="99617-111"><span id="EULAURL__required_"></span><span id="eulaurl__required_"></span><span id="EULAURL__REQUIRED_"></span>**EULAURL** (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="99617-111"><span id="EULAURL__required_"></span><span id="eulaurl__required_"></span><span id="EULAURL__REQUIRED_"></span>**EULAURL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="99617-112">URL completo di un file con estensione txt utilizzato da Windows Media Player per visualizzare un contratto di licenza con l'utente finale (EULA).</span><span class="sxs-lookup"><span data-stu-id="99617-112">Fully qualified URL for a file with a .txt file name extension that Windows Media Player uses to display an End User License Agreement (EULA).</span></span> <span data-ttu-id="99617-113">Questo file deve essere codificato in formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="99617-113">This file must be encoded in ANSI format.</span></span>

</dd> <dt>

<span data-ttu-id="99617-114"><span id="CodeURL__required_"></span><span id="codeurl__required_"></span><span id="CODEURL__REQUIRED_"></span>**CodeURL** (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="99617-114"><span id="CodeURL__required_"></span><span id="codeurl__required_"></span><span id="CODEURL__REQUIRED_"></span>**CodeURL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="99617-115">URL completo di un pacchetto, con estensione cab, usato per installare l'archivio online.</span><span class="sxs-lookup"><span data-stu-id="99617-115">Fully qualified URL for a package, with a .cab file name extension, that is used to install the online store.</span></span> <span data-ttu-id="99617-116">Il pacchetto e tutti i moduli di codice nel pacchetto devono essere firmati.</span><span class="sxs-lookup"><span data-stu-id="99617-116">The package and all code modules in the package must be signed.</span></span> <span data-ttu-id="99617-117">Per informazioni sulla firma del codice, vedere [Introduzione alla firma del codice](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)) in MSDN Library.</span><span class="sxs-lookup"><span data-stu-id="99617-117">For information about code signing, see [Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)) in the MSDN Library.</span></span>

</dd> <dt>

<span data-ttu-id="99617-118"><span id="PrivacyInfoURL__required_"></span><span id="privacyinfourl__required_"></span><span id="PRIVACYINFOURL__REQUIRED_"></span>**PrivacyInfoURL** (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="99617-118"><span id="PrivacyInfoURL__required_"></span><span id="privacyinfourl__required_"></span><span id="PRIVACYINFOURL__REQUIRED_"></span>**PrivacyInfoURL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="99617-119">URL completo per una pagina Web che contiene informazioni sulla privacy per il negozio online.</span><span class="sxs-lookup"><span data-stu-id="99617-119">Fully qualified URL for a webpage that contains privacy policy information for the online store.</span></span>

</dd> <dt>

<span data-ttu-id="99617-120"><span id="InstallApp__required_"></span><span id="installapp__required_"></span><span id="INSTALLAPP__REQUIRED_"></span>**InstallApp** (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="99617-120"><span id="InstallApp__required_"></span><span id="installapp__required_"></span><span id="INSTALLAPP__REQUIRED_"></span>**InstallApp** (required)</span></span>
</dt> <dd>

<span data-ttu-id="99617-121">Nome del file EXE o INF da eseguire.</span><span class="sxs-lookup"><span data-stu-id="99617-121">Name of the EXE or INF file to run.</span></span> <span data-ttu-id="99617-122">Questo file deve essere contenuto nel file CAB specificato dall'attributo **CodeURL** .</span><span class="sxs-lookup"><span data-stu-id="99617-122">This file must be contained in the CAB file specified by the **CodeURL** attribute.</span></span>

</dd> <dt>

<span data-ttu-id="99617-123"><span id="InstallData__optional_"></span><span id="installdata__optional_"></span><span id="INSTALLDATA__OPTIONAL_"></span>**InstallData** (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="99617-123"><span id="InstallData__optional_"></span><span id="installdata__optional_"></span><span id="INSTALLDATA__OPTIONAL_"></span>**InstallData** (optional)</span></span>
</dt> <dd>

<span data-ttu-id="99617-124">Stringa della riga di comando che viene passata all'applicazione specificata dall'attributo **installApp** .</span><span class="sxs-lookup"><span data-stu-id="99617-124">Command-line string that is passed to the application specified by the **InstallApp** attribute.</span></span> <span data-ttu-id="99617-125">Questo attributo è applicabile solo quando il valore di **installApp** specifica un eseguibile.</span><span class="sxs-lookup"><span data-stu-id="99617-125">This attribute is only applicable when the value for **InstallApp** specifies an executable.</span></span>

</dd> <dt>

<span data-ttu-id="99617-126"><span id="CatalogURL__required_for_type_1__ignored_for_type_2_"></span><span id="catalogurl__required_for_type_1__ignored_for_type_2_"></span><span id="CATALOGURL__REQUIRED_FOR_TYPE_1__IGNORED_FOR_TYPE_2_"></span>**CatalogURL** (obbligatorio per il tipo 1, ignorato per il tipo 2)</span><span class="sxs-lookup"><span data-stu-id="99617-126"><span id="CatalogURL__required_for_type_1__ignored_for_type_2_"></span><span id="catalogurl__required_for_type_1__ignored_for_type_2_"></span><span id="CATALOGURL__REQUIRED_FOR_TYPE_1__IGNORED_FOR_TYPE_2_"></span>**CatalogURL** (required for type 1, ignored for type 2)</span></span>
</dt> <dd>

<span data-ttu-id="99617-127">URL completo per il catalogo compilato del negozio online.</span><span class="sxs-lookup"><span data-stu-id="99617-127">Fully qualified URL for the online store's compiled catalog.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="99617-128">Elementi padre/figlio</span><span class="sxs-lookup"><span data-stu-id="99617-128">Parent/Child Elements</span></span>



| <span data-ttu-id="99617-129">Gerarchia</span><span class="sxs-lookup"><span data-stu-id="99617-129">Hierarchy</span></span>       | <span data-ttu-id="99617-130">Elemento</span><span class="sxs-lookup"><span data-stu-id="99617-130">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="99617-131">Elementi padre</span><span class="sxs-lookup"><span data-stu-id="99617-131">Parent elements</span></span> | <span data-ttu-id="99617-132">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="99617-132">**ServiceInfo**</span></span> |
| <span data-ttu-id="99617-133">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="99617-133">Child elements</span></span>  | <span data-ttu-id="99617-134">nessuno</span><span class="sxs-lookup"><span data-stu-id="99617-134">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="99617-135">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="99617-135">Remarks</span></span>

<span data-ttu-id="99617-136">Se uno degli attributi richiesti risulta mancante o non disponibile, il programma di installazione di Windows Media Player non tenterà di scaricare e installare il codice del provider del negozio online.</span><span class="sxs-lookup"><span data-stu-id="99617-136">If any of the required attributes are missing or not available, Windows Media Player setup will not attempt to download and install the online store provider code.</span></span> <span data-ttu-id="99617-137">Il programma di installazione configurerà i valori predefiniti offline come specificato nel documento **ServiceInfo** .</span><span class="sxs-lookup"><span data-stu-id="99617-137">Setup will configure the offline default values as specified in the **ServiceInfo** document.</span></span> <span data-ttu-id="99617-138">**ServiceInfo** può essere usata quando non si è connessi a Internet passando il nome del provider predefinito e le informazioni di **ServiceInfo** come parametri della riga di comando.</span><span class="sxs-lookup"><span data-stu-id="99617-138">**ServiceInfo** can be used when not connected to the Internet by passing the default provider name and the **ServiceInfo** information as command-line parameters.</span></span> <span data-ttu-id="99617-139">Per informazioni dettagliate sulle opzioni della riga di comando, vedere [ridistribuzione del software Windows Media Player](redistributing-windows-media-player-software.md) .</span><span class="sxs-lookup"><span data-stu-id="99617-139">See [Redistributing Windows Media Player Software](redistributing-windows-media-player-software.md) for details about command-line options.</span></span>

> [!Note]  
> <span data-ttu-id="99617-140">L'uso di questo elemento richiede la firma di un contratto di ridistribuzione con Microsoft.</span><span class="sxs-lookup"><span data-stu-id="99617-140">Use of this element requires that you sign a redistribution agreement with Microsoft.</span></span> <span data-ttu-id="99617-141">Per informazioni dettagliate, contattare il rappresentante aziendale.</span><span class="sxs-lookup"><span data-stu-id="99617-141">Contact your business representative for details.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="99617-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="99617-142">Requirements</span></span>



| <span data-ttu-id="99617-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="99617-143">Requirement</span></span> | <span data-ttu-id="99617-144">Valore</span><span class="sxs-lookup"><span data-stu-id="99617-144">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="99617-145">Versione</span><span class="sxs-lookup"><span data-stu-id="99617-145">Version</span></span><br/> | <span data-ttu-id="99617-146">Windows Media Player 10 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="99617-146">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="99617-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="99617-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99617-148">**Documento ServiceInfo di esempio per un negozio online di tipo 1**</span><span class="sxs-lookup"><span data-stu-id="99617-148">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="99617-149">**Documento ServiceInfo di esempio per un negozio online di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="99617-149">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="99617-150">**Documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="99617-150">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

