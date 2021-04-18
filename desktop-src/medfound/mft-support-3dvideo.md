---
description: Specifica se una trasformazione Media Foundation (MFT) supporta video stereoscopici 3D.
ms.assetid: DE96FD14-5C7E-4560-99AC-B1EBDA1EBB2B
title: Attributo MFT_SUPPORT_3DVIDEO (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdbc7208f9bbcf2c638ae83e988c6e541a4be2f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309074"
---
# <a name="mft_support_3dvideo-attribute"></a><span data-ttu-id="e2c51-103">\_Attributo 3DVIDEO del supporto MFT \_</span><span class="sxs-lookup"><span data-stu-id="e2c51-103">MFT\_SUPPORT\_3DVIDEO attribute</span></span>

<span data-ttu-id="e2c51-104">Specifica se una trasformazione Media Foundation (MFT) supporta video stereoscopici 3D.</span><span class="sxs-lookup"><span data-stu-id="e2c51-104">Specifies whether a Media Foundation transform (MFT) supports 3D stereoscopic video.</span></span>

## <a name="data-type"></a><span data-ttu-id="e2c51-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="e2c51-105">Data type</span></span>

<span data-ttu-id="e2c51-106">**Bool** archiviato come **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e2c51-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="e2c51-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="e2c51-107">Remarks</span></span>

<span data-ttu-id="e2c51-108">Per eseguire una query su questo attributo, chiamare [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) per ottenere l'archivio di attributi globale di MFT.</span><span class="sxs-lookup"><span data-stu-id="e2c51-108">To query this attribute, call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) to get the global attribute store of the MFT.</span></span> <span data-ttu-id="e2c51-109">Se **GetAttributes** ha esito positivo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="e2c51-109">If **GetAttributes** succeeds, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="e2c51-110">Il valore predefinito di questo attributo è **false**.</span><span class="sxs-lookup"><span data-stu-id="e2c51-110">The default value of this attribute is **FALSE**.</span></span> <span data-ttu-id="e2c51-111">Considerare questo attributo come di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="e2c51-111">Treat this attribute as read-only.</span></span> <span data-ttu-id="e2c51-112">Non modificare il valore. il MFT ignorerà tutte le modifiche apportate al valore.</span><span class="sxs-lookup"><span data-stu-id="e2c51-112">Do not change the value; the MFT will ignore any changes to the value.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2c51-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e2c51-113">Requirements</span></span>



| <span data-ttu-id="e2c51-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2c51-114">Requirement</span></span> | <span data-ttu-id="e2c51-115">Valore</span><span class="sxs-lookup"><span data-stu-id="e2c51-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2c51-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e2c51-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e2c51-117">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e2c51-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="e2c51-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e2c51-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e2c51-119">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="e2c51-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="e2c51-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e2c51-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2c51-121"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2c51-121"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2c51-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e2c51-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2c51-123">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e2c51-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




