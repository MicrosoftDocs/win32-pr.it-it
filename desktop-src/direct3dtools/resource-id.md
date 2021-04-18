---
description: Definisce gli ID risorsa per le risorse di stringa condivise.
MS-HAID: vspixengine.Resource\_Id
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Enumerazione Resource_Id
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: CC04FDC4-CD35-4A87-8EE8-48FFA07B8FC0
api_name:
- Resource_Id
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1e7d93111defb01000e32e4f5ade0c9eb09c827e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521890"
---
# <a name="span-idvspixengineresource_idspanresource_id-enumeration"></a><span data-ttu-id="c4b30-103"><span id="vspixengine.resource_id"></span>\_Enumerazione ID risorsa</span><span class="sxs-lookup"><span data-stu-id="c4b30-103"><span id="vspixengine.resource_id"></span>Resource\_Id enumeration</span></span>

<span data-ttu-id="c4b30-104">Definisce gli ID risorsa per le risorse di stringa condivise.</span><span class="sxs-lookup"><span data-stu-id="c4b30-104">Defines resource IDs for shared string resources.</span></span> <span data-ttu-id="c4b30-105">Questi vengono passati al motore di acquisizione dall'host.</span><span class="sxs-lookup"><span data-stu-id="c4b30-105">These are passed to the capture engine from the host.</span></span> <span data-ttu-id="c4b30-106">Vengono usati per visualizzare le stringhe per la sovrimpressione HUD dell'app acquisita o per passare i valori del registro di sistema dalle opzioni di Visual Studio all'acquisizione Engi</span><span class="sxs-lookup"><span data-stu-id="c4b30-106">They are used to display strings to the HUD overlay of the app being captured or to pass registry values from Visual Studio options to the capture engi</span></span>

## <a name="syntax"></a><span data-ttu-id="c4b30-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c4b30-107">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="c4b30-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="c4b30-108">Constants</span></span>

<span data-ttu-id="c4b30-109"><span id="IDS_ENGINEDISCONNECTED"></span><span id="ids_enginedisconnected"></span>**ID \_ ENGINEDISCONNECTED**</span><span class="sxs-lookup"><span data-stu-id="c4b30-109"><span id="IDS_ENGINEDISCONNECTED"></span><span id="ids_enginedisconnected"></span>**IDS\_ENGINEDISCONNECTED**</span></span>  
<span data-ttu-id="c4b30-110">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-110">Not used.</span></span> <span data-ttu-id="c4b30-111">ID risorsa per la stringa usata in precedenza per indicare che PrintScreen è stato raggiunto al termine della sessione di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="c4b30-111">Resource id for string formerly used to indicate that printscreen was hit after the capture session was complete.</span></span>

<span data-ttu-id="c4b30-112"><span id="IDR_RCDATA1"></span><span id="idr_rcdata1"></span>**\_RCDATA1 IDR**</span><span class="sxs-lookup"><span data-stu-id="c4b30-112"><span id="IDR_RCDATA1"></span><span id="idr_rcdata1"></span>**IDR\_RCDATA1**</span></span>  
<span data-ttu-id="c4b30-113">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-113">Not used.</span></span>

<span data-ttu-id="c4b30-114"><span id="IDS_DEFAULTEXPFILE_CONTENT"></span><span id="ids_defaultexpfile_content"></span>**\_contenuto ID DEFAULTEXPFILE \_**</span><span class="sxs-lookup"><span data-stu-id="c4b30-114"><span id="IDS_DEFAULTEXPFILE_CONTENT"></span><span id="ids_defaultexpfile_content"></span>**IDS\_DEFAULTEXPFILE\_CONTENT**</span></span>  
<span data-ttu-id="c4b30-115">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-115">Not used.</span></span> <span data-ttu-id="c4b30-116">ID risorsa per la stringa usata in precedenza per i dati XML negli scenari di acquisizione legacy.</span><span class="sxs-lookup"><span data-stu-id="c4b30-116">Resource id for string formerly used for XML data in legacy capture scenarios.</span></span>

<span data-ttu-id="c4b30-117"><span id="IDS_CAPTURE_MESSAGE"></span><span id="ids_capture_message"></span>**\_messaggio di acquisizione degli ID \_**</span><span class="sxs-lookup"><span data-stu-id="c4b30-117"><span id="IDS_CAPTURE_MESSAGE"></span><span id="ids_capture_message"></span>**IDS\_CAPTURE\_MESSAGE**</span></span>  
<span data-ttu-id="c4b30-118">ID risorsa per la stringa "frame acquisito".</span><span class="sxs-lookup"><span data-stu-id="c4b30-118">Resource ID for string "Captured frame."</span></span>

<span data-ttu-id="c4b30-119"><span id="IDS_CAPTURE_NOT_SUPPORTED"></span><span id="ids_capture_not_supported"></span>**acquisizione di ID \_ \_ non \_ supportata**</span><span class="sxs-lookup"><span data-stu-id="c4b30-119"><span id="IDS_CAPTURE_NOT_SUPPORTED"></span><span id="ids_capture_not_supported"></span>**IDS\_CAPTURE\_NOT\_SUPPORTED**</span></span>  
<span data-ttu-id="c4b30-120">ID risorsa per la stringa "questo programma ha indicato che non è possibile usarlo con gli strumenti di Diagnostica della grafica".</span><span class="sxs-lookup"><span data-stu-id="c4b30-120">Resource ID for string "This program has indicated that it cannot be used with Graphics Diagnostics tools."</span></span>

<span data-ttu-id="c4b30-121"><span id="IDS_CAPTURE_NOT_SUPPORTED_TITLE"></span><span id="ids_capture_not_supported_title"></span>**\_titolo di acquisizione ID \_ non \_ supportato \_**</span><span class="sxs-lookup"><span data-stu-id="c4b30-121"><span id="IDS_CAPTURE_NOT_SUPPORTED_TITLE"></span><span id="ids_capture_not_supported_title"></span>**IDS\_CAPTURE\_NOT\_SUPPORTED\_TITLE**</span></span>  
<span data-ttu-id="c4b30-122">ID risorsa per la stringa "funzionalità non supportata"</span><span class="sxs-lookup"><span data-stu-id="c4b30-122">Resource ID for string "Unsupported functionality"</span></span>

<span data-ttu-id="c4b30-123"><span id="IDS_FEATURE_NOT_SUPPORTED"></span><span id="ids_feature_not_supported"></span>**\_funzionalità ID \_ non \_ supportata**</span><span class="sxs-lookup"><span data-stu-id="c4b30-123"><span id="IDS_FEATURE_NOT_SUPPORTED"></span><span id="ids_feature_not_supported"></span>**IDS\_FEATURE\_NOT\_SUPPORTED**</span></span>  
<span data-ttu-id="c4b30-124">ID risorsa per la stringa "il livello di funzionalità del dispositivo non è supportato"</span><span class="sxs-lookup"><span data-stu-id="c4b30-124">Resource ID for string "Device feature level not supported"</span></span>

<span data-ttu-id="c4b30-125"><span id="IDS_DXVERSION_NOT_SUPPORTED"></span><span id="ids_dxversion_not_supported"></span>**ID \_ DXVERSION \_ non \_ supportati**</span><span class="sxs-lookup"><span data-stu-id="c4b30-125"><span id="IDS_DXVERSION_NOT_SUPPORTED"></span><span id="ids_dxversion_not_supported"></span>**IDS\_DXVERSION\_NOT\_SUPPORTED**</span></span>  
<span data-ttu-id="c4b30-126">ID risorsa per la stringa "versione DirectX non capturable"</span><span class="sxs-lookup"><span data-stu-id="c4b30-126">Resource ID for string "DirectX version not capturable"</span></span>

<span data-ttu-id="c4b30-127"><span id="IDS_DCOMP_NOT_SUPPORTED"></span><span id="ids_dcomp_not_supported"></span>**ID \_ DCOMP \_ non \_ supportati**</span><span class="sxs-lookup"><span data-stu-id="c4b30-127"><span id="IDS_DCOMP_NOT_SUPPORTED"></span><span id="ids_dcomp_not_supported"></span>**IDS\_DCOMP\_NOT\_SUPPORTED**</span></span>  
<span data-ttu-id="c4b30-128">ID risorsa per la stringa "DCOMP usato dall'app, ma non supportato in questo sistema operativo"</span><span class="sxs-lookup"><span data-stu-id="c4b30-128">Resource ID for string "DCOMP in use by app but not supported on this OS"</span></span>

<span data-ttu-id="c4b30-129"><span id="IDS_DWRITE_NOT_SUPPORTED"></span><span id="ids_dwrite_not_supported"></span>**ID \_ DWrite \_ non \_ supportati**</span><span class="sxs-lookup"><span data-stu-id="c4b30-129"><span id="IDS_DWRITE_NOT_SUPPORTED"></span><span id="ids_dwrite_not_supported"></span>**IDS\_DWRITE\_NOT\_SUPPORTED**</span></span>  
<span data-ttu-id="c4b30-130">ID risorsa per la stringa "DWRITE usato dall'app, ma non supportato in questo sistema operativo"</span><span class="sxs-lookup"><span data-stu-id="c4b30-130">Resource ID for string "DWRITE in use by app but not supported on this OS"</span></span>

<span data-ttu-id="c4b30-131"><span id="IDS_EXPECTED_FAILURE_FORMAT"></span><span id="ids_expected_failure_format"></span>**\_formato di \_ errore \_ previsto per gli ID**</span><span class="sxs-lookup"><span data-stu-id="c4b30-131"><span id="IDS_EXPECTED_FAILURE_FORMAT"></span><span id="ids_expected_failure_format"></span>**IDS\_EXPECTED\_FAILURE\_FORMAT**</span></span>  
<span data-ttu-id="c4b30-132">L'ID risorsa per la stringa "% s ha restituito un errore durante la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="c4b30-132">Resource ID for string "%s returned an error during playback.</span></span> <span data-ttu-id="c4b30-133">(HRESULT =% s) \\ r \\ n ".</span><span class="sxs-lookup"><span data-stu-id="c4b30-133">(HRESULT=%s)\\r\\n".</span></span>

<span data-ttu-id="c4b30-134"><span id="IDS_CAPTURETOOLTIP_MESSAGE"></span><span id="ids_capturetooltip_message"></span>**ID \_ CAPTURETOOLTIP \_ messaggio**</span><span class="sxs-lookup"><span data-stu-id="c4b30-134"><span id="IDS_CAPTURETOOLTIP_MESSAGE"></span><span id="ids_capturetooltip_message"></span>**IDS\_CAPTURETOOLTIP\_MESSAGE**</span></span>  
<span data-ttu-id="c4b30-135">ID risorsa per la stringa "use ' Stamp ' Key per acquisire un frame".</span><span class="sxs-lookup"><span data-stu-id="c4b30-135">Resource ID for string "Use 'Print Screen' key to capture a frame."</span></span>

<span data-ttu-id="c4b30-136"><span id="IDS_D2D_AND_D10_NOT_SUPPORTED"></span><span id="ids_d2d_and_d10_not_supported"></span>**ID \_ D2D \_ e \_ D10 \_ non \_ supportati**</span><span class="sxs-lookup"><span data-stu-id="c4b30-136"><span id="IDS_D2D_AND_D10_NOT_SUPPORTED"></span><span id="ids_d2d_and_d10_not_supported"></span>**IDS\_D2D\_AND\_D10\_NOT\_SUPPORTED**</span></span>  
<span data-ttu-id="c4b30-137">ID risorsa per la stringa "D2D e D10 non supportati insieme in questo sistema operativo"</span><span class="sxs-lookup"><span data-stu-id="c4b30-137">Resource ID for string "D2D and D10 not supported together on this OS"</span></span>

<span data-ttu-id="c4b30-138"><span id="IDS_HUD_STATISTICS"></span><span id="ids_hud_statistics"></span>**\_statistiche HUD \_ ID**</span><span class="sxs-lookup"><span data-stu-id="c4b30-138"><span id="IDS_HUD_STATISTICS"></span><span id="ids_hud_statistics"></span>**IDS\_HUD\_STATISTICS**</span></span>  
<span data-ttu-id="c4b30-139">ID risorsa per la stringa "frame acquisiti% d.</span><span class="sxs-lookup"><span data-stu-id="c4b30-139">Resource ID for string "Frames captured %d.</span></span> <span data-ttu-id="c4b30-140">Tempo fotogramma (MS)% 0.00 f "</span><span class="sxs-lookup"><span data-stu-id="c4b30-140">Frame time (ms) %0.00f"</span></span>

<span data-ttu-id="c4b30-141"><span id="IDS_INTERNAL_METHOD"></span><span id="ids_internal_method"></span>**ID \_ ( \_ metodo interno)**</span><span class="sxs-lookup"><span data-stu-id="c4b30-141"><span id="IDS_INTERNAL_METHOD"></span><span id="ids_internal_method"></span>**IDS\_INTERNAL\_METHOD**</span></span>  
<span data-ttu-id="c4b30-142">ID risorsa per la stringa "metodo interno DirectX"</span><span class="sxs-lookup"><span data-stu-id="c4b30-142">Resource ID for string "Directx Internal Method"</span></span>

<span data-ttu-id="c4b30-143"><span id="IDS_CAPTURE_FRAME_MARK"></span><span id="ids_capture_frame_mark"></span>**\_contrassegno del \_ frame di acquisizione degli ID \_**</span><span class="sxs-lookup"><span data-stu-id="c4b30-143"><span id="IDS_CAPTURE_FRAME_MARK"></span><span id="ids_capture_frame_mark"></span>**IDS\_CAPTURE\_FRAME\_MARK**</span></span>  
<span data-ttu-id="c4b30-144">ID risorsa per la stringa "frame acquisito% LD"</span><span class="sxs-lookup"><span data-stu-id="c4b30-144">Resource ID for string "Captured Frame %ld"</span></span>

<span data-ttu-id="c4b30-145"><span id="PIPELINESTAGE_INPUTASSEMBLER"></span><span id="pipelinestage_inputassembler"></span>**\_INPUTASSEMBLER PIPELINESTAGE**</span><span class="sxs-lookup"><span data-stu-id="c4b30-145"><span id="PIPELINESTAGE_INPUTASSEMBLER"></span><span id="pipelinestage_inputassembler"></span>**PIPELINESTAGE\_INPUTASSEMBLER**</span></span>  
<span data-ttu-id="c4b30-146">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-146">Not used.</span></span>

<span data-ttu-id="c4b30-147"><span id="PIPELINESTAGE_VERTEXSHADER"></span><span id="pipelinestage_vertexshader"></span>**\_VERTEXSHADER PIPELINESTAGE**</span><span class="sxs-lookup"><span data-stu-id="c4b30-147"><span id="PIPELINESTAGE_VERTEXSHADER"></span><span id="pipelinestage_vertexshader"></span>**PIPELINESTAGE\_VERTEXSHADER**</span></span>  
<span data-ttu-id="c4b30-148">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-148">Not used.</span></span>

<span data-ttu-id="c4b30-149"><span id="PIPELINESTAGE_HULLSHADER"></span><span id="pipelinestage_hullshader"></span>**\_HULLSHADER PIPELINESTAGE**</span><span class="sxs-lookup"><span data-stu-id="c4b30-149"><span id="PIPELINESTAGE_HULLSHADER"></span><span id="pipelinestage_hullshader"></span>**PIPELINESTAGE\_HULLSHADER**</span></span>  
<span data-ttu-id="c4b30-150">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-150">Not used.</span></span>

<span data-ttu-id="c4b30-151"><span id="PIPELINESTAGE_TESSELATOR"></span><span id="pipelinestage_tesselator"></span>**\_TESSELATOR PIPELINESTAGE**</span><span class="sxs-lookup"><span data-stu-id="c4b30-151"><span id="PIPELINESTAGE_TESSELATOR"></span><span id="pipelinestage_tesselator"></span>**PIPELINESTAGE\_TESSELATOR**</span></span>  
<span data-ttu-id="c4b30-152">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-152">Not used.</span></span>

<span data-ttu-id="c4b30-153"><span id="PIPELINESTAGE_DOMAINSHADER"></span><span id="pipelinestage_domainshader"></span>**\_DOMAINSHADER PIPELINESTAGE**</span><span class="sxs-lookup"><span data-stu-id="c4b30-153"><span id="PIPELINESTAGE_DOMAINSHADER"></span><span id="pipelinestage_domainshader"></span>**PIPELINESTAGE\_DOMAINSHADER**</span></span>  
<span data-ttu-id="c4b30-154">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-154">Not used.</span></span>

<span data-ttu-id="c4b30-155"><span id="PIPELINESTAGE_GEOMETRYSHADER"></span><span id="pipelinestage_geometryshader"></span>**\_GEOMETRYSHADER PIPELINESTAGE**</span><span class="sxs-lookup"><span data-stu-id="c4b30-155"><span id="PIPELINESTAGE_GEOMETRYSHADER"></span><span id="pipelinestage_geometryshader"></span>**PIPELINESTAGE\_GEOMETRYSHADER**</span></span>  
<span data-ttu-id="c4b30-156">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-156">Not used.</span></span>

<span data-ttu-id="c4b30-157"><span id="PIPELINESTAGE_STREAMOUTPUT"></span><span id="pipelinestage_streamoutput"></span>**\_STREAMOUTPUT PIPELINESTAGE**</span><span class="sxs-lookup"><span data-stu-id="c4b30-157"><span id="PIPELINESTAGE_STREAMOUTPUT"></span><span id="pipelinestage_streamoutput"></span>**PIPELINESTAGE\_STREAMOUTPUT**</span></span>  
<span data-ttu-id="c4b30-158">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-158">Not used.</span></span>

