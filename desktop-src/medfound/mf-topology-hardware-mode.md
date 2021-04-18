---
description: Specifica se caricare le trasformazioni di Microsoft Media Foundation basate su hardware (MFTs) nella topologia.
ms.assetid: f7ac3c9b-c163-412f-84c0-27bf551091d8
title: Attributo MF_TOPOLOGY_HARDWARE_MODE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec7933e9a380bbf5e66f4030a214f3f4aa93abc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305367"
---
# <a name="mf_topology_hardware_mode-attribute"></a><span data-ttu-id="c5fc7-103">\_ \_ Attributo modalità hardware della TOPOLOGIa MF \_</span><span class="sxs-lookup"><span data-stu-id="c5fc7-103">MF\_TOPOLOGY\_HARDWARE\_MODE attribute</span></span>

<span data-ttu-id="c5fc7-104">Specifica se caricare le trasformazioni di Microsoft Media Foundation basate su hardware (MFTs) nella topologia.</span><span class="sxs-lookup"><span data-stu-id="c5fc7-104">Specifies whether to load hardware-based Microsoft Media Foundation transforms (MFTs) in the topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="c5fc7-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c5fc7-105">Data type</span></span>

<span data-ttu-id="c5fc7-106">**[**MFTOPOLOGY \_ \_Modalità hardware**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_hardware_mode)** archiviata come **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c5fc7-106">**[**MFTOPOLOGY\_HARDWARE\_MODE**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_hardware_mode)** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="c5fc7-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="c5fc7-107">Get/set</span></span>

<span data-ttu-id="c5fc7-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="c5fc7-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="c5fc7-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="c5fc7-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="c5fc7-110">Si applica a</span><span class="sxs-lookup"><span data-stu-id="c5fc7-110">Applies to</span></span>

[<span data-ttu-id="c5fc7-111">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="c5fc7-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="c5fc7-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="c5fc7-112">Remarks</span></span>

<span data-ttu-id="c5fc7-113">Questo attributo è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="c5fc7-113">This attribute is optional.</span></span> <span data-ttu-id="c5fc7-114">Impostare l'attributo prima di risolvere la topologia.</span><span class="sxs-lookup"><span data-stu-id="c5fc7-114">Set the attribute before resolving the topology.</span></span>



| <span data-ttu-id="c5fc7-115">Valore</span><span class="sxs-lookup"><span data-stu-id="c5fc7-115">Value</span></span>                                  | <span data-ttu-id="c5fc7-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c5fc7-116">Description</span></span>                                                                                                                                                                                                                                                                       |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5fc7-117">**MFTOPOLOGY \_ HWMODE \_ Usa l' \_ hardware**</span><span class="sxs-lookup"><span data-stu-id="c5fc7-117">**MFTOPOLOGY\_HWMODE\_USE\_HARDWARE**</span></span>  | <span data-ttu-id="c5fc7-118">Il caricatore della topologia caricherà i MFTs basati su hardware, ad esempio i decodificatori hardware, quando disponibili.</span><span class="sxs-lookup"><span data-stu-id="c5fc7-118">The Topology Loader will load hardware-based MFTs, such as hardware decoders, when available.</span></span><br/> <span data-ttu-id="c5fc7-119">Il caricatore della topologia esegue automaticamente il fallback alla decodifica software se non viene trovato alcun decodificatore hardware o se un decodificatore hardware non riesce a connettersi per qualche motivo.</span><span class="sxs-lookup"><span data-stu-id="c5fc7-119">The Topology Loader automatically falls back to software decoding if no hardware decoder is found, or if a hardware decoder fails to connect for some reason.</span></span><br/> |
| <span data-ttu-id="c5fc7-120">**\_solo MFTOPOLOGY HWMODE \_ software \_**</span><span class="sxs-lookup"><span data-stu-id="c5fc7-120">**MFTOPOLOGY\_HWMODE\_SOFTWARE\_ONLY**</span></span> | <span data-ttu-id="c5fc7-121">Il caricatore della topologia caricherà solo MFTs software, inclusi i decodificatori software.</span><span class="sxs-lookup"><span data-stu-id="c5fc7-121">The Topology Loader will load only software MFTs, including software decoders.</span></span>                                                                                                                                                                                                    |



 

<span data-ttu-id="c5fc7-122">Il valore predefinito è **\_ \_ \_ solo MFTOPOLOGY HWMODE software**, per la compatibilità con le applicazioni esistenti.</span><span class="sxs-lookup"><span data-stu-id="c5fc7-122">The default value is **MFTOPOLOGY\_HWMODE\_SOFTWARE\_ONLY**, for compatibility with existing applications.</span></span> <span data-ttu-id="c5fc7-123">Il valore consigliato è **MFTOPOLOGY \_ HWMODE \_ use \_ hardware**.</span><span class="sxs-lookup"><span data-stu-id="c5fc7-123">The recommended value is **MFTOPOLOGY\_HWMODE\_USE\_HARDWARE**.</span></span>

<span data-ttu-id="c5fc7-124">Se il caricatore della topologia inserisce una MFT hardware nella topologia, imposta l'attributo dell' [ \_ \_ \_ \_ attributo dell'URL dell'enumerazione MFT](mft-enum-hardware-url-attribute.md) nel nodo della topologia.</span><span class="sxs-lookup"><span data-stu-id="c5fc7-124">If the Topology Loader inserts a hardware MFT into the topology, it sets the [MFT\_ENUM\_HARDWARE\_URL\_Attribute](mft-enum-hardware-url-attribute.md) attribute on the topology node.</span></span> <span data-ttu-id="c5fc7-125">Per verificare se è presente un hardware MFT, enumerare i nodi nella topologia risolta e verificare se questo attributo è presente.</span><span class="sxs-lookup"><span data-stu-id="c5fc7-125">To check whether a hardware MFT is present, enumerate the nodes in the resolved topology and check whether this attribute is present.</span></span>

<span data-ttu-id="c5fc7-126">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="c5fc7-126">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5fc7-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c5fc7-127">Requirements</span></span>



| <span data-ttu-id="c5fc7-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5fc7-128">Requirement</span></span> | <span data-ttu-id="c5fc7-129">Valore</span><span class="sxs-lookup"><span data-stu-id="c5fc7-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c5fc7-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c5fc7-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c5fc7-131">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c5fc7-131">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c5fc7-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c5fc7-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c5fc7-133">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c5fc7-133">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="c5fc7-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c5fc7-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5fc7-135"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5fc7-135"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5fc7-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c5fc7-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5fc7-137">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c5fc7-137">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c5fc7-138">Attributi della topologia</span><span class="sxs-lookup"><span data-stu-id="c5fc7-138">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




