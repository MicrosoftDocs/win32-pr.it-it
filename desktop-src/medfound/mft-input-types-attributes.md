---
description: Contiene i tipi di input registrati per una trasformazione Media Foundation (MFT).
ms.assetid: 0fb1d9f2-2b57-41bc-8365-0b88bd5a2f3d
title: Attributo MFT_INPUT_TYPES_Attributes (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c42a051c124cdb96e57ea239c02ebaa47f22e0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527918"
---
# <a name="mft_input_types_attributes-attribute"></a><span data-ttu-id="33acf-103">\_ \_ Attributo attributi tipi di input MFT \_</span><span class="sxs-lookup"><span data-stu-id="33acf-103">MFT\_INPUT\_TYPES\_Attributes attribute</span></span>

<span data-ttu-id="33acf-104">Contiene i tipi di input registrati per una trasformazione Media Foundation (MFT).</span><span class="sxs-lookup"><span data-stu-id="33acf-104">Contains the registered input types for a Media Foundation transform (MFT).</span></span>

## <a name="data-type"></a><span data-ttu-id="33acf-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="33acf-105">Data type</span></span>

<span data-ttu-id="33acf-106">**MFT \_ Registra \_ \_ informazioni \[ sul \] tipo** archiviate come **byte \[ \]**</span><span class="sxs-lookup"><span data-stu-id="33acf-106">**MFT\_REGISTER\_TYPE\_INFO\[\]** stored as **BYTE\[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="33acf-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="33acf-107">Get/set</span></span>

<span data-ttu-id="33acf-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="33acf-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="33acf-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="33acf-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="remarks"></a><span data-ttu-id="33acf-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="33acf-110">Remarks</span></span>

<span data-ttu-id="33acf-111">Questo attributo viene impostato sui puntatori [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) restituiti dalla funzione [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="33acf-111">This attribute is set on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers returned by the [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

<span data-ttu-id="33acf-112">Questo attributo contiene una matrice di strutture di [**\_ informazioni sul \_ tipo \_ di registro MFT**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) che descrivono uno o più formati di input supportati da MFT.</span><span class="sxs-lookup"><span data-stu-id="33acf-112">This attribute contains an array of [**MFT\_REGISTER\_TYPE\_INFO**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) structures that describe one or more input formats supported by the MFT.</span></span> <span data-ttu-id="33acf-113">Questi valori vengono ricavati dal registro di sistema e sono intesi come hint per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="33acf-113">These values are taken from the registry and are intended as a hint to the application.</span></span> <span data-ttu-id="33acf-114">Il MFT potrebbe supportare formati aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="33acf-114">The MFT might support additional formats.</span></span> <span data-ttu-id="33acf-115">Per impostare il formato di input effettivo, è necessario creare il MFT e chiamare [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).</span><span class="sxs-lookup"><span data-stu-id="33acf-115">To set the actual input format, you must create the MFT and call [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype).</span></span>

<span data-ttu-id="33acf-116">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="33acf-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="33acf-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="33acf-117">Requirements</span></span>



| <span data-ttu-id="33acf-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="33acf-118">Requirement</span></span> | <span data-ttu-id="33acf-119">Valore</span><span class="sxs-lookup"><span data-stu-id="33acf-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="33acf-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33acf-120">Minimum supported client</span></span><br/> | <span data-ttu-id="33acf-121">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="33acf-121">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="33acf-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="33acf-122">Minimum supported server</span></span><br/> | <span data-ttu-id="33acf-123">App desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="33acf-123">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="33acf-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="33acf-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="33acf-125"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="33acf-125"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33acf-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="33acf-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33acf-127">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="33acf-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="33acf-128">Attributi di trasformazione</span><span class="sxs-lookup"><span data-stu-id="33acf-128">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