<span data-ttu-id="c4b30-159"><span id="PIPELINESTAGE_RASTERIZER"></span><span id="pipelinestage_rasterizer"></span>**\_rasterizzatore PIPELINESTAGE**</span><span class="sxs-lookup"><span data-stu-id="c4b30-159"><span id="PIPELINESTAGE_RASTERIZER"></span><span id="pipelinestage_rasterizer"></span>**PIPELINESTAGE\_RASTERIZER**</span></span>  
<span data-ttu-id="c4b30-160">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-160">Not used.</span></span>

<span data-ttu-id="c4b30-161"><span id="PIPELINESTAGE_PIXELSHADER"></span><span id="pipelinestage_pixelshader"></span>**\_PIXELSHADER PIPELINESTAGE**</span><span class="sxs-lookup"><span data-stu-id="c4b30-161"><span id="PIPELINESTAGE_PIXELSHADER"></span><span id="pipelinestage_pixelshader"></span>**PIPELINESTAGE\_PIXELSHADER**</span></span>  
<span data-ttu-id="c4b30-162">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-162">Not used.</span></span>

<span data-ttu-id="c4b30-163"><span id="PIPELINESTAGE_OUTPUTMERGER"></span><span id="pipelinestage_outputmerger"></span>**\_OUTPUTMERGER PIPELINESTAGE**</span><span class="sxs-lookup"><span data-stu-id="c4b30-163"><span id="PIPELINESTAGE_OUTPUTMERGER"></span><span id="pipelinestage_outputmerger"></span>**PIPELINESTAGE\_OUTPUTMERGER**</span></span>  
<span data-ttu-id="c4b30-164">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-164">Not used.</span></span>

<span data-ttu-id="c4b30-165"><span id="PIPELINESTAGE_COMPUTESHADER"></span><span id="pipelinestage_computeshader"></span>**\_COMPUTESHADER PIPELINESTAGE**</span><span class="sxs-lookup"><span data-stu-id="c4b30-165"><span id="PIPELINESTAGE_COMPUTESHADER"></span><span id="pipelinestage_computeshader"></span>**PIPELINESTAGE\_COMPUTESHADER**</span></span>  
<span data-ttu-id="c4b30-166">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-166">Not used.</span></span>

<span data-ttu-id="c4b30-167"><span id="BUFFEROBJECT_SUPPORTEDFORMAT"></span><span id="bufferobject_supportedformat"></span>**\_SUPPORTEDFORMAT BUFFEROBJECT**</span><span class="sxs-lookup"><span data-stu-id="c4b30-167"><span id="BUFFEROBJECT_SUPPORTEDFORMAT"></span><span id="bufferobject_supportedformat"></span>**BUFFEROBJECT\_SUPPORTEDFORMAT**</span></span>  
<span data-ttu-id="c4b30-168">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-168">Not used.</span></span>

<span data-ttu-id="c4b30-169"><span id="BUFFEROBJECT_CURRENTFORMAT"></span><span id="bufferobject_currentformat"></span>**\_CURRENTFORMAT BUFFEROBJECT**</span><span class="sxs-lookup"><span data-stu-id="c4b30-169"><span id="BUFFEROBJECT_CURRENTFORMAT"></span><span id="bufferobject_currentformat"></span>**BUFFEROBJECT\_CURRENTFORMAT**</span></span>  
<span data-ttu-id="c4b30-170">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-170">Not used.</span></span>

<span data-ttu-id="c4b30-171"><span id="BUFFEROBJECT_HEADER"></span><span id="bufferobject_header"></span>**\_intestazione BUFFEROBJECT**</span><span class="sxs-lookup"><span data-stu-id="c4b30-171"><span id="BUFFEROBJECT_HEADER"></span><span id="bufferobject_header"></span>**BUFFEROBJECT\_HEADER**</span></span>  
<span data-ttu-id="c4b30-172">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-172">Not used.</span></span>

<span data-ttu-id="c4b30-173"><span id="BUFFEROBJECT_LINE"></span><span id="bufferobject_line"></span>**\_linea BUFFEROBJECT**</span><span class="sxs-lookup"><span data-stu-id="c4b30-173"><span id="BUFFEROBJECT_LINE"></span><span id="bufferobject_line"></span>**BUFFEROBJECT\_LINE**</span></span>  
<span data-ttu-id="c4b30-174">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-174">Not used.</span></span>

<span data-ttu-id="c4b30-175"><span id="BUFFEROBJECT_INVALIDFORMAT"></span><span id="bufferobject_invalidformat"></span>**\_INVALIDFORMAT BUFFEROBJECT**</span><span class="sxs-lookup"><span data-stu-id="c4b30-175"><span id="BUFFEROBJECT_INVALIDFORMAT"></span><span id="bufferobject_invalidformat"></span>**BUFFEROBJECT\_INVALIDFORMAT**</span></span>  
<span data-ttu-id="c4b30-176">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-176">Not used.</span></span>

<span data-ttu-id="c4b30-177"><span id="BUFFEROBJECT_INVALIDEMPTYFORMAT"></span><span id="bufferobject_invalidemptyformat"></span>**\_INVALIDEMPTYFORMAT BUFFEROBJECT**</span><span class="sxs-lookup"><span data-stu-id="c4b30-177"><span id="BUFFEROBJECT_INVALIDEMPTYFORMAT"></span><span id="bufferobject_invalidemptyformat"></span>**BUFFEROBJECT\_INVALIDEMPTYFORMAT**</span></span>  
<span data-ttu-id="c4b30-178">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-178">Not used.</span></span>

<span data-ttu-id="c4b30-179"><span id="BUFFEROBJECT_INVALIDFORMATSIZE"></span><span id="bufferobject_invalidformatsize"></span>**\_INVALIDFORMATSIZE BUFFEROBJECT**</span><span class="sxs-lookup"><span data-stu-id="c4b30-179"><span id="BUFFEROBJECT_INVALIDFORMATSIZE"></span><span id="bufferobject_invalidformatsize"></span>**BUFFEROBJECT\_INVALIDFORMATSIZE**</span></span>  
<span data-ttu-id="c4b30-180">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-180">Not used.</span></span>

<span data-ttu-id="c4b30-181"><span id="SUMMARYINFO_TARGETAPPLICATION"></span><span id="summaryinfo_targetapplication"></span>**\_specificato SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-181"><span id="SUMMARYINFO_TARGETAPPLICATION"></span><span id="summaryinfo_targetapplication"></span>**SUMMARYINFO\_TARGETAPPLICATION**</span></span>  
<span data-ttu-id="c4b30-182">Testo visualizzato nella finestra delle proprietà di vsglog-applicazione di destinazione</span><span class="sxs-lookup"><span data-stu-id="c4b30-182">Text shown in the vsglog properties window - Target Application</span></span>

<span data-ttu-id="c4b30-183"><span id="SUMMARYINFO_PATH"></span><span id="summaryinfo_path"></span>**\_percorso SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-183"><span id="SUMMARYINFO_PATH"></span><span id="summaryinfo_path"></span>**SUMMARYINFO\_PATH**</span></span>  
<span data-ttu-id="c4b30-184">Testo visualizzato in vsglog Finestra Proprietà-Path</span><span class="sxs-lookup"><span data-stu-id="c4b30-184">Text shown in the vsglog Properties window - Path</span></span>

<span data-ttu-id="c4b30-185"><span id="SUMMARYINFO_TARGETVERSION"></span><span id="summaryinfo_targetversion"></span>**\_TARGETVERSION SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-185"><span id="SUMMARYINFO_TARGETVERSION"></span><span id="summaryinfo_targetversion"></span>**SUMMARYINFO\_TARGETVERSION**</span></span>  
<span data-ttu-id="c4b30-186">Testo visualizzato nella versione di vsglog Finestra Proprietà-Target</span><span class="sxs-lookup"><span data-stu-id="c4b30-186">Text shown in the vsglog Properties window - Target Version</span></span>

<span data-ttu-id="c4b30-187"><span id="SUMMARYINFO_LASTMODIFIEDDATE"></span><span id="summaryinfo_lastmodifieddate"></span>**\_LASTMODIFIEDDATE SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-187"><span id="SUMMARYINFO_LASTMODIFIEDDATE"></span><span id="summaryinfo_lastmodifieddate"></span>**SUMMARYINFO\_LASTMODIFIEDDATE**</span></span>  
<span data-ttu-id="c4b30-188">Testo visualizzato nella vsglog Finestra Proprietà-data dell'Ultima modifica</span><span class="sxs-lookup"><span data-stu-id="c4b30-188">Text shown in the vsglog Properties window - Last Modified Date</span></span>

<span data-ttu-id="c4b30-189"><span id="SUMMARYINFO_PROCESSID"></span><span id="summaryinfo_processid"></span>**SUMMARYINFO \_ ProcessID**</span><span class="sxs-lookup"><span data-stu-id="c4b30-189"><span id="SUMMARYINFO_PROCESSID"></span><span id="summaryinfo_processid"></span>**SUMMARYINFO\_PROCESSID**</span></span>  
<span data-ttu-id="c4b30-190">Testo visualizzato in vsglog Finestra Proprietà-Process ID</span><span class="sxs-lookup"><span data-stu-id="c4b30-190">Text shown in the vsglog Properties window - Process ID</span></span>

<span data-ttu-id="c4b30-191"><span id="SUMMARYINFO_EXPERIMENTFILE"></span><span id="summaryinfo_experimentfile"></span>**\_EXPERIMENTFILE SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-191"><span id="SUMMARYINFO_EXPERIMENTFILE"></span><span id="summaryinfo_experimentfile"></span>**SUMMARYINFO\_EXPERIMENTFILE**</span></span>  
<span data-ttu-id="c4b30-192">Testo visualizzato nel file vsglog Finestra Proprietà-Experiment</span><span class="sxs-lookup"><span data-stu-id="c4b30-192">Text shown in the vsglog Properties window - Experiment File</span></span>

<span data-ttu-id="c4b30-193"><span id="SUMMARYINFO_RUNFILE"></span><span id="summaryinfo_runfile"></span>**\_RUNFILE SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-193"><span id="SUMMARYINFO_RUNFILE"></span><span id="summaryinfo_runfile"></span>**SUMMARYINFO\_RUNFILE**</span></span>  
<span data-ttu-id="c4b30-194">Testo visualizzato nel file vsglog Finestra Proprietà-Run</span><span class="sxs-lookup"><span data-stu-id="c4b30-194">Text shown in the vsglog Properties window - Run File</span></span>

<span data-ttu-id="c4b30-195"><span id="SUMMARYINFO_SIZE"></span><span id="summaryinfo_size"></span>**\_dimensioni SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-195"><span id="SUMMARYINFO_SIZE"></span><span id="summaryinfo_size"></span>**SUMMARYINFO\_SIZE**</span></span>  
<span data-ttu-id="c4b30-196">Testo visualizzato in vsglog Finestra Proprietà-Size</span><span class="sxs-lookup"><span data-stu-id="c4b30-196">Text shown in the vsglog Properties window - Size</span></span>

<span data-ttu-id="c4b30-197"><span id="SUMMARYINFO_CREATEDBYPIXVERSION"></span><span id="summaryinfo_createdbypixversion"></span>**\_CREATEDBYPIXVERSION SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-197"><span id="SUMMARYINFO_CREATEDBYPIXVERSION"></span><span id="summaryinfo_createdbypixversion"></span>**SUMMARYINFO\_CREATEDBYPIXVERSION**</span></span>  
<span data-ttu-id="c4b30-198">Testo visualizzato in vsglog Finestra Proprietà creato dalla versione</span><span class="sxs-lookup"><span data-stu-id="c4b30-198">Text shown in the vsglog Properties window - Created By Version</span></span>

<span data-ttu-id="c4b30-199"><span id="SUMMARYINFO_SESSIONSTARTTIME"></span><span id="summaryinfo_sessionstarttime"></span>**\_SESSIONSTARTTIME SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-199"><span id="SUMMARYINFO_SESSIONSTARTTIME"></span><span id="summaryinfo_sessionstarttime"></span>**SUMMARYINFO\_SESSIONSTARTTIME**</span></span>  
<span data-ttu-id="c4b30-200">Testo visualizzato nell'ora di inizio della sessione Finestra Proprietà vsglog</span><span class="sxs-lookup"><span data-stu-id="c4b30-200">Text shown in the vsglog Properties window - Session Start time</span></span>

<span data-ttu-id="c4b30-201"><span id="SUMMARYINFO_SYSTEMINFORMATION"></span><span id="summaryinfo_systeminformation"></span>**SUMMARYINFO \_ SYSTEMINFORMATION**</span><span class="sxs-lookup"><span data-stu-id="c4b30-201"><span id="SUMMARYINFO_SYSTEMINFORMATION"></span><span id="summaryinfo_systeminformation"></span>**SUMMARYINFO\_SYSTEMINFORMATION**</span></span>  
<span data-ttu-id="c4b30-202">Testo visualizzato in vsglog Finestra Proprietà-System Information</span><span class="sxs-lookup"><span data-stu-id="c4b30-202">Text shown in the vsglog Properties window - System Information</span></span>

<span data-ttu-id="c4b30-203"><span id="SUMMARYINFO_PROCESSOR"></span><span id="summaryinfo_processor"></span>**\_processore SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-203"><span id="SUMMARYINFO_PROCESSOR"></span><span id="summaryinfo_processor"></span>**SUMMARYINFO\_PROCESSOR**</span></span>  
<span data-ttu-id="c4b30-204">Testo visualizzato in vsglog Finestra Proprietà-Processor</span><span class="sxs-lookup"><span data-stu-id="c4b30-204">Text shown in the vsglog Properties window - Processor</span></span>

<span data-ttu-id="c4b30-205"><span id="SUMMARYINFO_MEMORY"></span><span id="summaryinfo_memory"></span>**\_memoria SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-205"><span id="SUMMARYINFO_MEMORY"></span><span id="summaryinfo_memory"></span>**SUMMARYINFO\_MEMORY**</span></span>  
<span data-ttu-id="c4b30-206">Testo visualizzato in vsglog Finestra Proprietà-Memory</span><span class="sxs-lookup"><span data-stu-id="c4b30-206">Text shown in the vsglog Properties window - Memory</span></span>

<span data-ttu-id="c4b30-207"><span id="SUMMARYINFO_OSVERSION"></span><span id="summaryinfo_osversion"></span>**\_OSVERSION SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-207"><span id="SUMMARYINFO_OSVERSION"></span><span id="summaryinfo_osversion"></span>**SUMMARYINFO\_OSVERSION**</span></span>  
<span data-ttu-id="c4b30-208">Testo visualizzato nella vsglog Finestra Proprietà-OS Version</span><span class="sxs-lookup"><span data-stu-id="c4b30-208">Text shown in the vsglog Properties window - OS Version</span></span>

<span data-ttu-id="c4b30-209"><span id="SUMMARYINFO_OSARCHITECTURE"></span><span id="summaryinfo_osarchitecture"></span>**\_OSARCHITECTURE SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-209"><span id="SUMMARYINFO_OSARCHITECTURE"></span><span id="summaryinfo_osarchitecture"></span>**SUMMARYINFO\_OSARCHITECTURE**</span></span>  
<span data-ttu-id="c4b30-210">Testo visualizzato nell'architettura vsglog Finestra Proprietà-OS</span><span class="sxs-lookup"><span data-stu-id="c4b30-210">Text shown in the vsglog Properties window - OS Architecture</span></span>

<span data-ttu-id="c4b30-211"><span id="SUMMARYINFO_TARGETAPPARCHITECTURE"></span><span id="summaryinfo_targetapparchitecture"></span>**\_TARGETAPPARCHITECTURE SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-211"><span id="SUMMARYINFO_TARGETAPPARCHITECTURE"></span><span id="summaryinfo_targetapparchitecture"></span>**SUMMARYINFO\_TARGETAPPARCHITECTURE**</span></span>  
<span data-ttu-id="c4b30-212">Testo visualizzato nell'architettura dell'app vsglog Finestra Proprietà-Target</span><span class="sxs-lookup"><span data-stu-id="c4b30-212">Text shown in the vsglog Properties window - Target App Architecture</span></span>

<span data-ttu-id="c4b30-213"><span id="SUMMARYINFO_MAXHWFEATURELEVEL"></span><span id="summaryinfo_maxhwfeaturelevel"></span>**\_MAXHWFEATURELEVEL SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-213"><span id="SUMMARYINFO_MAXHWFEATURELEVEL"></span><span id="summaryinfo_maxhwfeaturelevel"></span>**SUMMARYINFO\_MAXHWFEATURELEVEL**</span></span>  
<span data-ttu-id="c4b30-214">Testo visualizzato nel vsglog Finestra Proprietà-Max livello funzionalità hardware</span><span class="sxs-lookup"><span data-stu-id="c4b30-214">Text shown in the vsglog Properties window - Max Hardware Feature Level</span></span>

