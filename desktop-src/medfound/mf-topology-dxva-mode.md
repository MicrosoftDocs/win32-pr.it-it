---
description: Specifica se il caricatore della topologia Abilita Microsoft DirectX Video Acceleration (DXVA) nella topologia.
ms.assetid: 03783ef3-f957-41e3-9734-94cb34ecc088
title: Attributo MF_TOPOLOGY_DXVA_MODE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ad75b37a2ca2e971077b05d1bbeb92748530614
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306754"
---
# <a name="mf_topology_dxva_mode-attribute"></a><span data-ttu-id="c7105-103">\_ \_ Attributo modalità DXVA TOPOLOGIa MF \_</span><span class="sxs-lookup"><span data-stu-id="c7105-103">MF\_TOPOLOGY\_DXVA\_MODE attribute</span></span>

<span data-ttu-id="c7105-104">Specifica se il caricatore della topologia Abilita Microsoft DirectX Video Acceleration (DXVA) nella topologia.</span><span class="sxs-lookup"><span data-stu-id="c7105-104">Specifies whether the topology loader enables Microsoft DirectX Video Acceleration (DXVA) in the topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="c7105-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="c7105-105">Data type</span></span>

<span data-ttu-id="c7105-106">**[**MFTOPOLOGY \_ \_Modalità DXVA**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode)** archiviata come **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c7105-106">**[**MFTOPOLOGY\_DXVA\_MODE**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode)** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="c7105-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="c7105-107">Get/set</span></span>

<span data-ttu-id="c7105-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="c7105-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="c7105-109">Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.</span><span class="sxs-lookup"><span data-stu-id="c7105-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="c7105-110">Si applica a</span><span class="sxs-lookup"><span data-stu-id="c7105-110">Applies to</span></span>

[<span data-ttu-id="c7105-111">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="c7105-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="c7105-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="c7105-112">Remarks</span></span>

<span data-ttu-id="c7105-113">Il valore di questo attributo è una costante di enumerazione della [**\_ \_ Modalità DXVA di MFTOPOLOGY**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode) .</span><span class="sxs-lookup"><span data-stu-id="c7105-113">The value of this attribute is an [**MFTOPOLOGY\_DXVA\_MODE**](/windows/desktop/api/mfidl/ne-mfidl-mftopology_dxva_mode) enumeration constant.</span></span> <span data-ttu-id="c7105-114">Il valore predefinito è **MFTOPOLOGY \_ DXVA \_ default**.</span><span class="sxs-lookup"><span data-stu-id="c7105-114">The default value is **MFTOPOLOGY\_DXVA\_DEFAULT**.</span></span>

<span data-ttu-id="c7105-115">Questo attributo controlla quali MFTs ricevono un puntatore a gestione dispositivi Direct3D.</span><span class="sxs-lookup"><span data-stu-id="c7105-115">This attribute controls which MFTs receive a pointer to the Direct3D device manager.</span></span> <span data-ttu-id="c7105-116">Per abilitare l'accelerazione video completa, impostare il valore su **MFTOPOLOGY \_ DXVA \_ full**.</span><span class="sxs-lookup"><span data-stu-id="c7105-116">To enable full video acceleration, set the value to **MFTOPOLOGY\_DXVA\_FULL**.</span></span> <span data-ttu-id="c7105-117">Il valore **MFTOPOLOGY \_ DXVA \_ default** è definito per compatibilità con le versioni precedenti, ma corrisponde al comportamento di tutte le versioni precedenti di Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="c7105-117">The value **MFTOPOLOGY\_DXVA\_DEFAULT** is defined for backward compatibility; it matches the behavior of all earlier versions of Microsoft Media Foundation.</span></span>

<span data-ttu-id="c7105-118">La costante GUID per questo attributo viene esportata da mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="c7105-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7105-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c7105-119">Requirements</span></span>



| <span data-ttu-id="c7105-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7105-120">Requirement</span></span> | <span data-ttu-id="c7105-121">Valore</span><span class="sxs-lookup"><span data-stu-id="c7105-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c7105-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c7105-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c7105-123">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="c7105-123">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c7105-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c7105-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c7105-125">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c7105-125">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="c7105-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c7105-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7105-127"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7105-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7105-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c7105-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7105-129">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c7105-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c7105-130">Gestione dispositivi Direct3D</span><span class="sxs-lookup"><span data-stu-id="c7105-130">Direct3D Device Manager</span></span>](direct3d-device-manager.md)
</dt> <dt>

[<span data-ttu-id="c7105-131">Attributi della topologia</span><span class="sxs-lookup"><span data-stu-id="c7105-131">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




