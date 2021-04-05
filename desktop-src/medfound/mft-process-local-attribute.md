---
description: Specifica se una trasformazione Media Foundation (MFT) viene registrata solo nel processo di applicazioni.
ms.assetid: e10d6378-8e85-4f73-9fa3-a2e954fc8249
title: Attributo MFT_PROCESS_LOCAL_Attribute (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1d3595ef530008b8d09f27e3e76fad81a06039
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753943"
---
# <a name="mft_process_local_attribute-attribute"></a><span data-ttu-id="592ee-103">\_Attributo dell' \_ attributo locale del processo MFT \_</span><span class="sxs-lookup"><span data-stu-id="592ee-103">MFT\_PROCESS\_LOCAL\_Attribute attribute</span></span>

<span data-ttu-id="592ee-104">Specifica se una trasformazione Media Foundation (MFT) viene registrata solo nel processo dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="592ee-104">Specifies whether a Media Foundation transform (MFT) is registered only in the application's process.</span></span>

## <a name="data-type"></a><span data-ttu-id="592ee-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="592ee-105">Data type</span></span>

<span data-ttu-id="592ee-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="592ee-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="592ee-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="592ee-107">Get/set</span></span>

<span data-ttu-id="592ee-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="592ee-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="592ee-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="592ee-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="592ee-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="592ee-110">Remarks</span></span>

<span data-ttu-id="592ee-111">Questo attributo viene utilizzato come segue:</span><span class="sxs-lookup"><span data-stu-id="592ee-111">This attribute is used as follows:</span></span>

1.  <span data-ttu-id="592ee-112">L'applicazione registra una MFT locale chiamando la funzione [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) o [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid) .</span><span class="sxs-lookup"><span data-stu-id="592ee-112">The application registers a local MFT by calling either the [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal) or [**MFTRegisterLocalByCLSID**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocalbyclsid) function.</span></span> <span data-ttu-id="592ee-113">Queste funzioni registrano il MFT nel processo dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="592ee-113">These functions register the MFT in the application's process.</span></span>
2.  <span data-ttu-id="592ee-114">Viene chiamata la funzione [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) per enumerare MFTS che corrispondono a un particolare set di criteri.</span><span class="sxs-lookup"><span data-stu-id="592ee-114">The [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function is called to enumerate MFTs that match a particular set of criteria.</span></span> <span data-ttu-id="592ee-115">L'applicazione può chiamare direttamente la funzione **MFTEnumEx** , ma più spesso questa funzione viene chiamata dal caricatore della topologia.</span><span class="sxs-lookup"><span data-stu-id="592ee-115">The application might call the **MFTEnumEx** function directly, but more often this function is called by the topology loader.</span></span>
3.  <span data-ttu-id="592ee-116">La funzione [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) recupera una matrice di puntatori [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , ognuno dei quali rappresenta un oggetto Activation per un MFT.</span><span class="sxs-lookup"><span data-stu-id="592ee-116">The [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function retrieves an array of [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers, each representing an activation object for an MFT.</span></span> <span data-ttu-id="592ee-117">Se una MFT è registrata localmente, l' \_ attributo dell' \_ attributo locale del processo MFT \_ viene impostato su **true** nell'oggetto Activation corrispondente.</span><span class="sxs-lookup"><span data-stu-id="592ee-117">If an MFT is registered locally, the MFT\_PROCESS\_LOCAL\_Attribute attribute is set to **TRUE** on the corresponding activation object.</span></span>

<span data-ttu-id="592ee-118">Il valore predefinito di questo attributo è **false**.</span><span class="sxs-lookup"><span data-stu-id="592ee-118">The default value for this attribute is **FALSE**.</span></span>

<span data-ttu-id="592ee-119">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="592ee-119">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="592ee-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="592ee-120">Requirements</span></span>



| <span data-ttu-id="592ee-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="592ee-121">Requirement</span></span> | <span data-ttu-id="592ee-122">Valore</span><span class="sxs-lookup"><span data-stu-id="592ee-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="592ee-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="592ee-123">Minimum supported client</span></span><br/> | <span data-ttu-id="592ee-124">App desktop di Windows 7 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="592ee-124">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="592ee-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="592ee-125">Minimum supported server</span></span><br/> | <span data-ttu-id="592ee-126">App desktop di Windows Server 2008 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="592ee-126">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="592ee-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="592ee-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="592ee-128"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="592ee-128"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="592ee-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="592ee-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="592ee-130">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="592ee-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="592ee-131">Attributi di trasformazione</span><span class="sxs-lookup"><span data-stu-id="592ee-131">Transform Attributes</span></span>](transform-attributes.md)
</dt> </dl>

 

 