<span data-ttu-id="c4b30-215"><span id="SUMMARYINFO_DRIVERCONCURRENTCREATES"></span><span id="summaryinfo_driverconcurrentcreates"></span>**\_DRIVERCONCURRENTCREATES SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-215"><span id="SUMMARYINFO_DRIVERCONCURRENTCREATES"></span><span id="summaryinfo_driverconcurrentcreates"></span>**SUMMARYINFO\_DRIVERCONCURRENTCREATES**</span></span>  
<span data-ttu-id="c4b30-216">Testo visualizzato in vsglog Finestra Proprietà-driver simultanei creati</span><span class="sxs-lookup"><span data-stu-id="c4b30-216">Text shown in the vsglog Properties window - Driver Concurrent Creates</span></span>

<span data-ttu-id="c4b30-217"><span id="SUMMARYINFO_DRIVERCOMMANDLISTS"></span><span id="summaryinfo_drivercommandlists"></span>**\_DRIVERCOMMANDLISTS SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-217"><span id="SUMMARYINFO_DRIVERCOMMANDLISTS"></span><span id="summaryinfo_drivercommandlists"></span>**SUMMARYINFO\_DRIVERCOMMANDLISTS**</span></span>  
<span data-ttu-id="c4b30-218">Testo visualizzato negli elenchi di comandi vsglog Finestra Proprietà-driver</span><span class="sxs-lookup"><span data-stu-id="c4b30-218">Text shown in the vsglog Properties window - Driver Command Lists</span></span>

<span data-ttu-id="c4b30-219"><span id="SUMMARYINFO_DOUBLEPRECISIONSHADERS"></span><span id="summaryinfo_doubleprecisionshaders"></span>**\_DOUBLEPRECISIONSHADERS SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-219"><span id="SUMMARYINFO_DOUBLEPRECISIONSHADERS"></span><span id="summaryinfo_doubleprecisionshaders"></span>**SUMMARYINFO\_DOUBLEPRECISIONSHADERS**</span></span>  
<span data-ttu-id="c4b30-220">Testo visualizzato in vsglog Finestra Proprietà-Double Precision shaders</span><span class="sxs-lookup"><span data-stu-id="c4b30-220">Text shown in the vsglog Properties window - Double Precision Shaders</span></span>

<span data-ttu-id="c4b30-221"><span id="SUMMARYINFO_DIRECTCOMPUTECS4X"></span><span id="summaryinfo_directcomputecs4x"></span>**\_DIRECTCOMPUTECS4X SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-221"><span id="SUMMARYINFO_DIRECTCOMPUTECS4X"></span><span id="summaryinfo_directcomputecs4x"></span>**SUMMARYINFO\_DIRECTCOMPUTECS4X**</span></span>  
<span data-ttu-id="c4b30-222">Testo visualizzato in vsglog Finestra Proprietà-Direct Compute CS 4. x</span><span class="sxs-lookup"><span data-stu-id="c4b30-222">Text shown in the vsglog Properties window - Direct Compute CS 4.x</span></span>

<span data-ttu-id="c4b30-223"><span id="SUMMARYINFO_10BITXRHIGHCOLORFORMAT"></span><span id="summaryinfo_10bitxrhighcolorformat"></span>**\_10BITXRHIGHCOLORFORMAT SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-223"><span id="SUMMARYINFO_10BITXRHIGHCOLORFORMAT"></span><span id="summaryinfo_10bitxrhighcolorformat"></span>**SUMMARYINFO\_10BITXRHIGHCOLORFORMAT**</span></span>  
<span data-ttu-id="c4b30-224">Testo visualizzato in vsglog Finestra Proprietà-10BITXRHIGHCOLORFORMAT</span><span class="sxs-lookup"><span data-stu-id="c4b30-224">Text shown in the vsglog Properties window - 10BITXRHIGHCOLORFORMAT</span></span>

<span data-ttu-id="c4b30-225"><span id="SUMMARYINFO_EXTENDEDCOLORFORMATSUPPORT"></span><span id="summaryinfo_extendedcolorformatsupport"></span>**\_EXTENDEDCOLORFORMATSUPPORT SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-225"><span id="SUMMARYINFO_EXTENDEDCOLORFORMATSUPPORT"></span><span id="summaryinfo_extendedcolorformatsupport"></span>**SUMMARYINFO\_EXTENDEDCOLORFORMATSUPPORT**</span></span>  
<span data-ttu-id="c4b30-226">Testo visualizzato in vsglog Finestra Proprietà-supporto per il formato di colore esteso</span><span class="sxs-lookup"><span data-stu-id="c4b30-226">Text shown in the vsglog Properties window - Extended Color Format Support</span></span>

<span data-ttu-id="c4b30-227"><span id="SUMMARYINFO_DISPLAYINFORMATION"></span><span id="summaryinfo_displayinformation"></span>**\_DISPLAYINFORMATION SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-227"><span id="SUMMARYINFO_DISPLAYINFORMATION"></span><span id="summaryinfo_displayinformation"></span>**SUMMARYINFO\_DISPLAYINFORMATION**</span></span>  
<span data-ttu-id="c4b30-228">Testo visualizzato in vsglog Finestra Proprietà-Visualizza informazioni</span><span class="sxs-lookup"><span data-stu-id="c4b30-228">Text shown in the vsglog Properties window - Display Information</span></span>

<span data-ttu-id="c4b30-229"><span id="SUMMARYINFO_DISPLAYNINFORMATION"></span><span id="summaryinfo_displayninformation"></span>**\_DISPLAYNINFORMATION SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-229"><span id="SUMMARYINFO_DISPLAYNINFORMATION"></span><span id="summaryinfo_displayninformation"></span>**SUMMARYINFO\_DISPLAYNINFORMATION**</span></span>  
<span data-ttu-id="c4b30-230">Testo visualizzato in vsglog Finestra Proprietà-display N Information</span><span class="sxs-lookup"><span data-stu-id="c4b30-230">Text shown in the vsglog Properties window - Display N Information</span></span>

<span data-ttu-id="c4b30-231"><span id="SUMMARYINFO_NAME"></span><span id="summaryinfo_name"></span>**\_nome SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-231"><span id="SUMMARYINFO_NAME"></span><span id="summaryinfo_name"></span>**SUMMARYINFO\_NAME**</span></span>  
<span data-ttu-id="c4b30-232">Testo visualizzato in vsglog Finestra Proprietà-Name</span><span class="sxs-lookup"><span data-stu-id="c4b30-232">Text shown in the vsglog Properties window - Name</span></span>

<span data-ttu-id="c4b30-233"><span id="SUMMARYINFO_DESCRIPTION"></span><span id="summaryinfo_description"></span>**Descrizione di SUMMARYINFO \_**</span><span class="sxs-lookup"><span data-stu-id="c4b30-233"><span id="SUMMARYINFO_DESCRIPTION"></span><span id="summaryinfo_description"></span>**SUMMARYINFO\_DESCRIPTION**</span></span>  
<span data-ttu-id="c4b30-234">Testo visualizzato in vsglog Finestra Proprietà-Description</span><span class="sxs-lookup"><span data-stu-id="c4b30-234">Text shown in the vsglog Properties window - Description</span></span>

<span data-ttu-id="c4b30-235"><span id="SUMMARYINFO_DISPLAYMEMORY"></span><span id="summaryinfo_displaymemory"></span>**\_DISPLAYMEMORY SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-235"><span id="SUMMARYINFO_DISPLAYMEMORY"></span><span id="summaryinfo_displaymemory"></span>**SUMMARYINFO\_DISPLAYMEMORY**</span></span>  
<span data-ttu-id="c4b30-236">Testo visualizzato in vsglog Finestra Proprietà-Display Memory</span><span class="sxs-lookup"><span data-stu-id="c4b30-236">Text shown in the vsglog Properties window - Display Memory</span></span>

<span data-ttu-id="c4b30-237"><span id="SUMMARYINFO_DRIVERNAME"></span><span id="summaryinfo_drivername"></span>**\_drivername SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-237"><span id="SUMMARYINFO_DRIVERNAME"></span><span id="summaryinfo_drivername"></span>**SUMMARYINFO\_DRIVERNAME**</span></span>  
<span data-ttu-id="c4b30-238">Testo visualizzato nel Finestra Proprietà vsglog-nome del driver</span><span class="sxs-lookup"><span data-stu-id="c4b30-238">Text shown in the vsglog Properties window - Driver Name</span></span>

<span data-ttu-id="c4b30-239"><span id="SUMMARYINFO_DRIVERVERSION"></span><span id="summaryinfo_driverversion"></span>**\_DRIVERVERSION SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-239"><span id="SUMMARYINFO_DRIVERVERSION"></span><span id="summaryinfo_driverversion"></span>**SUMMARYINFO\_DRIVERVERSION**</span></span>  
<span data-ttu-id="c4b30-240">Testo visualizzato nella vsglog Finestra Proprietà-Driver Version</span><span class="sxs-lookup"><span data-stu-id="c4b30-240">Text shown in the vsglog Properties window - Driver Version</span></span>

<span data-ttu-id="c4b30-241"><span id="SUMMARYINFO_MODULEINFORMATION"></span><span id="summaryinfo_moduleinformation"></span>**\_MODULEINFORMATION SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-241"><span id="SUMMARYINFO_MODULEINFORMATION"></span><span id="summaryinfo_moduleinformation"></span>**SUMMARYINFO\_MODULEINFORMATION**</span></span>  
<span data-ttu-id="c4b30-242">Testo visualizzato nelle informazioni del modulo Finestra Proprietà vsglog</span><span class="sxs-lookup"><span data-stu-id="c4b30-242">Text shown in the vsglog Properties window - Module Information</span></span>

<span data-ttu-id="c4b30-243"><span id="SUMMARYINFO_DIRECT3DINFORMATION"></span><span id="summaryinfo_direct3dinformation"></span>**\_DIRECT3DINFORMATION SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-243"><span id="SUMMARYINFO_DIRECT3DINFORMATION"></span><span id="summaryinfo_direct3dinformation"></span>**SUMMARYINFO\_DIRECT3DINFORMATION**</span></span>  
<span data-ttu-id="c4b30-244">Testo visualizzato in vsglog Finestra Proprietà-Direct3D Information</span><span class="sxs-lookup"><span data-stu-id="c4b30-244">Text shown in the vsglog Properties window - Direct3D Information</span></span>

<span data-ttu-id="c4b30-245"><span id="SUMMARYINFO_VSGVERSION"></span><span id="summaryinfo_vsgversion"></span>**\_VSGVERSION SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-245"><span id="SUMMARYINFO_VSGVERSION"></span><span id="summaryinfo_vsgversion"></span>**SUMMARYINFO\_VSGVERSION**</span></span>  
<span data-ttu-id="c4b30-246">Testo visualizzato nella versione Finestra Proprietà-VSG di vsglog</span><span class="sxs-lookup"><span data-stu-id="c4b30-246">Text shown in the vsglog Properties window - VSG Version</span></span>

<span data-ttu-id="c4b30-247"><span id="SUMMARYINFO_CAPTUREMACHINE"></span><span id="summaryinfo_capturemachine"></span>**\_CAPTUREMACHINE SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-247"><span id="SUMMARYINFO_CAPTUREMACHINE"></span><span id="summaryinfo_capturemachine"></span>**SUMMARYINFO\_CAPTUREMACHINE**</span></span>  
<span data-ttu-id="c4b30-248">Testo visualizzato nel computer di acquisizione Finestra Proprietà vsglog</span><span class="sxs-lookup"><span data-stu-id="c4b30-248">Text shown in the vsglog Properties window - Capture Machine</span></span>

<span data-ttu-id="c4b30-249"><span id="SUMMARYINFO_PLAYBACKMACHINE"></span><span id="summaryinfo_playbackmachine"></span>**\_PLAYBACKMACHINE SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-249"><span id="SUMMARYINFO_PLAYBACKMACHINE"></span><span id="summaryinfo_playbackmachine"></span>**SUMMARYINFO\_PLAYBACKMACHINE**</span></span>  
<span data-ttu-id="c4b30-250">Testo visualizzato nel computer vsglog Finestra Proprietà-Playback</span><span class="sxs-lookup"><span data-stu-id="c4b30-250">Text shown in the vsglog Properties window - Playback Machine</span></span>

<span data-ttu-id="c4b30-251"><span id="SUMMARYINFO_REMOTEDATA"></span><span id="summaryinfo_remotedata"></span>**\_REMOTEDATA SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-251"><span id="SUMMARYINFO_REMOTEDATA"></span><span id="summaryinfo_remotedata"></span>**SUMMARYINFO\_REMOTEDATA**</span></span>  
<span data-ttu-id="c4b30-252">Testo visualizzato in vsglog Finestra Proprietà-dati remoti</span><span class="sxs-lookup"><span data-stu-id="c4b30-252">Text shown in the vsglog Properties window - Remote Data</span></span>

<span data-ttu-id="c4b30-253"><span id="SUMMARYINFO_OtherDirect3DInformation"></span><span id="summaryinfo_otherdirect3dinformation"></span><span id="SUMMARYINFO_OTHERDIRECT3DINFORMATION"></span>**\_OTHERDIRECT3DINFORMATION SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-253"><span id="SUMMARYINFO_OtherDirect3DInformation"></span><span id="summaryinfo_otherdirect3dinformation"></span><span id="SUMMARYINFO_OTHERDIRECT3DINFORMATION"></span>**SUMMARYINFO\_OtherDirect3DInformation**</span></span>  
<span data-ttu-id="c4b30-254">Testo visualizzato in vsglog Finestra Proprietà-other Direct3D Information</span><span class="sxs-lookup"><span data-stu-id="c4b30-254">Text shown in the vsglog Properties window - Other Direct3D Information</span></span>

<span data-ttu-id="c4b30-255"><span id="SUMMARYINFO_SIZEGB"></span><span id="summaryinfo_sizegb"></span>**\_SIZEGB SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-255"><span id="SUMMARYINFO_SIZEGB"></span><span id="summaryinfo_sizegb"></span>**SUMMARYINFO\_SIZEGB**</span></span>  
<span data-ttu-id="c4b30-256">Testo visualizzato in vsglog Finestra Proprietà-Size GB</span><span class="sxs-lookup"><span data-stu-id="c4b30-256">Text shown in the vsglog Properties window - Size GB</span></span>

<span data-ttu-id="c4b30-257"><span id="SUMMARYINFO_SIZEMB"></span><span id="summaryinfo_sizemb"></span>**\_SIZEMB SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-257"><span id="SUMMARYINFO_SIZEMB"></span><span id="summaryinfo_sizemb"></span>**SUMMARYINFO\_SIZEMB**</span></span>  
<span data-ttu-id="c4b30-258">Testo visualizzato in vsglog Finestra Proprietà-size MB</span><span class="sxs-lookup"><span data-stu-id="c4b30-258">Text shown in the vsglog Properties window - Size MB</span></span>

<span data-ttu-id="c4b30-259"><span id="SUMMARYINFO_SIZEBYTES"></span><span id="summaryinfo_sizebytes"></span>**\_SIZEBYTES SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-259"><span id="SUMMARYINFO_SIZEBYTES"></span><span id="summaryinfo_sizebytes"></span>**SUMMARYINFO\_SIZEBYTES**</span></span>  
<span data-ttu-id="c4b30-260">Testo visualizzato in vsglog Finestra Proprietà-Size bytes</span><span class="sxs-lookup"><span data-stu-id="c4b30-260">Text shown in the vsglog Properties window - Size Bytes</span></span>

<span data-ttu-id="c4b30-261"><span id="SUMMARYINFO_MEMORYMB"></span><span id="summaryinfo_memorymb"></span>**\_MEMORYMB SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-261"><span id="SUMMARYINFO_MEMORYMB"></span><span id="summaryinfo_memorymb"></span>**SUMMARYINFO\_MEMORYMB**</span></span>  
<span data-ttu-id="c4b30-262">Testo visualizzato in vsglog Finestra Proprietà-memory MB</span><span class="sxs-lookup"><span data-stu-id="c4b30-262">Text shown in the vsglog Properties window - Memory MB</span></span>

<span data-ttu-id="c4b30-263"><span id="SUMMARYINFO_X86"></span><span id="summaryinfo_x86"></span>**SUMMARYINFO \_ x86**</span><span class="sxs-lookup"><span data-stu-id="c4b30-263"><span id="SUMMARYINFO_X86"></span><span id="summaryinfo_x86"></span>**SUMMARYINFO\_X86**</span></span>  
<span data-ttu-id="c4b30-264">Testo visualizzato in vsglog Finestra Proprietà-x86</span><span class="sxs-lookup"><span data-stu-id="c4b30-264">Text shown in the vsglog Properties window - X86</span></span>

<span data-ttu-id="c4b30-265"><span id="SUMMARYINFO_X64"></span><span id="summaryinfo_x64"></span>**SUMMARYINFO \_ x64**</span><span class="sxs-lookup"><span data-stu-id="c4b30-265"><span id="SUMMARYINFO_X64"></span><span id="summaryinfo_x64"></span>**SUMMARYINFO\_X64**</span></span>  
<span data-ttu-id="c4b30-266">Testo visualizzato in vsglog Finestra Proprietà-x64</span><span class="sxs-lookup"><span data-stu-id="c4b30-266">Text shown in the vsglog Properties window - X64</span></span>

<span data-ttu-id="c4b30-267"><span id="SUMMARYINFO_TRUE"></span><span id="summaryinfo_true"></span>**SUMMARYINFO \_ true**</span><span class="sxs-lookup"><span data-stu-id="c4b30-267"><span id="SUMMARYINFO_TRUE"></span><span id="summaryinfo_true"></span>**SUMMARYINFO\_TRUE**</span></span>  
<span data-ttu-id="c4b30-268">Testo visualizzato in vsglog Finestra Proprietà-true</span><span class="sxs-lookup"><span data-stu-id="c4b30-268">Text shown in the vsglog Properties window - True</span></span>

