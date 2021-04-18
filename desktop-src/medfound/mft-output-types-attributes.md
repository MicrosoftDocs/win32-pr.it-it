---
description: Contiene i tipi di output registrati per una trasformazione Media Foundation (MFT).
ms.assetid: 925267a2-4421-4874-a8a2-437876c729f1
title: Attributo MFT_OUTPUT_TYPES_Attributes (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 991b94b52782eb631846ee1ce182b4676a3cfd2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309075"
---
# <a name="mft_output_types_attributes-attribute"></a><span data-ttu-id="d3807-103">\_ \_ Attributo attributi tipi di output MFT \_</span><span class="sxs-lookup"><span data-stu-id="d3807-103">MFT\_OUTPUT\_TYPES\_Attributes attribute</span></span>

<span data-ttu-id="d3807-104">Contiene i tipi di output registrati per una trasformazione Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="d3807-104">Contains the registered output types for a Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="d3807-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="d3807-105">Data type</span></span>

<span data-ttu-id="d3807-106">**MFT \_ Registra \_ \_ informazioni \[ sul \] tipo** archiviate come **byte \[ \]**</span><span class="sxs-lookup"><span data-stu-id="d3807-106">**MFT\_REGISTER\_TYPE\_INFO\[\]** stored as **BYTE\[\]**</span></span>

## <a name="remarks"></a><span data-ttu-id="d3807-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="d3807-107">Remarks</span></span>

<span data-ttu-id="d3807-108">Questo attributo viene impostato sui puntatori [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) restituiti dalla funzione [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="d3807-108">This attribute is set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers returned by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

<span data-ttu-id="d3807-109">Questo attributo contiene una matrice di strutture di [**\_ informazioni sul \_ tipo \_ di registro MFT**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) che descrivono uno o più formati di output supportati da MFT.</span><span class="sxs-lookup"><span data-stu-id="d3807-109">This attribute contains an array of [**MFT\_REGISTER\_TYPE\_INFO**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) structures that describe one or more output formats supported by the MFT.</span></span> <span data-ttu-id="d3807-110">Questi valori vengono ricavati dal registro di sistema e sono intesi come hint per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d3807-110">These values are taken from the registry and are intended as a hint to the application.</span></span> <span data-ttu-id="d3807-111">Il MFT potrebbe supportare formati aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="d3807-111">The MFT might support additional formats.</span></span> <span data-ttu-id="d3807-112">Per impostare il formato di output effettivo, è necessario creare il MFT e chiamare [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span><span class="sxs-lookup"><span data-stu-id="d3807-112">To set the actual output format, you must create the MFT and call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span>

<span data-ttu-id="d3807-113">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="d3807-113">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3807-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d3807-114">Requirements</span></span>



| <span data-ttu-id="d3807-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3807-115">Requirement</span></span> | <span data-ttu-id="d3807-116">Valore</span><span class="sxs-lookup"><span data-stu-id="d3807-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3807-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3807-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d3807-118">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d3807-118">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="d3807-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d3807-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d3807-120">App desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d3807-120">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="d3807-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d3807-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3807-122"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3807-122"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3807-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d3807-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3807-124">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d3807-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d3807-125">Attributi di trasformazione</span><span class="sxs-lookup"><span data-stu-id="d3807-125">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