<span data-ttu-id="c4b30-269"><span id="SUMMARYINFO_FALSE"></span><span id="summaryinfo_false"></span>**SUMMARYINFO \_ false**</span><span class="sxs-lookup"><span data-stu-id="c4b30-269"><span id="SUMMARYINFO_FALSE"></span><span id="summaryinfo_false"></span>**SUMMARYINFO\_FALSE**</span></span>  
<span data-ttu-id="c4b30-270">Testo visualizzato in vsglog Finestra Proprietà-false</span><span class="sxs-lookup"><span data-stu-id="c4b30-270">Text shown in the vsglog Properties window - False</span></span>

<span data-ttu-id="c4b30-271"><span id="SUMMARYINFO_ARM32"></span><span id="summaryinfo_arm32"></span>**\_ARM32 SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-271"><span id="SUMMARYINFO_ARM32"></span><span id="summaryinfo_arm32"></span>**SUMMARYINFO\_ARM32**</span></span>  
<span data-ttu-id="c4b30-272">Testo visualizzato in vsglog Finestra Proprietà-ARM 32</span><span class="sxs-lookup"><span data-stu-id="c4b30-272">Text shown in the vsglog Properties window - ARM 32</span></span>

<span data-ttu-id="c4b30-273"><span id="SUMMARYINFO_UNKNOWNCPUARCHITECTURE"></span><span id="summaryinfo_unknowncpuarchitecture"></span>**\_UNKNOWNCPUARCHITECTURE SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-273"><span id="SUMMARYINFO_UNKNOWNCPUARCHITECTURE"></span><span id="summaryinfo_unknowncpuarchitecture"></span>**SUMMARYINFO\_UNKNOWNCPUARCHITECTURE**</span></span>  
<span data-ttu-id="c4b30-274">Testo visualizzato in vsglog Finestra Proprietà-architettura CPU sconosciuta</span><span class="sxs-lookup"><span data-stu-id="c4b30-274">Text shown in the vsglog Properties window - Unknown CPU Architecture</span></span>

<span data-ttu-id="c4b30-275"><span id="SUMMARYINFO_AllDXGIFormatValues"></span><span id="summaryinfo_alldxgiformatvalues"></span><span id="SUMMARYINFO_ALLDXGIFORMATVALUES"></span>**\_ALLDXGIFORMATVALUES SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-275"><span id="SUMMARYINFO_AllDXGIFormatValues"></span><span id="summaryinfo_alldxgiformatvalues"></span><span id="SUMMARYINFO_ALLDXGIFORMATVALUES"></span>**SUMMARYINFO\_AllDXGIFormatValues**</span></span>  
<span data-ttu-id="c4b30-276">Testo visualizzato in vsglog Finestra Proprietà-tutti i valori di formato DXGI</span><span class="sxs-lookup"><span data-stu-id="c4b30-276">Text shown in the vsglog Properties window - All DXGI Format Values</span></span>

<span data-ttu-id="c4b30-277"><span id="SUMMARYINFO_AllD3D11FormatSupportValues"></span><span id="summaryinfo_alld3d11formatsupportvalues"></span><span id="SUMMARYINFO_ALLD3D11FORMATSUPPORTVALUES"></span>**\_ALLD3D11FORMATSUPPORTVALUES SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-277"><span id="SUMMARYINFO_AllD3D11FormatSupportValues"></span><span id="summaryinfo_alld3d11formatsupportvalues"></span><span id="SUMMARYINFO_ALLD3D11FORMATSUPPORTVALUES"></span>**SUMMARYINFO\_AllD3D11FormatSupportValues**</span></span>  
<span data-ttu-id="c4b30-278">Testo visualizzato nel vsglog Finestra Proprietà-tutti i valori di supporto del formato D3D11</span><span class="sxs-lookup"><span data-stu-id="c4b30-278">Text shown in the vsglog Properties window - All D3D11 Format Support Values</span></span>

<span data-ttu-id="c4b30-279"><span id="SUMMARYINFO_D3D11_FEATURE_THREADING"></span><span id="summaryinfo_d3d11_feature_threading"></span>**\_ \_ Threading delle funzionalità d3d11 di SUMMARYINFO \_**</span><span class="sxs-lookup"><span data-stu-id="c4b30-279"><span id="SUMMARYINFO_D3D11_FEATURE_THREADING"></span><span id="summaryinfo_d3d11_feature_threading"></span>**SUMMARYINFO\_D3D11\_FEATURE\_THREADING**</span></span>  
<span data-ttu-id="c4b30-280">Testo visualizzato nel \_ Threading delle funzionalità vsglog finestra Proprietà-d3d11 \_</span><span class="sxs-lookup"><span data-stu-id="c4b30-280">Text shown in the vsglog Properties window - D3D11\_FEATURE\_THREADING</span></span>

<span data-ttu-id="c4b30-281"><span id="SUMMARYINFO_DriverConcurrentCreates1"></span><span id="summaryinfo_driverconcurrentcreates1"></span><span id="SUMMARYINFO_DRIVERCONCURRENTCREATES1"></span>**\_DRIVERCONCURRENTCREATES1 SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-281"><span id="SUMMARYINFO_DriverConcurrentCreates1"></span><span id="summaryinfo_driverconcurrentcreates1"></span><span id="SUMMARYINFO_DRIVERCONCURRENTCREATES1"></span>**SUMMARYINFO\_DriverConcurrentCreates1**</span></span>  
<span data-ttu-id="c4b30-282">Testo visualizzato in vsglog Finestra Proprietà-driver Concurrent Crea 1</span><span class="sxs-lookup"><span data-stu-id="c4b30-282">Text shown in the vsglog Properties window - Driver Concurrent Creates 1</span></span>

<span data-ttu-id="c4b30-283"><span id="SUMMARYINFO_DriverCommandLists1"></span><span id="summaryinfo_drivercommandlists1"></span><span id="SUMMARYINFO_DRIVERCOMMANDLISTS1"></span>**\_DRIVERCOMMANDLISTS1 SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-283"><span id="SUMMARYINFO_DriverCommandLists1"></span><span id="summaryinfo_drivercommandlists1"></span><span id="SUMMARYINFO_DRIVERCOMMANDLISTS1"></span>**SUMMARYINFO\_DriverCommandLists1**</span></span>  
<span data-ttu-id="c4b30-284">Testo visualizzato negli elenchi di comandi vsglog Finestra Proprietà-driver 1</span><span class="sxs-lookup"><span data-stu-id="c4b30-284">Text shown in the vsglog Properties window - Driver Command Lists 1</span></span>

<span data-ttu-id="c4b30-285"><span id="SUMMARYINFO_D3D11_FEATURE_DOUBLES"></span><span id="summaryinfo_d3d11_feature_doubles"></span>**SUMMARYINFO \_ d3d11 \_ funzionalità \_ doppie**</span><span class="sxs-lookup"><span data-stu-id="c4b30-285"><span id="SUMMARYINFO_D3D11_FEATURE_DOUBLES"></span><span id="summaryinfo_d3d11_feature_doubles"></span>**SUMMARYINFO\_D3D11\_FEATURE\_DOUBLES**</span></span>  
<span data-ttu-id="c4b30-286">Il testo visualizzato nella funzionalità vsglog Finestra Proprietà- \_ d3d11 \_ raddoppia</span><span class="sxs-lookup"><span data-stu-id="c4b30-286">Text shown in the vsglog Properties window - D3D11\_FEATURE\_DOUBLES</span></span>

<span data-ttu-id="c4b30-287"><span id="SUMMARYINFO_DoublePrecisionFloatShaderOps"></span><span id="summaryinfo_doubleprecisionfloatshaderops"></span><span id="SUMMARYINFO_DOUBLEPRECISIONFLOATSHADEROPS"></span>**\_DOUBLEPRECISIONFLOATSHADEROPS SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-287"><span id="SUMMARYINFO_DoublePrecisionFloatShaderOps"></span><span id="summaryinfo_doubleprecisionfloatshaderops"></span><span id="SUMMARYINFO_DOUBLEPRECISIONFLOATSHADEROPS"></span>**SUMMARYINFO\_DoublePrecisionFloatShaderOps**</span></span>  
<span data-ttu-id="c4b30-288">Testo visualizzato in vsglog Finestra Proprietà-operazioni di shader con precisione doppia float</span><span class="sxs-lookup"><span data-stu-id="c4b30-288">Text shown in the vsglog Properties window - Double Precision Float Shader Ops</span></span>

<span data-ttu-id="c4b30-289"><span id="SUMMARYINFO_D3D11_FEATURE_D3D10_X_HARDWARE_OPTIONS"></span><span id="summaryinfo_d3d11_feature_d3d10_x_hardware_options"></span>**SUMMARYINFO \_ d3d11 \_ funzionalità \_ D3D10 \_ X \_ hardware \_**</span><span class="sxs-lookup"><span data-stu-id="c4b30-289"><span id="SUMMARYINFO_D3D11_FEATURE_D3D10_X_HARDWARE_OPTIONS"></span><span id="summaryinfo_d3d11_feature_d3d10_x_hardware_options"></span>**SUMMARYINFO\_D3D11\_FEATURE\_D3D10\_X\_HARDWARE\_OPTIONS**</span></span>  
<span data-ttu-id="c4b30-290">Testo visualizzato nella vsglog Finestra Proprietà-D3D11 \_ funzionalità \_ D3D10 \_ X \_ hardware \_ Options</span><span class="sxs-lookup"><span data-stu-id="c4b30-290">Text shown in the vsglog Properties window - D3D11\_FEATURE\_D3D10\_X\_HARDWARE\_OPTIONS</span></span>

<span data-ttu-id="c4b30-291"><span id="SUMMARYINFO_ComputeShaders_Plus_RawAndStructuredBuffers_Via_Shader_4_x"></span><span id="summaryinfo_computeshaders_plus_rawandstructuredbuffers_via_shader_4_x"></span><span id="SUMMARYINFO_COMPUTESHADERS_PLUS_RAWANDSTRUCTUREDBUFFERS_VIA_SHADER_4_X"></span>**SUMMARYINFO \_ ComputeShaders \_ Plus \_ RawAndStructuredBuffers \_ tramite \_ shader \_ 4 \_ x**</span><span class="sxs-lookup"><span data-stu-id="c4b30-291"><span id="SUMMARYINFO_ComputeShaders_Plus_RawAndStructuredBuffers_Via_Shader_4_x"></span><span id="summaryinfo_computeshaders_plus_rawandstructuredbuffers_via_shader_4_x"></span><span id="SUMMARYINFO_COMPUTESHADERS_PLUS_RAWANDSTRUCTUREDBUFFERS_VIA_SHADER_4_X"></span>**SUMMARYINFO\_ComputeShaders\_Plus\_RawAndStructuredBuffers\_Via\_Shader\_4\_x**</span></span>  
<span data-ttu-id="c4b30-292">Testo visualizzato in vsglog Finestra Proprietà-ComputeShaders + RAW e Structure dBuffers tramite Shader 4. x</span><span class="sxs-lookup"><span data-stu-id="c4b30-292">Text shown in the vsglog Properties window - ComputeShaders + Raw and Structure dBuffers via Shader 4.x</span></span>

<span data-ttu-id="c4b30-293"><span id="SUMMARYINFO_D3D11_FEATURE_D3D11_OPTIONS"></span><span id="summaryinfo_d3d11_feature_d3d11_options"></span>**\_ \_ Opzioni d3d11 della funzionalità d3d11 \_ di \_ SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-293"><span id="SUMMARYINFO_D3D11_FEATURE_D3D11_OPTIONS"></span><span id="summaryinfo_d3d11_feature_d3d11_options"></span>**SUMMARYINFO\_D3D11\_FEATURE\_D3D11\_OPTIONS**</span></span>  
<span data-ttu-id="c4b30-294">Testo visualizzato nella vsglog Finestra Proprietà-D3D11 \_ funzionalità \_ d3d11 \_ Opzioni</span><span class="sxs-lookup"><span data-stu-id="c4b30-294">Text shown in the vsglog Properties window - D3D11\_FEATURE\_D3D11\_OPTIONS</span></span>

<span data-ttu-id="c4b30-295"><span id="SUMMARYINFO_OutputMergerLogicOp"></span><span id="summaryinfo_outputmergerlogicop"></span><span id="SUMMARYINFO_OUTPUTMERGERLOGICOP"></span>**\_OUTPUTMERGERLOGICOP SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-295"><span id="SUMMARYINFO_OutputMergerLogicOp"></span><span id="summaryinfo_outputmergerlogicop"></span><span id="SUMMARYINFO_OUTPUTMERGERLOGICOP"></span>**SUMMARYINFO\_OutputMergerLogicOp**</span></span>  
<span data-ttu-id="c4b30-296">Testo visualizzato nel vsglog Finestra Proprietà-output della logica di Unione</span><span class="sxs-lookup"><span data-stu-id="c4b30-296">Text shown in the vsglog Properties window - Output Merger Logic Op</span></span>

<span data-ttu-id="c4b30-297"><span id="SUMMARYINFO_UAVOnlyRenderingForcedSampleCount"></span><span id="summaryinfo_uavonlyrenderingforcedsamplecount"></span><span id="SUMMARYINFO_UAVONLYRENDERINGFORCEDSAMPLECOUNT"></span>**\_UAVONLYRENDERINGFORCEDSAMPLECOUNT SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-297"><span id="SUMMARYINFO_UAVOnlyRenderingForcedSampleCount"></span><span id="summaryinfo_uavonlyrenderingforcedsamplecount"></span><span id="SUMMARYINFO_UAVONLYRENDERINGFORCEDSAMPLECOUNT"></span>**SUMMARYINFO\_UAVOnlyRenderingForcedSampleCount**</span></span>  
<span data-ttu-id="c4b30-298">Testo visualizzato nel vsglog Finestra Proprietà-UAV che esegue solo il rendering del numero di campioni forzato</span><span class="sxs-lookup"><span data-stu-id="c4b30-298">Text shown in the vsglog Properties window - UAV Only Rendering Forced Sample Count</span></span>

<span data-ttu-id="c4b30-299"><span id="SUMMARYINFO_DiscardAPIsSeenByDriver"></span><span id="summaryinfo_discardapisseenbydriver"></span><span id="SUMMARYINFO_DISCARDAPISSEENBYDRIVER"></span>**\_DISCARDAPISSEENBYDRIVER SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-299"><span id="SUMMARYINFO_DiscardAPIsSeenByDriver"></span><span id="summaryinfo_discardapisseenbydriver"></span><span id="SUMMARYINFO_DISCARDAPISSEENBYDRIVER"></span>**SUMMARYINFO\_DiscardAPIsSeenByDriver**</span></span>  
<span data-ttu-id="c4b30-300">Testo visualizzato in vsglog Finestra Proprietà-ignora le API visualizzate dal driver</span><span class="sxs-lookup"><span data-stu-id="c4b30-300">Text shown in the vsglog Properties window - Discard APIs Seen By Driver</span></span>

<span data-ttu-id="c4b30-301"><span id="SUMMARYINFO_FlagsForUpdateAndCopySeenByDriver"></span><span id="summaryinfo_flagsforupdateandcopyseenbydriver"></span><span id="SUMMARYINFO_FLAGSFORUPDATEANDCOPYSEENBYDRIVER"></span>**\_FLAGSFORUPDATEANDCOPYSEENBYDRIVER SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-301"><span id="SUMMARYINFO_FlagsForUpdateAndCopySeenByDriver"></span><span id="summaryinfo_flagsforupdateandcopyseenbydriver"></span><span id="SUMMARYINFO_FLAGSFORUPDATEANDCOPYSEENBYDRIVER"></span>**SUMMARYINFO\_FlagsForUpdateAndCopySeenByDriver**</span></span>  
<span data-ttu-id="c4b30-302">Testo visualizzato in vsglog Finestra Proprietà flag per l'aggiornamento e la copia visualizzati dal driver</span><span class="sxs-lookup"><span data-stu-id="c4b30-302">Text shown in the vsglog Properties window - Flags For Update And Copy Seen By Driver</span></span>

<span data-ttu-id="c4b30-303"><span id="SUMMARYINFO_ClearView"></span><span id="summaryinfo_clearview"></span><span id="SUMMARYINFO_CLEARVIEW"></span>**\_CLEARVIEW SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-303"><span id="SUMMARYINFO_ClearView"></span><span id="summaryinfo_clearview"></span><span id="SUMMARYINFO_CLEARVIEW"></span>**SUMMARYINFO\_ClearView**</span></span>  
<span data-ttu-id="c4b30-304">Testo visualizzato nella visualizzazione Finestra Proprietà vsglog-Clear</span><span class="sxs-lookup"><span data-stu-id="c4b30-304">Text shown in the vsglog Properties window - Clear View</span></span>

<span data-ttu-id="c4b30-305"><span id="SUMMARYINFO_CopyWithOverlap"></span><span id="summaryinfo_copywithoverlap"></span><span id="SUMMARYINFO_COPYWITHOVERLAP"></span>**\_COPYWITHOVERLAP SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-305"><span id="SUMMARYINFO_CopyWithOverlap"></span><span id="summaryinfo_copywithoverlap"></span><span id="SUMMARYINFO_COPYWITHOVERLAP"></span>**SUMMARYINFO\_CopyWithOverlap**</span></span>  
<span data-ttu-id="c4b30-306">Testo visualizzato nel vsglog Finestra Proprietà-copia con sovrapposizione</span><span class="sxs-lookup"><span data-stu-id="c4b30-306">Text shown in the vsglog Properties window - Copy With Overlap</span></span>

<span data-ttu-id="c4b30-307"><span id="SUMMARYINFO_ConstantBufferPartialUpdate"></span><span id="summaryinfo_constantbufferpartialupdate"></span><span id="SUMMARYINFO_CONSTANTBUFFERPARTIALUPDATE"></span>**\_CONSTANTBUFFERPARTIALUPDATE SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-307"><span id="SUMMARYINFO_ConstantBufferPartialUpdate"></span><span id="summaryinfo_constantbufferpartialupdate"></span><span id="SUMMARYINFO_CONSTANTBUFFERPARTIALUPDATE"></span>**SUMMARYINFO\_ConstantBufferPartialUpdate**</span></span>  
<span data-ttu-id="c4b30-308">Testo visualizzato nell'vsglog Finestra Proprietà-aggiornamento parziale del buffer costante</span><span class="sxs-lookup"><span data-stu-id="c4b30-308">Text shown in the vsglog Properties window - Constant Buffer Partial Update</span></span>

<span data-ttu-id="c4b30-309"><span id="SUMMARYINFO_ConstantBufferOffsetting"></span><span id="summaryinfo_constantbufferoffsetting"></span><span id="SUMMARYINFO_CONSTANTBUFFEROFFSETTING"></span>**\_CONSTANTBUFFEROFFSETTING SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-309"><span id="SUMMARYINFO_ConstantBufferOffsetting"></span><span id="summaryinfo_constantbufferoffsetting"></span><span id="SUMMARYINFO_CONSTANTBUFFEROFFSETTING"></span>**SUMMARYINFO\_ConstantBufferOffsetting**</span></span>  
<span data-ttu-id="c4b30-310">Testo visualizzato in vsglog Finestra Proprietà-offset del buffer costante</span><span class="sxs-lookup"><span data-stu-id="c4b30-310">Text shown in the vsglog Properties window - Constant Buffer Offsetting</span></span>

<span data-ttu-id="c4b30-311"><span id="SUMMARYINFO_MapNoOverwriteOnDynamicConstantBuffer"></span><span id="summaryinfo_mapnooverwriteondynamicconstantbuffer"></span><span id="SUMMARYINFO_MAPNOOVERWRITEONDYNAMICCONSTANTBUFFER"></span>**\_MAPNOOVERWRITEONDYNAMICCONSTANTBUFFER SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-311"><span id="SUMMARYINFO_MapNoOverwriteOnDynamicConstantBuffer"></span><span id="summaryinfo_mapnooverwriteondynamicconstantbuffer"></span><span id="SUMMARYINFO_MAPNOOVERWRITEONDYNAMICCONSTANTBUFFER"></span>**SUMMARYINFO\_MapNoOverwriteOnDynamicConstantBuffer**</span></span>  
<span data-ttu-id="c4b30-312">Testo visualizzato in vsglog Finestra Proprietà-Map No overwrite on Dynamic constant buffer</span><span class="sxs-lookup"><span data-stu-id="c4b30-312">Text shown in the vsglog Properties window - Map No Overwrite On Dynamic Constant Buffer</span></span>

<span data-ttu-id="c4b30-313"><span id="SUMMARYINFO_MapNoOverwriteOnDynamicBufferSRV"></span><span id="summaryinfo_mapnooverwriteondynamicbuffersrv"></span><span id="SUMMARYINFO_MAPNOOVERWRITEONDYNAMICBUFFERSRV"></span>**\_MAPNOOVERWRITEONDYNAMICBUFFERSRV SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-313"><span id="SUMMARYINFO_MapNoOverwriteOnDynamicBufferSRV"></span><span id="summaryinfo_mapnooverwriteondynamicbuffersrv"></span><span id="SUMMARYINFO_MAPNOOVERWRITEONDYNAMICBUFFERSRV"></span>**SUMMARYINFO\_MapNoOverwriteOnDynamicBufferSRV**</span></span>  
<span data-ttu-id="c4b30-314">Testo visualizzato in vsglog Finestra Proprietà-Map No overwrite on Dynamic buffer SRV</span><span class="sxs-lookup"><span data-stu-id="c4b30-314">Text shown in the vsglog Properties window - Map No Overwrite On Dynamic Buffer SRV</span></span>

<span data-ttu-id="c4b30-315"><span id="SUMMARYINFO_MultisampleRTVWithForcedSampleCountOne"></span><span id="summaryinfo_multisamplertvwithforcedsamplecountone"></span><span id="SUMMARYINFO_MULTISAMPLERTVWITHFORCEDSAMPLECOUNTONE"></span>**\_MULTISAMPLERTVWITHFORCEDSAMPLECOUNTONE SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-315"><span id="SUMMARYINFO_MultisampleRTVWithForcedSampleCountOne"></span><span id="summaryinfo_multisamplertvwithforcedsamplecountone"></span><span id="SUMMARYINFO_MULTISAMPLERTVWITHFORCEDSAMPLECOUNTONE"></span>**SUMMARYINFO\_MultisampleRTVWithForcedSampleCountOne**</span></span>  
<span data-ttu-id="c4b30-316">Testo visualizzato nel vsglog Finestra Proprietà-multisample RTV con esempio forzato conteggio uno</span><span class="sxs-lookup"><span data-stu-id="c4b30-316">Text shown in the vsglog Properties window - Multisample RTV With Forced Sample Count One</span></span>

<span data-ttu-id="c4b30-317"><span id="SUMMARYINFO_SAD4ShaderInstructions"></span><span id="summaryinfo_sad4shaderinstructions"></span><span id="SUMMARYINFO_SAD4SHADERINSTRUCTIONS"></span>**\_SAD4SHADERINSTRUCTIONS SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-317"><span id="SUMMARYINFO_SAD4ShaderInstructions"></span><span id="summaryinfo_sad4shaderinstructions"></span><span id="SUMMARYINFO_SAD4SHADERINSTRUCTIONS"></span>**SUMMARYINFO\_SAD4ShaderInstructions**</span></span>  
<span data-ttu-id="c4b30-318">Testo visualizzato nelle istruzioni vsglog Finestra Proprietà-SAD4 shader</span><span class="sxs-lookup"><span data-stu-id="c4b30-318">Text shown in the vsglog Properties window - SAD4 Shader Instructions</span></span>

<span data-ttu-id="c4b30-319"><span id="SUMMARYINFO_ExtendedDoublesShaderInstructions"></span><span id="summaryinfo_extendeddoublesshaderinstructions"></span><span id="SUMMARYINFO_EXTENDEDDOUBLESSHADERINSTRUCTIONS"></span>**\_EXTENDEDDOUBLESSHADERINSTRUCTIONS SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-319"><span id="SUMMARYINFO_ExtendedDoublesShaderInstructions"></span><span id="summaryinfo_extendeddoublesshaderinstructions"></span><span id="SUMMARYINFO_EXTENDEDDOUBLESSHADERINSTRUCTIONS"></span>**SUMMARYINFO\_ExtendedDoublesShaderInstructions**</span></span>  
<span data-ttu-id="c4b30-320">Testo visualizzato nelle istruzioni vsglog Finestra Proprietà-Extended Doubles shader</span><span class="sxs-lookup"><span data-stu-id="c4b30-320">Text shown in the vsglog Properties window - Extended Doubles Shader Instructions</span></span>

<span data-ttu-id="c4b30-321"><span id="SUMMARYINFO_ExtendedResourceSharing"></span><span id="summaryinfo_extendedresourcesharing"></span><span id="SUMMARYINFO_EXTENDEDRESOURCESHARING"></span>**\_EXTENDEDRESOURCESHARING SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-321"><span id="SUMMARYINFO_ExtendedResourceSharing"></span><span id="summaryinfo_extendedresourcesharing"></span><span id="SUMMARYINFO_EXTENDEDRESOURCESHARING"></span>**SUMMARYINFO\_ExtendedResourceSharing**</span></span>  
<span data-ttu-id="c4b30-322">Testo visualizzato in vsglog Finestra Proprietà-condivisione delle risorse estesa</span><span class="sxs-lookup"><span data-stu-id="c4b30-322">Text shown in the vsglog Properties window - Extended Resource Sharing</span></span>

<span data-ttu-id="c4b30-323"><span id="SUMMARYINFO_D3D11_FEATURE_ARCHITECTURE_INFO"></span><span id="summaryinfo_d3d11_feature_architecture_info"></span>**\_Informazioni sull' \_ architettura della funzionalità d3d11 \_ di SUMMARYINFO \_**</span><span class="sxs-lookup"><span data-stu-id="c4b30-323"><span id="SUMMARYINFO_D3D11_FEATURE_ARCHITECTURE_INFO"></span><span id="summaryinfo_d3d11_feature_architecture_info"></span>**SUMMARYINFO\_D3D11\_FEATURE\_ARCHITECTURE\_INFO**</span></span>  
<span data-ttu-id="c4b30-324">Testo visualizzato nelle informazioni sull'architettura della funzionalità vsglog Finestra Proprietà-D3D11 \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="c4b30-324">Text shown in the vsglog Properties window - D3D11\_FEATURE\_ARCHITECTURE\_INFO</span></span>

<span data-ttu-id="c4b30-325"><span id="SUMMARYINFO_TileBasedDeferredRenderer"></span><span id="summaryinfo_tilebaseddeferredrenderer"></span><span id="SUMMARYINFO_TILEBASEDDEFERREDRENDERER"></span>**\_TILEBASEDDEFERREDRENDERER SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-325"><span id="SUMMARYINFO_TileBasedDeferredRenderer"></span><span id="summaryinfo_tilebaseddeferredrenderer"></span><span id="SUMMARYINFO_TILEBASEDDEFERREDRENDERER"></span>**SUMMARYINFO\_TileBasedDeferredRenderer**</span></span>  
<span data-ttu-id="c4b30-326">Testo visualizzato nel renderer posticipato di vsglog Finestra Proprietà-Tile</span><span class="sxs-lookup"><span data-stu-id="c4b30-326">Text shown in the vsglog Properties window - Tile Based Deferred Renderer</span></span>

<span data-ttu-id="c4b30-327"><span id="SUMMARYINFO_D3D11_FEATURE_D3D9_OPTIONS"></span><span id="summaryinfo_d3d11_feature_d3d9_options"></span>**\_ \_ Opzioni d3d9 della funzionalità d3d11 \_ di \_ SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-327"><span id="SUMMARYINFO_D3D11_FEATURE_D3D9_OPTIONS"></span><span id="summaryinfo_d3d11_feature_d3d9_options"></span>**SUMMARYINFO\_D3D11\_FEATURE\_D3D9\_OPTIONS**</span></span>  
<span data-ttu-id="c4b30-328">Testo visualizzato nella vsglog Finestra Proprietà-D3D11 \_ funzionalità \_ d3d9 \_ Opzioni</span><span class="sxs-lookup"><span data-stu-id="c4b30-328">Text shown in the vsglog Properties window - D3D11\_FEATURE\_D3D9\_OPTIONS</span></span>

<span data-ttu-id="c4b30-329"><span id="SUMMARYINFO_FullNonPow2TextureSupport"></span><span id="summaryinfo_fullnonpow2texturesupport"></span><span id="SUMMARYINFO_FULLNONPOW2TEXTURESUPPORT"></span>**\_FULLNONPOW2TEXTURESUPPORT SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-329"><span id="SUMMARYINFO_FullNonPow2TextureSupport"></span><span id="summaryinfo_fullnonpow2texturesupport"></span><span id="SUMMARYINFO_FULLNONPOW2TEXTURESUPPORT"></span>**SUMMARYINFO\_FullNonPow2TextureSupport**</span></span>  
<span data-ttu-id="c4b30-330">Testo visualizzato nel vsglog Finestra Proprietà-supporto della trama non Pow2 completo</span><span class="sxs-lookup"><span data-stu-id="c4b30-330">Text shown in the vsglog Properties window - Full Non-Pow2 Texture Support</span></span>

<span data-ttu-id="c4b30-331"><span id="SUMMARYINFO_D3D11_FEATURE_SHADER_MIN_PRECISION_SUPPORT"></span><span id="summaryinfo_d3d11_feature_shader_min_precision_support"></span>**Supporto per la precisione di SUMMARYINFO \_ d3d11 \_ feature \_ shader \_ Min \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c4b30-331"><span id="SUMMARYINFO_D3D11_FEATURE_SHADER_MIN_PRECISION_SUPPORT"></span><span id="summaryinfo_d3d11_feature_shader_min_precision_support"></span>**SUMMARYINFO\_D3D11\_FEATURE\_SHADER\_MIN\_PRECISION\_SUPPORT**</span></span>  
<span data-ttu-id="c4b30-332">Testo visualizzato in vsglog Finestra Proprietà-D3D11 \_ feature \_ shader \_ Min \_ Precision \_ support</span><span class="sxs-lookup"><span data-stu-id="c4b30-332">Text shown in the vsglog Properties window - D3D11\_FEATURE\_SHADER\_MIN\_PRECISION\_SUPPORT</span></span>

<span data-ttu-id="c4b30-333"><span id="SUMMARYINFO_PixelShaderMinPrecision"></span><span id="summaryinfo_pixelshaderminprecision"></span><span id="SUMMARYINFO_PIXELSHADERMINPRECISION"></span>**\_PIXELSHADERMINPRECISION SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-333"><span id="SUMMARYINFO_PixelShaderMinPrecision"></span><span id="summaryinfo_pixelshaderminprecision"></span><span id="SUMMARYINFO_PIXELSHADERMINPRECISION"></span>**SUMMARYINFO\_PixelShaderMinPrecision**</span></span>  
<span data-ttu-id="c4b30-334">Testo visualizzato in vsglog Finestra Proprietà-pixel shader min Precision</span><span class="sxs-lookup"><span data-stu-id="c4b30-334">Text shown in the vsglog Properties window - Pixel Shader Min Precision</span></span>

<span data-ttu-id="c4b30-335"><span id="SUMMARYINFO_AllOtherShaderStagesMinPrecision"></span><span id="summaryinfo_allothershaderstagesminprecision"></span><span id="SUMMARYINFO_ALLOTHERSHADERSTAGESMINPRECISION"></span>**\_ALLOTHERSHADERSTAGESMINPRECISION SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-335"><span id="SUMMARYINFO_AllOtherShaderStagesMinPrecision"></span><span id="summaryinfo_allothershaderstagesminprecision"></span><span id="SUMMARYINFO_ALLOTHERSHADERSTAGESMINPRECISION"></span>**SUMMARYINFO\_AllOtherShaderStagesMinPrecision**</span></span>  
<span data-ttu-id="c4b30-336">Testo visualizzato in vsglog Finestra Proprietà-tutti gli altri stadi di shader con precisione minima</span><span class="sxs-lookup"><span data-stu-id="c4b30-336">Text shown in the vsglog Properties window - All Other Shader Stages Min Precision</span></span>

<span data-ttu-id="c4b30-337"><span id="SUMMARYINFO_D3D11_FEATURE_D3D9_SHADOW_SUPPORT"></span><span id="summaryinfo_d3d11_feature_d3d9_shadow_support"></span>**\_Supporto di \_ \_ shadow d3d9 \_ per la funzionalità d3d11 di \_ SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-337"><span id="SUMMARYINFO_D3D11_FEATURE_D3D9_SHADOW_SUPPORT"></span><span id="summaryinfo_d3d11_feature_d3d9_shadow_support"></span>**SUMMARYINFO\_D3D11\_FEATURE\_D3D9\_SHADOW\_SUPPORT**</span></span>  
<span data-ttu-id="c4b30-338">Testo visualizzato nella funzionalità vsglog Finestra Proprietà-D3D11 \_ \_ d3d9 \_ shadow \_ support</span><span class="sxs-lookup"><span data-stu-id="c4b30-338">Text shown in the vsglog Properties window - D3D11\_FEATURE\_D3D9\_SHADOW\_SUPPORT</span></span>

<span data-ttu-id="c4b30-339"><span id="SUMMARYINFO_SupportsDepthAsTextureWithLessEqualComparisonFilter"></span><span id="summaryinfo_supportsdepthastexturewithlessequalcomparisonfilter"></span><span id="SUMMARYINFO_SUPPORTSDEPTHASTEXTUREWITHLESSEQUALCOMPARISONFILTER"></span>**\_SUPPORTSDEPTHASTEXTUREWITHLESSEQUALCOMPARISONFILTER SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-339"><span id="SUMMARYINFO_SupportsDepthAsTextureWithLessEqualComparisonFilter"></span><span id="summaryinfo_supportsdepthastexturewithlessequalcomparisonfilter"></span><span id="SUMMARYINFO_SUPPORTSDEPTHASTEXTUREWITHLESSEQUALCOMPARISONFILTER"></span>**SUMMARYINFO\_SupportsDepthAsTextureWithLessEqualComparisonFilter**</span></span>  
<span data-ttu-id="c4b30-340">Testo visualizzato in vsglog Finestra Proprietà-supporta la profondità come trama con un filtro di confronto meno uguale</span><span class="sxs-lookup"><span data-stu-id="c4b30-340">Text shown in the vsglog Properties window - Supports Depth As Texture With Less Equal Comparison Filter</span></span>

<span data-ttu-id="c4b30-341"><span id="SUMMARYINFO_D3D11_FEATURE_D3D11_OPTIONS1"></span><span id="summaryinfo_d3d11_feature_d3d11_options1"></span>**SUMMARYINFO \_ d3d11 \_ feature \_ d3d11 \_ OPTIONS1**</span><span class="sxs-lookup"><span data-stu-id="c4b30-341"><span id="SUMMARYINFO_D3D11_FEATURE_D3D11_OPTIONS1"></span><span id="summaryinfo_d3d11_feature_d3d11_options1"></span>**SUMMARYINFO\_D3D11\_FEATURE\_D3D11\_OPTIONS1**</span></span>  
<span data-ttu-id="c4b30-342">Testo visualizzato nella funzionalità vsglog Finestra Proprietà-D3D11 \_ \_ d3d11 \_ OPTIONS1</span><span class="sxs-lookup"><span data-stu-id="c4b30-342">Text shown in the vsglog Properties window - D3D11\_FEATURE\_D3D11\_OPTIONS1</span></span>

<span data-ttu-id="c4b30-343"><span id="SUMMARYINFO_TiledResourcesTier"></span><span id="summaryinfo_tiledresourcestier"></span><span id="SUMMARYINFO_TILEDRESOURCESTIER"></span>**\_TILEDRESOURCESTIER SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-343"><span id="SUMMARYINFO_TiledResourcesTier"></span><span id="summaryinfo_tiledresourcestier"></span><span id="SUMMARYINFO_TILEDRESOURCESTIER"></span>**SUMMARYINFO\_TiledResourcesTier**</span></span>  
<span data-ttu-id="c4b30-344">Testo visualizzato nel vsglog Finestra Proprietà-livello di risorse affiancato</span><span class="sxs-lookup"><span data-stu-id="c4b30-344">Text shown in the vsglog Properties window - Tiled Resources Tier</span></span>

<span data-ttu-id="c4b30-345"><span id="SUMMARYINFO_MinMaxFiltering"></span><span id="summaryinfo_minmaxfiltering"></span><span id="SUMMARYINFO_MINMAXFILTERING"></span>**\_MINMAXFILTERING SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-345"><span id="SUMMARYINFO_MinMaxFiltering"></span><span id="summaryinfo_minmaxfiltering"></span><span id="SUMMARYINFO_MINMAXFILTERING"></span>**SUMMARYINFO\_MinMaxFiltering**</span></span>  
<span data-ttu-id="c4b30-346">Testo visualizzato nel vsglog Finestra Proprietà-min max Filtering</span><span class="sxs-lookup"><span data-stu-id="c4b30-346">Text shown in the vsglog Properties window - Min Max Filtering</span></span>

<span data-ttu-id="c4b30-347"><span id="SUMMARYINFO_ClearViewAlsoSupportsDepthOnlyFormats"></span><span id="summaryinfo_clearviewalsosupportsdepthonlyformats"></span><span id="SUMMARYINFO_CLEARVIEWALSOSUPPORTSDEPTHONLYFORMATS"></span>**\_CLEARVIEWALSOSUPPORTSDEPTHONLYFORMATS SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-347"><span id="SUMMARYINFO_ClearViewAlsoSupportsDepthOnlyFormats"></span><span id="summaryinfo_clearviewalsosupportsdepthonlyformats"></span><span id="SUMMARYINFO_CLEARVIEWALSOSUPPORTSDEPTHONLYFORMATS"></span>**SUMMARYINFO\_ClearViewAlsoSupportsDepthOnlyFormats**</span></span>  
<span data-ttu-id="c4b30-348">Il testo visualizzato nella vsglog Finestra Proprietà-Clear View supporta anche formati di profondità</span><span class="sxs-lookup"><span data-stu-id="c4b30-348">Text shown in the vsglog Properties window - Clear View Also Supports Depth Only Formats</span></span>

<span data-ttu-id="c4b30-349"><span id="SUMMARYINFO_MapOnDefaultBuffers"></span><span id="summaryinfo_mapondefaultbuffers"></span><span id="SUMMARYINFO_MAPONDEFAULTBUFFERS"></span>**\_MAPONDEFAULTBUFFERS SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-349"><span id="SUMMARYINFO_MapOnDefaultBuffers"></span><span id="summaryinfo_mapondefaultbuffers"></span><span id="SUMMARYINFO_MAPONDEFAULTBUFFERS"></span>**SUMMARYINFO\_MapOnDefaultBuffers**</span></span>  
<span data-ttu-id="c4b30-350">Testo visualizzato in vsglog Finestra Proprietà-Map sui buffer predefiniti</span><span class="sxs-lookup"><span data-stu-id="c4b30-350">Text shown in the vsglog Properties window - Map On Default Buffers</span></span>

<span data-ttu-id="c4b30-351"><span id="SUMMARYINFO_D3D11_FEATURE_D3D9_SIMPLE_INSTANCING_SUPPORT"></span><span id="summaryinfo_d3d11_feature_d3d9_simple_instancing_support"></span>**SUMMARYINFO \_ d3d11 \_ funzionalità \_ d3d9 \_ \_ supporto per istanze semplici \_**</span><span class="sxs-lookup"><span data-stu-id="c4b30-351"><span id="SUMMARYINFO_D3D11_FEATURE_D3D9_SIMPLE_INSTANCING_SUPPORT"></span><span id="summaryinfo_d3d11_feature_d3d9_simple_instancing_support"></span>**SUMMARYINFO\_D3D11\_FEATURE\_D3D9\_SIMPLE\_INSTANCING\_SUPPORT**</span></span>  
<span data-ttu-id="c4b30-352">Testo visualizzato nella vsglog Finestra Proprietà-D3D11 \_ funzionalità \_ d3d9 \_ supporto per \_ istanze \_ semplici</span><span class="sxs-lookup"><span data-stu-id="c4b30-352">Text shown in the vsglog Properties window - D3D11\_FEATURE\_D3D9\_SIMPLE\_INSTANCING\_SUPPORT</span></span>

<span data-ttu-id="c4b30-353"><span id="SUMMARYINFO_SimpleInstancingSupported0"></span><span id="summaryinfo_simpleinstancingsupported0"></span><span id="SUMMARYINFO_SIMPLEINSTANCINGSUPPORTED0"></span>**\_SIMPLEINSTANCINGSUPPORTED0 SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-353"><span id="SUMMARYINFO_SimpleInstancingSupported0"></span><span id="summaryinfo_simpleinstancingsupported0"></span><span id="SUMMARYINFO_SIMPLEINSTANCINGSUPPORTED0"></span>**SUMMARYINFO\_SimpleInstancingSupported0**</span></span>  
<span data-ttu-id="c4b30-354">Testo visualizzato in vsglog Finestra Proprietà-l'istanza semplice supporta 0</span><span class="sxs-lookup"><span data-stu-id="c4b30-354">Text shown in the vsglog Properties window - Simple Instancing Supported 0</span></span>

<span data-ttu-id="c4b30-355"><span id="SUMMARYINFO_D3D11_FEATURE_MARKER_SUPPORT"></span><span id="summaryinfo_d3d11_feature_marker_support"></span>**\_Supporto del \_ \_ marcatore funzionalità d3d11 \_ SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-355"><span id="SUMMARYINFO_D3D11_FEATURE_MARKER_SUPPORT"></span><span id="summaryinfo_d3d11_feature_marker_support"></span>**SUMMARYINFO\_D3D11\_FEATURE\_MARKER\_SUPPORT**</span></span>  
<span data-ttu-id="c4b30-356">Testo visualizzato in vsglog Finestra Proprietà-D3D11 \_ feature \_ marker \_ support</span><span class="sxs-lookup"><span data-stu-id="c4b30-356">Text shown in the vsglog Properties window - D3D11\_FEATURE\_MARKER\_SUPPORT</span></span>

<span data-ttu-id="c4b30-357"><span id="SUMMARYINFO_Profile"></span><span id="summaryinfo_profile"></span><span id="SUMMARYINFO_PROFILE"></span>**\_Profilo SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-357"><span id="SUMMARYINFO_Profile"></span><span id="summaryinfo_profile"></span><span id="SUMMARYINFO_PROFILE"></span>**SUMMARYINFO\_Profile**</span></span>  
<span data-ttu-id="c4b30-358">Testo visualizzato in vsglog Finestra Proprietà-profile</span><span class="sxs-lookup"><span data-stu-id="c4b30-358">Text shown in the vsglog Properties window - Profile</span></span>

<span data-ttu-id="c4b30-359"><span id="SUMMARYINFO_D3D11_FEATURE_D3D9_OPTIONS1"></span><span id="summaryinfo_d3d11_feature_d3d9_options1"></span>**SUMMARYINFO \_ d3d11 \_ feature \_ d3d9 \_ OPTIONS1**</span><span class="sxs-lookup"><span data-stu-id="c4b30-359"><span id="SUMMARYINFO_D3D11_FEATURE_D3D9_OPTIONS1"></span><span id="summaryinfo_d3d11_feature_d3d9_options1"></span>**SUMMARYINFO\_D3D11\_FEATURE\_D3D9\_OPTIONS1**</span></span>  
<span data-ttu-id="c4b30-360">Testo visualizzato nella funzionalità vsglog Finestra Proprietà-D3D11 \_ \_ d3d9 \_ OPTIONS1</span><span class="sxs-lookup"><span data-stu-id="c4b30-360">Text shown in the vsglog Properties window - D3D11\_FEATURE\_D3D9\_OPTIONS1</span></span>

<span data-ttu-id="c4b30-361"><span id="SUMMARYINFO_FullNonPow2TextureSupported"></span><span id="summaryinfo_fullnonpow2texturesupported"></span><span id="SUMMARYINFO_FULLNONPOW2TEXTURESUPPORTED"></span>**\_FULLNONPOW2TEXTURESUPPORTED SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-361"><span id="SUMMARYINFO_FullNonPow2TextureSupported"></span><span id="summaryinfo_fullnonpow2texturesupported"></span><span id="SUMMARYINFO_FULLNONPOW2TEXTURESUPPORTED"></span>**SUMMARYINFO\_FullNonPow2TextureSupported**</span></span>  
<span data-ttu-id="c4b30-362">Testo visualizzato in vsglog Finestra Proprietà-trama non Pow2 completa supportata</span><span class="sxs-lookup"><span data-stu-id="c4b30-362">Text shown in the vsglog Properties window - Full Non-Pow2 Texture Supported</span></span>

<span data-ttu-id="c4b30-363"><span id="SUMMARYINFO_DepthAsTextureWithLessEqualComparisonFilterSupported"></span><span id="summaryinfo_depthastexturewithlessequalcomparisonfiltersupported"></span><span id="SUMMARYINFO_DEPTHASTEXTUREWITHLESSEQUALCOMPARISONFILTERSUPPORTED"></span>**\_DEPTHASTEXTUREWITHLESSEQUALCOMPARISONFILTERSUPPORTED SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-363"><span id="SUMMARYINFO_DepthAsTextureWithLessEqualComparisonFilterSupported"></span><span id="summaryinfo_depthastexturewithlessequalcomparisonfiltersupported"></span><span id="SUMMARYINFO_DEPTHASTEXTUREWITHLESSEQUALCOMPARISONFILTERSUPPORTED"></span>**SUMMARYINFO\_DepthAsTextureWithLessEqualComparisonFilterSupported**</span></span>  
<span data-ttu-id="c4b30-364">Testo visualizzato in vsglog Finestra Proprietà-Depth come trama con filtro di confronto meno uguale supportato</span><span class="sxs-lookup"><span data-stu-id="c4b30-364">Text shown in the vsglog Properties window - Depth As Texture With Less Equal Comparison Filter Supported</span></span>

<span data-ttu-id="c4b30-365"><span id="SUMMARYINFO_SimpleInstancingSupported1"></span><span id="summaryinfo_simpleinstancingsupported1"></span><span id="SUMMARYINFO_SIMPLEINSTANCINGSUPPORTED1"></span>**\_SIMPLEINSTANCINGSUPPORTED1 SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-365"><span id="SUMMARYINFO_SimpleInstancingSupported1"></span><span id="summaryinfo_simpleinstancingsupported1"></span><span id="SUMMARYINFO_SIMPLEINSTANCINGSUPPORTED1"></span>**SUMMARYINFO\_SimpleInstancingSupported1**</span></span>  
<span data-ttu-id="c4b30-366">Testo visualizzato in vsglog Finestra Proprietà-istanza semplice supportata 1</span><span class="sxs-lookup"><span data-stu-id="c4b30-366">Text shown in the vsglog Properties window - Simple Instancing Supported 1</span></span>

<span data-ttu-id="c4b30-367"><span id="SUMMARYINFO_TextureCubeFaceRenderTargetWithNonCubeDepthStencilSupported"></span><span id="summaryinfo_texturecubefacerendertargetwithnoncubedepthstencilsupported"></span><span id="SUMMARYINFO_TEXTURECUBEFACERENDERTARGETWITHNONCUBEDEPTHSTENCILSUPPORTED"></span>**\_TEXTURECUBEFACERENDERTARGETWITHNONCUBEDEPTHSTENCILSUPPORTED SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-367"><span id="SUMMARYINFO_TextureCubeFaceRenderTargetWithNonCubeDepthStencilSupported"></span><span id="summaryinfo_texturecubefacerendertargetwithnoncubedepthstencilsupported"></span><span id="SUMMARYINFO_TEXTURECUBEFACERENDERTARGETWITHNONCUBEDEPTHSTENCILSUPPORTED"></span>**SUMMARYINFO\_TextureCubeFaceRenderTargetWithNonCubeDepthStencilSupported**</span></span>  
<span data-ttu-id="c4b30-368">Testo visualizzato nella destinazione di rendering del vsglog Finestra Proprietà-texture del cubo con stencil profondità non cubo supportato</span><span class="sxs-lookup"><span data-stu-id="c4b30-368">Text shown in the vsglog Properties window - Texture Cube Face Render Target With Non-Cube Depth Stencil Supported</span></span>

<span data-ttu-id="c4b30-369"><span id="SUMMARYINFO_DXGIFormat"></span><span id="summaryinfo_dxgiformat"></span><span id="SUMMARYINFO_DXGIFORMAT"></span>**\_DXGIFORMAT SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-369"><span id="SUMMARYINFO_DXGIFormat"></span><span id="summaryinfo_dxgiformat"></span><span id="SUMMARYINFO_DXGIFORMAT"></span>**SUMMARYINFO\_DXGIFormat**</span></span>  
<span data-ttu-id="c4b30-370">Testo visualizzato in vsglog Finestra Proprietà-DXGIFormat</span><span class="sxs-lookup"><span data-stu-id="c4b30-370">Text shown in the vsglog Properties window - DXGIFormat</span></span>

<span data-ttu-id="c4b30-371"><span id="SUMMARYINFO_DXGIFormat1"></span><span id="summaryinfo_dxgiformat1"></span><span id="SUMMARYINFO_DXGIFORMAT1"></span>**\_DXGIFORMAT1 SUMMARYINFO**</span><span class="sxs-lookup"><span data-stu-id="c4b30-371"><span id="SUMMARYINFO_DXGIFormat1"></span><span id="summaryinfo_dxgiformat1"></span><span id="SUMMARYINFO_DXGIFORMAT1"></span>**SUMMARYINFO\_DXGIFormat1**</span></span>  
<span data-ttu-id="c4b30-372">Testo visualizzato in vsglog Finestra Proprietà-DXGIFormat1</span><span class="sxs-lookup"><span data-stu-id="c4b30-372">Text shown in the vsglog Properties window - DXGIFormat1</span></span>

<span data-ttu-id="c4b30-373"><span id="SUMMARYINFO_MODULENAME"></span><span id="summaryinfo_modulename"></span>**SUMMARYINFO \_ ModuleName**</span><span class="sxs-lookup"><span data-stu-id="c4b30-373"><span id="SUMMARYINFO_MODULENAME"></span><span id="summaryinfo_modulename"></span>**SUMMARYINFO\_MODULENAME**</span></span>  
<span data-ttu-id="c4b30-374">Testo visualizzato in vsglog Finestra Proprietà-MODULEname</span><span class="sxs-lookup"><span data-stu-id="c4b30-374">Text shown in the vsglog Properties window - MODULENAME</span></span>

<span data-ttu-id="c4b30-375"><span id="IDD_CONFIGURATION"></span><span id="idd_configuration"></span>**\_configurazione IDD**</span><span class="sxs-lookup"><span data-stu-id="c4b30-375"><span id="IDD_CONFIGURATION"></span><span id="idd_configuration"></span>**IDD\_CONFIGURATION**</span></span>  
<span data-ttu-id="c4b30-376">Testo visualizzato nella finestra di dialogo Configura firewall in VsGraphicsRemoteEngine</span><span class="sxs-lookup"><span data-stu-id="c4b30-376">Text shown in the Configure Firewall dialog in the VsGraphicsRemoteEngine</span></span>

<span data-ttu-id="c4b30-377"><span id="IDC_STATIC_HEADER_ICON"></span><span id="idc_static_header_icon"></span>**\_icona dell' \_ intestazione \_ statica IDC**</span><span class="sxs-lookup"><span data-stu-id="c4b30-377"><span id="IDC_STATIC_HEADER_ICON"></span><span id="idc_static_header_icon"></span>**IDC\_STATIC\_HEADER\_ICON**</span></span>  
<span data-ttu-id="c4b30-378">Testo visualizzato nell'icona di configurazione del controllo della finestra di dialogo Configura firewall-intestazione statica</span><span class="sxs-lookup"><span data-stu-id="c4b30-378">Text shown in the Configure Firewall dialog control - Static Header Icon</span></span>

<span data-ttu-id="c4b30-379"><span id="IDC_STATIC_HEADER"></span><span id="idc_static_header"></span>**\_intestazione statica \_ IDC**</span><span class="sxs-lookup"><span data-stu-id="c4b30-379"><span id="IDC_STATIC_HEADER"></span><span id="idc_static_header"></span>**IDC\_STATIC\_HEADER**</span></span>  
<span data-ttu-id="c4b30-380">Testo visualizzato nell'intestazione del controllo della finestra di dialogo Configura firewall</span><span class="sxs-lookup"><span data-stu-id="c4b30-380">Text shown in the Configure Firewall dialog control - Static Header</span></span>

<span data-ttu-id="c4b30-381"><span id="IDC_STATIC_FW_CONFIGURATION"></span><span id="idc_static_fw_configuration"></span>**\_ \_ configurazione FW statica \_ IDC**</span><span class="sxs-lookup"><span data-stu-id="c4b30-381"><span id="IDC_STATIC_FW_CONFIGURATION"></span><span id="idc_static_fw_configuration"></span>**IDC\_STATIC\_FW\_CONFIGURATION**</span></span>  
<span data-ttu-id="c4b30-382">Testo visualizzato nella configurazione del controllo della finestra di dialogo Configura firewall-configurazione del firewall statico</span><span class="sxs-lookup"><span data-stu-id="c4b30-382">Text shown in the Configure Firewall dialog control - Static Firewall Configuration</span></span>

<span data-ttu-id="c4b30-383"><span id="IDC_STATIC_FW_ICON"></span><span id="idc_static_fw_icon"></span>**\_icona del \_ FW \_ statico IDC**</span><span class="sxs-lookup"><span data-stu-id="c4b30-383"><span id="IDC_STATIC_FW_ICON"></span><span id="idc_static_fw_icon"></span>**IDC\_STATIC\_FW\_ICON**</span></span>  
<span data-ttu-id="c4b30-384">Testo visualizzato nell'icona del controllo della finestra di dialogo Configura firewall-icona del firewall statico</span><span class="sxs-lookup"><span data-stu-id="c4b30-384">Text shown in the Configure Firewall dialog control - Static Firewall Icon</span></span>

<span data-ttu-id="c4b30-385"><span id="IDC_STATIC_FW_HEADER"></span><span id="idc_static_fw_header"></span>**\_ \_ intestazione FW statica \_ IDC**</span><span class="sxs-lookup"><span data-stu-id="c4b30-385"><span id="IDC_STATIC_FW_HEADER"></span><span id="idc_static_fw_header"></span>**IDC\_STATIC\_FW\_HEADER**</span></span>  
<span data-ttu-id="c4b30-386">Testo visualizzato nell'intestazione del controllo della finestra di dialogo Configura firewall-static firewall</span><span class="sxs-lookup"><span data-stu-id="c4b30-386">Text shown in the Configure Firewall dialog control - Static Firewall Header</span></span>

<span data-ttu-id="c4b30-387"><span id="IDC_STATIC_GROUPBOX_FW"></span><span id="idc_static_groupbox_fw"></span>**\_ \_ FW GroupBox statico di IDC \_**</span><span class="sxs-lookup"><span data-stu-id="c4b30-387"><span id="IDC_STATIC_GROUPBOX_FW"></span><span id="idc_static_groupbox_fw"></span>**IDC\_STATIC\_GROUPBOX\_FW**</span></span>  
<span data-ttu-id="c4b30-388">Testo visualizzato nella finestra di dialogo Configura controllo della finestra di dialogo-firewall statico GroupBox</span><span class="sxs-lookup"><span data-stu-id="c4b30-388">Text shown in the Configure Firewall dialog control - Static Groupbox Firewall</span></span>

<span data-ttu-id="c4b30-389"><span id="IDC_CHECK_FW_DOMAIN_NETWORKS"></span><span id="idc_check_fw_domain_networks"></span>**\_controllo IDC \_ \_ reti di dominio FW \_**</span><span class="sxs-lookup"><span data-stu-id="c4b30-389"><span id="IDC_CHECK_FW_DOMAIN_NETWORKS"></span><span id="idc_check_fw_domain_networks"></span>**IDC\_CHECK\_FW\_DOMAIN\_NETWORKS**</span></span>  
<span data-ttu-id="c4b30-390">Testo visualizzato nel controllo della finestra di dialogo Configura firewall-controlla reti di dominio firewall</span><span class="sxs-lookup"><span data-stu-id="c4b30-390">Text shown in the Configure Firewall dialog control - Check Firewall Domain Networks</span></span>

<span data-ttu-id="c4b30-391"><span id="IDC_CHECK_FW_PRIVATE_NETWORKS"></span><span id="idc_check_fw_private_networks"></span>**\_controllo IDC \_ \_ reti private \_ FW**</span><span class="sxs-lookup"><span data-stu-id="c4b30-391"><span id="IDC_CHECK_FW_PRIVATE_NETWORKS"></span><span id="idc_check_fw_private_networks"></span>**IDC\_CHECK\_FW\_PRIVATE\_NETWORKS**</span></span>  
<span data-ttu-id="c4b30-392">Testo visualizzato nel controllo della finestra di dialogo Configura firewall-controlla reti private firewall</span><span class="sxs-lookup"><span data-stu-id="c4b30-392">Text shown in the Configure Firewall dialog control - Check Firewall Private Networks</span></span>

<span data-ttu-id="c4b30-393"><span id="IDC_CHECK_FW_PUBLIC_NETWORKS"></span><span id="idc_check_fw_public_networks"></span>**\_controllo IDC \_ \_ reti pubbliche \_ FW**</span><span class="sxs-lookup"><span data-stu-id="c4b30-393"><span id="IDC_CHECK_FW_PUBLIC_NETWORKS"></span><span id="idc_check_fw_public_networks"></span>**IDC\_CHECK\_FW\_PUBLIC\_NETWORKS**</span></span>  
<span data-ttu-id="c4b30-394">Testo visualizzato nel controllo della finestra di dialogo Configura firewall-controlla reti pubbliche firewall</span><span class="sxs-lookup"><span data-stu-id="c4b30-394">Text shown in the Configure Firewall dialog control - Check Firewall Public Networks</span></span>

<span data-ttu-id="c4b30-395"><span id="IDC_BUTTON_CONFIGURE"></span><span id="idc_button_configure"></span>**\_pulsante IDC \_ configurare**</span><span class="sxs-lookup"><span data-stu-id="c4b30-395"><span id="IDC_BUTTON_CONFIGURE"></span><span id="idc_button_configure"></span>**IDC\_BUTTON\_CONFIGURE**</span></span>  
<span data-ttu-id="c4b30-396">Testo visualizzato nel configurare il controllo della finestra di dialogo del firewall-pulsante Configura</span><span class="sxs-lookup"><span data-stu-id="c4b30-396">Text shown in the Configure Firewall dialog control - Button Configure</span></span>

<span data-ttu-id="c4b30-397"><span id="ID_CONFIGURATION_CANCEL"></span><span id="id_configuration_cancel"></span>**\_annullamento configurazione \_ ID**</span><span class="sxs-lookup"><span data-stu-id="c4b30-397"><span id="ID_CONFIGURATION_CANCEL"></span><span id="id_configuration_cancel"></span>**ID\_CONFIGURATION\_CANCEL**</span></span>  
<span data-ttu-id="c4b30-398">Testo visualizzato nel controllo della finestra di dialogo Configura firewall-Annulla configurazione</span><span class="sxs-lookup"><span data-stu-id="c4b30-398">Text shown in the Configure Firewall dialog control - Configuration Cancel</span></span>

<span data-ttu-id="c4b30-399"><span id="IDS_TEXT_FW_NOT_CONFIGURED"></span><span id="ids_text_fw_not_configured"></span>**ID \_ testo \_ FW \_ non \_ configurato**</span><span class="sxs-lookup"><span data-stu-id="c4b30-399"><span id="IDS_TEXT_FW_NOT_CONFIGURED"></span><span id="ids_text_fw_not_configured"></span>**IDS\_TEXT\_FW\_NOT\_CONFIGURED**</span></span>  
<span data-ttu-id="c4b30-400">Testo visualizzato nella finestra di dialogo Configura firewall-firewall del testo non configurato</span><span class="sxs-lookup"><span data-stu-id="c4b30-400">Text shown in the Configure Firewall dialog - Text Firewall Not Configured</span></span>

<span data-ttu-id="c4b30-401"><span id="IDS_TEXT_FW_CONFIGURED"></span><span id="ids_text_fw_configured"></span>**ID \_ testo \_ FW \_ configurato**</span><span class="sxs-lookup"><span data-stu-id="c4b30-401"><span id="IDS_TEXT_FW_CONFIGURED"></span><span id="ids_text_fw_configured"></span>**IDS\_TEXT\_FW\_CONFIGURED**</span></span>  
<span data-ttu-id="c4b30-402">Testo visualizzato nella finestra di dialogo Configura firewall-firewall del testo configurato</span><span class="sxs-lookup"><span data-stu-id="c4b30-402">Text shown in the Configure Firewall dialog - Text Firewall Configured</span></span>

<span data-ttu-id="c4b30-403"><span id="IDS_FIREWALL_RULE_NAME"></span><span id="ids_firewall_rule_name"></span>**\_nome della \_ regola del firewall ID \_**</span><span class="sxs-lookup"><span data-stu-id="c4b30-403"><span id="IDS_FIREWALL_RULE_NAME"></span><span id="ids_firewall_rule_name"></span>**IDS\_FIREWALL\_RULE\_NAME**</span></span>  
<span data-ttu-id="c4b30-404">Testo visualizzato nella finestra di dialogo Configura firewall-nome regola firewall</span><span class="sxs-lookup"><span data-stu-id="c4b30-404">Text shown in the Configure Firewall dialog - Firewall Rule Name</span></span>

<span data-ttu-id="c4b30-405"><span id="IDS_FIREWALL_RULE_DESCRIPTION"></span><span id="ids_firewall_rule_description"></span>**\_Descrizione della \_ regola del firewall ID \_**</span><span class="sxs-lookup"><span data-stu-id="c4b30-405"><span id="IDS_FIREWALL_RULE_DESCRIPTION"></span><span id="ids_firewall_rule_description"></span>**IDS\_FIREWALL\_RULE\_DESCRIPTION**</span></span>  
<span data-ttu-id="c4b30-406">Testo visualizzato nella finestra di dialogo Configura Firewall-Descrizione regola firewall</span><span class="sxs-lookup"><span data-stu-id="c4b30-406">Text shown in the Configure Firewall dialog - Firewall Rule Description</span></span>

<span data-ttu-id="c4b30-407"><span id="IDS_STATIC_HEADER"></span><span id="ids_static_header"></span>**\_intestazione statica \_ ID**</span><span class="sxs-lookup"><span data-stu-id="c4b30-407"><span id="IDS_STATIC_HEADER"></span><span id="ids_static_header"></span>**IDS\_STATIC\_HEADER**</span></span>  
<span data-ttu-id="c4b30-408">Testo visualizzato nella finestra di dialogo Configura firewall-intestazione statica</span><span class="sxs-lookup"><span data-stu-id="c4b30-408">Text shown in the Configure Firewall dialog - Static Header</span></span>

<span data-ttu-id="c4b30-409"><span id="IDS_CONFIGURATION_TITLE"></span><span id="ids_configuration_title"></span>**\_titolo configurazione \_ ID**</span><span class="sxs-lookup"><span data-stu-id="c4b30-409"><span id="IDS_CONFIGURATION_TITLE"></span><span id="ids_configuration_title"></span>**IDS\_CONFIGURATION\_TITLE**</span></span>  
<span data-ttu-id="c4b30-410">Testo visualizzato nella finestra di dialogo Configura firewall-titolo configurazione</span><span class="sxs-lookup"><span data-stu-id="c4b30-410">Text shown in the Configure Firewall dialog - Configuration Title</span></span>

<span data-ttu-id="c4b30-411"><span id="IDS_STATIC_FW_HEADER"></span><span id="ids_static_fw_header"></span>**\_ \_ intestazione FW statica \_ ID**</span><span class="sxs-lookup"><span data-stu-id="c4b30-411"><span id="IDS_STATIC_FW_HEADER"></span><span id="ids_static_fw_header"></span>**IDS\_STATIC\_FW\_HEADER**</span></span>  
<span data-ttu-id="c4b30-412">Testo visualizzato nella finestra di dialogo Configura firewall-intestazione del firewall statico</span><span class="sxs-lookup"><span data-stu-id="c4b30-412">Text shown in the Configure Firewall dialog - Static Firewall Header</span></span>

<span data-ttu-id="c4b30-413"><span id="IDS_STATIC_GROUPBOX_FW"></span><span id="ids_static_groupbox_fw"></span>**ID \_ \_ GroupBox statico \_**</span><span class="sxs-lookup"><span data-stu-id="c4b30-413"><span id="IDS_STATIC_GROUPBOX_FW"></span><span id="ids_static_groupbox_fw"></span>**IDS\_STATIC\_GROUPBOX\_FW**</span></span>  
<span data-ttu-id="c4b30-414">Testo visualizzato nella finestra di dialogo Configura firewall-firewall GroupBox statico</span><span class="sxs-lookup"><span data-stu-id="c4b30-414">Text shown in the Configure Firewall dialog - Static Groupbox Firewall</span></span>

<span data-ttu-id="c4b30-415"><span id="IDS_CHECK_FW_DOMAIN_NETWORKS"></span><span id="ids_check_fw_domain_networks"></span>**ID \_ controllare \_ le \_ reti di dominio FW \_**</span><span class="sxs-lookup"><span data-stu-id="c4b30-415"><span id="IDS_CHECK_FW_DOMAIN_NETWORKS"></span><span id="ids_check_fw_domain_networks"></span>**IDS\_CHECK\_FW\_DOMAIN\_NETWORKS**</span></span>  
<span data-ttu-id="c4b30-416">Testo visualizzato nella finestra di dialogo Configura firewall-controlla reti di dominio firewall</span><span class="sxs-lookup"><span data-stu-id="c4b30-416">Text shown in the Configure Firewall dialog - Check Firewall Domain Networks</span></span>

<span data-ttu-id="c4b30-417"><span id="IDS_CHECK_FW_PRIVATE_NETWORKS"></span><span id="ids_check_fw_private_networks"></span>**ID \_ controlla \_ \_ reti private \_ FW**</span><span class="sxs-lookup"><span data-stu-id="c4b30-417"><span id="IDS_CHECK_FW_PRIVATE_NETWORKS"></span><span id="ids_check_fw_private_networks"></span>**IDS\_CHECK\_FW\_PRIVATE\_NETWORKS**</span></span>  
<span data-ttu-id="c4b30-418">Testo visualizzato nella finestra di dialogo Configura firewall-controlla reti private firewall</span><span class="sxs-lookup"><span data-stu-id="c4b30-418">Text shown in the Configure Firewall dialog - Check Firewall Private Networks</span></span>

<span data-ttu-id="c4b30-419"><span id="IDS_CHECK_FW_PUBLIC_NETWORKS"></span><span id="ids_check_fw_public_networks"></span>**ID \_ controlla \_ \_ reti pubbliche \_ FW**</span><span class="sxs-lookup"><span data-stu-id="c4b30-419"><span id="IDS_CHECK_FW_PUBLIC_NETWORKS"></span><span id="ids_check_fw_public_networks"></span>**IDS\_CHECK\_FW\_PUBLIC\_NETWORKS**</span></span>  
<span data-ttu-id="c4b30-420">Testo visualizzato nella finestra di dialogo Configura firewall-controlla reti pubbliche firewall</span><span class="sxs-lookup"><span data-stu-id="c4b30-420">Text shown in the Configure Firewall dialog - Check Firewall public Networks</span></span>

<span data-ttu-id="c4b30-421"><span id="IDS_BUTTON_CONFIGURE"></span><span id="ids_button_configure"></span>**pulsante ID- \_ \_ Configura**</span><span class="sxs-lookup"><span data-stu-id="c4b30-421"><span id="IDS_BUTTON_CONFIGURE"></span><span id="ids_button_configure"></span>**IDS\_BUTTON\_CONFIGURE**</span></span>  
<span data-ttu-id="c4b30-422">Testo visualizzato nella finestra di dialogo Configura firewall-pulsante confiture</span><span class="sxs-lookup"><span data-stu-id="c4b30-422">Text shown in the Configure Firewall dialog - Buttom Confiture</span></span>

<span data-ttu-id="c4b30-423"><span id="IDS_CONFIGURATION_CANCEL"></span><span id="ids_configuration_cancel"></span>**\_annullamento configurazione \_ ID**</span><span class="sxs-lookup"><span data-stu-id="c4b30-423"><span id="IDS_CONFIGURATION_CANCEL"></span><span id="ids_configuration_cancel"></span>**IDS\_CONFIGURATION\_CANCEL**</span></span>  
<span data-ttu-id="c4b30-424">Testo visualizzato nella finestra di dialogo Configura firewall-Annulla configurazione</span><span class="sxs-lookup"><span data-stu-id="c4b30-424">Text shown in the Configure Firewall dialog - Configuration Cancel</span></span>

<span data-ttu-id="c4b30-425"><span id="IDS_CAPTURETOOLTIP_MESSAGE_CORESYSTEM"></span><span id="ids_capturetooltip_message_coresystem"></span>**ID \_ CAPTURETOOLTIP \_ messaggio \_ CORESYSTEM**</span><span class="sxs-lookup"><span data-stu-id="c4b30-425"><span id="IDS_CAPTURETOOLTIP_MESSAGE_CORESYSTEM"></span><span id="ids_capturetooltip_message_coresystem"></span>**IDS\_CAPTURETOOLTIP\_MESSAGE\_CORESYSTEM**</span></span>  
<span data-ttu-id="c4b30-426">ID risorsa per la stringa "usare il pulsante di acquisizione in Visual Studio per acquisire i frame."</span><span class="sxs-lookup"><span data-stu-id="c4b30-426">Resource ID for string "Use the capture button in Visual Studio to capture frame(s)."</span></span>

<span data-ttu-id="c4b30-427"><span id="IDS_ET_NONE"></span><span id="ids_et_none"></span>**ID \_ ed \_ None**</span><span class="sxs-lookup"><span data-stu-id="c4b30-427"><span id="IDS_ET_NONE"></span><span id="ids_et_none"></span>**IDS\_ET\_NONE**</span></span>  
<span data-ttu-id="c4b30-428">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-428">Not used.</span></span>

<span data-ttu-id="c4b30-429"><span id="IDS_ET_SESSIONSTART"></span><span id="ids_et_sessionstart"></span>**ID \_ ed \_ SESSIONSTART**</span><span class="sxs-lookup"><span data-stu-id="c4b30-429"><span id="IDS_ET_SESSIONSTART"></span><span id="ids_et_sessionstart"></span>**IDS\_ET\_SESSIONSTART**</span></span>  
<span data-ttu-id="c4b30-430">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-430">Not used.</span></span>

<span data-ttu-id="c4b30-431"><span id="IDS_ET_SESSIONEND"></span><span id="ids_et_sessionend"></span>**ID \_ ed \_ SESSIONEND**</span><span class="sxs-lookup"><span data-stu-id="c4b30-431"><span id="IDS_ET_SESSIONEND"></span><span id="ids_et_sessionend"></span>**IDS\_ET\_SESSIONEND**</span></span>  
<span data-ttu-id="c4b30-432">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-432">Not used.</span></span>

<span data-ttu-id="c4b30-433"><span id="IDS_ET_PROCESSSTART"></span><span id="ids_et_processstart"></span>**ID \_ ed \_ PROCESSSTART**</span><span class="sxs-lookup"><span data-stu-id="c4b30-433"><span id="IDS_ET_PROCESSSTART"></span><span id="ids_et_processstart"></span>**IDS\_ET\_PROCESSSTART**</span></span>  
<span data-ttu-id="c4b30-434">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-434">Not used.</span></span>

<span data-ttu-id="c4b30-435"><span id="IDS_ET_PROCESSEND"></span><span id="ids_et_processend"></span>**ID \_ ed \_ PROCESSEND**</span><span class="sxs-lookup"><span data-stu-id="c4b30-435"><span id="IDS_ET_PROCESSEND"></span><span id="ids_et_processend"></span>**IDS\_ET\_PROCESSEND**</span></span>  
<span data-ttu-id="c4b30-436">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-436">Not used.</span></span>

<span data-ttu-id="c4b30-437"><span id="IDS_ET_FRAMEBEGIN"></span><span id="ids_et_framebegin"></span>**ID \_ ed \_ FRAMEBEGIN**</span><span class="sxs-lookup"><span data-stu-id="c4b30-437"><span id="IDS_ET_FRAMEBEGIN"></span><span id="ids_et_framebegin"></span>**IDS\_ET\_FRAMEBEGIN**</span></span>  
<span data-ttu-id="c4b30-438">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-438">Not used.</span></span>

<span data-ttu-id="c4b30-439"><span id="IDS_ET_FRAMEEND"></span><span id="ids_et_frameend"></span>**ID \_ ed \_ FRAMEEND**</span><span class="sxs-lookup"><span data-stu-id="c4b30-439"><span id="IDS_ET_FRAMEEND"></span><span id="ids_et_frameend"></span>**IDS\_ET\_FRAMEEND**</span></span>  
<span data-ttu-id="c4b30-440">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-440">Not used.</span></span>

<span data-ttu-id="c4b30-441"><span id="IDS_ET_USEREVENTBEGIN"></span><span id="ids_et_usereventbegin"></span>**ID \_ ed \_ USEREVENTBEGIN**</span><span class="sxs-lookup"><span data-stu-id="c4b30-441"><span id="IDS_ET_USEREVENTBEGIN"></span><span id="ids_et_usereventbegin"></span>**IDS\_ET\_USEREVENTBEGIN**</span></span>  
<span data-ttu-id="c4b30-442">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-442">Not used.</span></span>

<span data-ttu-id="c4b30-443"><span id="IDS_ET_USEREVENTEND"></span><span id="ids_et_usereventend"></span>**ID \_ ed \_ USEREVENTEND**</span><span class="sxs-lookup"><span data-stu-id="c4b30-443"><span id="IDS_ET_USEREVENTEND"></span><span id="ids_et_usereventend"></span>**IDS\_ET\_USEREVENTEND**</span></span>  
<span data-ttu-id="c4b30-444">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-444">Not used.</span></span>

<span data-ttu-id="c4b30-445"><span id="IDS_ET_USERMARKER"></span><span id="ids_et_usermarker"></span>**ID \_ ed \_ USERMARKER**</span><span class="sxs-lookup"><span data-stu-id="c4b30-445"><span id="IDS_ET_USERMARKER"></span><span id="ids_et_usermarker"></span>**IDS\_ET\_USERMARKER**</span></span>  
<span data-ttu-id="c4b30-446">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-446">Not used.</span></span>

<span data-ttu-id="c4b30-447"><span id="IDS_ET_CALL"></span><span id="ids_et_call"></span>**ID \_ e \_ chiamata**</span><span class="sxs-lookup"><span data-stu-id="c4b30-447"><span id="IDS_ET_CALL"></span><span id="ids_et_call"></span>**IDS\_ET\_CALL**</span></span>  
<span data-ttu-id="c4b30-448">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-448">Not used.</span></span>

<span data-ttu-id="c4b30-449"><span id="IDS_ET_OBJECTPOPULATION"></span><span id="ids_et_objectpopulation"></span>**ID \_ ed \_ OBJECTPOPULATION**</span><span class="sxs-lookup"><span data-stu-id="c4b30-449"><span id="IDS_ET_OBJECTPOPULATION"></span><span id="ids_et_objectpopulation"></span>**IDS\_ET\_OBJECTPOPULATION**</span></span>  
<span data-ttu-id="c4b30-450">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-450">Not used.</span></span>

<span data-ttu-id="c4b30-451"><span id="IDS_ET_OBJECTCREATION"></span><span id="ids_et_objectcreation"></span>**ID \_ ed \_ OBJECTCREATION**</span><span class="sxs-lookup"><span data-stu-id="c4b30-451"><span id="IDS_ET_OBJECTCREATION"></span><span id="ids_et_objectcreation"></span>**IDS\_ET\_OBJECTCREATION**</span></span>  
<span data-ttu-id="c4b30-452">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-452">Not used.</span></span>

<span data-ttu-id="c4b30-453"><span id="IDS_ET_CALLSYNC"></span><span id="ids_et_callsync"></span>**ID \_ ed \_ CALLSYNC**</span><span class="sxs-lookup"><span data-stu-id="c4b30-453"><span id="IDS_ET_CALLSYNC"></span><span id="ids_et_callsync"></span>**IDS\_ET\_CALLSYNC**</span></span>  
<span data-ttu-id="c4b30-454">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-454">Not used.</span></span>

<span data-ttu-id="c4b30-455"><span id="IDS_ET_UNKNOWN"></span><span id="ids_et_unknown"></span>**ID \_ e \_ sconosciuti**</span><span class="sxs-lookup"><span data-stu-id="c4b30-455"><span id="IDS_ET_UNKNOWN"></span><span id="ids_et_unknown"></span>**IDS\_ET\_UNKNOWN**</span></span>  
<span data-ttu-id="c4b30-456">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-456">Not used.</span></span>

<span data-ttu-id="c4b30-457"><span id="IDS_TRIGGER_NONE"></span><span id="ids_trigger_none"></span>**ID \_ trigger \_ None**</span><span class="sxs-lookup"><span data-stu-id="c4b30-457"><span id="IDS_TRIGGER_NONE"></span><span id="ids_trigger_none"></span>**IDS\_TRIGGER\_NONE**</span></span>  
<span data-ttu-id="c4b30-458">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-458">Not used.</span></span>

<span data-ttu-id="c4b30-459"><span id="IDS_TRIGGER_PROGRAMSTART"></span><span id="ids_trigger_programstart"></span>**\_trigger ID \_ PROGRAMSTART**</span><span class="sxs-lookup"><span data-stu-id="c4b30-459"><span id="IDS_TRIGGER_PROGRAMSTART"></span><span id="ids_trigger_programstart"></span>**IDS\_TRIGGER\_PROGRAMSTART**</span></span>  
<span data-ttu-id="c4b30-460">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-460">Not used.</span></span>

<span data-ttu-id="c4b30-461"><span id="IDS_TRIGGER_FRAME"></span><span id="ids_trigger_frame"></span>**\_frame trigger \_ ID**</span><span class="sxs-lookup"><span data-stu-id="c4b30-461"><span id="IDS_TRIGGER_FRAME"></span><span id="ids_trigger_frame"></span>**IDS\_TRIGGER\_FRAME**</span></span>  
<span data-ttu-id="c4b30-462">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-462">Not used.</span></span>

<span data-ttu-id="c4b30-463"><span id="IDS_TRIGGER_TIME"></span><span id="ids_trigger_time"></span>**\_tempo di attivazione ID \_**</span><span class="sxs-lookup"><span data-stu-id="c4b30-463"><span id="IDS_TRIGGER_TIME"></span><span id="ids_trigger_time"></span>**IDS\_TRIGGER\_TIME**</span></span>  
<span data-ttu-id="c4b30-464">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-464">Not used.</span></span>

<span data-ttu-id="c4b30-465"><span id="IDS_TRIGGER_USERMARKER"></span><span id="ids_trigger_usermarker"></span>**\_trigger ID \_ USERMARKER**</span><span class="sxs-lookup"><span data-stu-id="c4b30-465"><span id="IDS_TRIGGER_USERMARKER"></span><span id="ids_trigger_usermarker"></span>**IDS\_TRIGGER\_USERMARKER**</span></span>  
<span data-ttu-id="c4b30-466">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-466">Not used.</span></span>

<span data-ttu-id="c4b30-467"><span id="IDS_TRIGGER_BEGINUSEREVENT"></span><span id="ids_trigger_beginuserevent"></span>**\_trigger ID \_ BEGINUSEREVENT**</span><span class="sxs-lookup"><span data-stu-id="c4b30-467"><span id="IDS_TRIGGER_BEGINUSEREVENT"></span><span id="ids_trigger_beginuserevent"></span>**IDS\_TRIGGER\_BEGINUSEREVENT**</span></span>  
<span data-ttu-id="c4b30-468">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-468">Not used.</span></span>

<span data-ttu-id="c4b30-469"><span id="IDS_TRIGGER_ENDUSEREVENT"></span><span id="ids_trigger_enduserevent"></span>**\_trigger ID \_ ENDUSEREVENT**</span><span class="sxs-lookup"><span data-stu-id="c4b30-469"><span id="IDS_TRIGGER_ENDUSEREVENT"></span><span id="ids_trigger_enduserevent"></span>**IDS\_TRIGGER\_ENDUSEREVENT**</span></span>  
<span data-ttu-id="c4b30-470">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-470">Not used.</span></span>

<span data-ttu-id="c4b30-471"><span id="IDS_TRIGGER_CAPTUREFRAME"></span><span id="ids_trigger_captureframe"></span>**\_trigger ID \_ CAPTUREFRAME**</span><span class="sxs-lookup"><span data-stu-id="c4b30-471"><span id="IDS_TRIGGER_CAPTUREFRAME"></span><span id="ids_trigger_captureframe"></span>**IDS\_TRIGGER\_CAPTUREFRAME**</span></span>  
<span data-ttu-id="c4b30-472">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-472">Not used.</span></span>

<span data-ttu-id="c4b30-473"><span id="IDS_TRIGGER_APICAPTURE"></span><span id="ids_trigger_apicapture"></span>**\_trigger ID \_ APICAPTURE**</span><span class="sxs-lookup"><span data-stu-id="c4b30-473"><span id="IDS_TRIGGER_APICAPTURE"></span><span id="ids_trigger_apicapture"></span>**IDS\_TRIGGER\_APICAPTURE**</span></span>  
<span data-ttu-id="c4b30-474">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-474">Not used.</span></span>

<span data-ttu-id="c4b30-475"><span id="IDS_ERROR_CALLDATA"></span><span id="ids_error_calldata"></span>**ID \_ errore \_ CALLDATA**</span><span class="sxs-lookup"><span data-stu-id="c4b30-475"><span id="IDS_ERROR_CALLDATA"></span><span id="ids_error_calldata"></span>**IDS\_ERROR\_CALLDATA**</span></span>  
<span data-ttu-id="c4b30-476">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-476">Not used.</span></span>

<span data-ttu-id="c4b30-477"><span id="IDS_ERROR_CREATINGLOG"></span><span id="ids_error_creatinglog"></span>**ID \_ errore \_ CREATINGLOG**</span><span class="sxs-lookup"><span data-stu-id="c4b30-477"><span id="IDS_ERROR_CREATINGLOG"></span><span id="ids_error_creatinglog"></span>**IDS\_ERROR\_CREATINGLOG**</span></span>  
<span data-ttu-id="c4b30-478">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-478">Not used.</span></span>

<span data-ttu-id="c4b30-479"><span id="IDS_UNKNOWNCALL"></span><span id="ids_unknowncall"></span>**ID \_ UNKNOWNCALL**</span><span class="sxs-lookup"><span data-stu-id="c4b30-479"><span id="IDS_UNKNOWNCALL"></span><span id="ids_unknowncall"></span>**IDS\_UNKNOWNCALL**</span></span>  
<span data-ttu-id="c4b30-480">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-480">Not used.</span></span>

<span data-ttu-id="c4b30-481"><span id="IDS_WARN_FEATURE_LEVEL_CHANGED"></span><span id="ids_warn_feature_level_changed"></span>**ID \_ avviso \_ \_ livello funzionalità \_ modificato**</span><span class="sxs-lookup"><span data-stu-id="c4b30-481"><span id="IDS_WARN_FEATURE_LEVEL_CHANGED"></span><span id="ids_warn_feature_level_changed"></span>**IDS\_WARN\_FEATURE\_LEVEL\_CHANGED**</span></span>  
<span data-ttu-id="c4b30-482">Non usato.</span><span class="sxs-lookup"><span data-stu-id="c4b30-482">Not used.</span></span>

<span data-ttu-id="c4b30-483"><span id="ID_STATUS_FREQUENCY"></span><span id="id_status_frequency"></span>**\_frequenza stato \_ ID**</span><span class="sxs-lookup"><span data-stu-id="c4b30-483"><span id="ID_STATUS_FREQUENCY"></span><span id="id_status_frequency"></span>**ID\_STATUS\_FREQUENCY**</span></span>  

<span data-ttu-id="c4b30-484"><span id="ID_DISABLE_HUD"></span><span id="id_disable_hud"></span>**ID \_ disabilitare \_ HUD**</span><span class="sxs-lookup"><span data-stu-id="c4b30-484"><span id="ID_DISABLE_HUD"></span><span id="id_disable_hud"></span>**ID\_DISABLE\_HUD**</span></span>  

<span data-ttu-id="c4b30-485"><span id="ID_DISABLE_COMPAT"></span><span id="id_disable_compat"></span>**ID \_ Disabilita \_ compatibilità**</span><span class="sxs-lookup"><span data-stu-id="c4b30-485"><span id="ID_DISABLE_COMPAT"></span><span id="id_disable_compat"></span>**ID\_DISABLE\_COMPAT**</span></span>  

<span data-ttu-id="c4b30-486"><span id="ID_COLLECT_CALLSTACKS"></span><span id="id_collect_callstacks"></span>**ID \_ raccolta \_ stack**</span><span class="sxs-lookup"><span data-stu-id="c4b30-486"><span id="ID_COLLECT_CALLSTACKS"></span><span id="id_collect_callstacks"></span>**ID\_COLLECT\_CALLSTACKS**</span></span>  

<span data-ttu-id="c4b30-487"><span id="ID_ENABLE_SDKERROR_STOP"></span><span id="id_enable_sdkerror_stop"></span>**ID \_ Abilita \_ SDKERROR \_ Stop**</span><span class="sxs-lookup"><span data-stu-id="c4b30-487"><span id="ID_ENABLE_SDKERROR_STOP"></span><span id="id_enable_sdkerror_stop"></span>**ID\_ENABLE\_SDKERROR\_STOP**</span></span>  

## <a name="requirements"></a><span data-ttu-id="c4b30-488">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c4b30-488">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="c4b30-489">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c4b30-489">Header</span></span></p></td><td><span data-ttu-id="c4b30-490">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="c4b30-490">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



