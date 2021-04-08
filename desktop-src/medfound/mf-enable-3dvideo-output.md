---
description: Specifica il modo in cui un Media Foundation Transform (MFT) deve restituire un flusso video stereoscopico 3D.
ms.assetid: AA75A2FB-DEAC-44E9-93E9-4AC2D9F03B39
title: Attributo MF_ENABLE_3DVIDEO_OUTPUT (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd0123a574ec74ed4aa9fa0aea3b2cabecbb29da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880234"
---
# <a name="mf_enable_3dvideo_output-attribute"></a><span data-ttu-id="d6f92-103">\_Abilita l' \_ \_ attributo output 3DVIDEO</span><span class="sxs-lookup"><span data-stu-id="d6f92-103">MF\_ENABLE\_3DVIDEO\_OUTPUT attribute</span></span>

<span data-ttu-id="d6f92-104">Specifica il modo in cui un Media Foundation Transform (MFT) deve restituire un flusso video stereoscopico 3D.</span><span class="sxs-lookup"><span data-stu-id="d6f92-104">Specifies how a Media Foundation transform (MFT) should output a 3D stereoscopic video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="d6f92-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="d6f92-105">Data type</span></span>

<span data-ttu-id="d6f92-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="d6f92-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="d6f92-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="d6f92-107">Remarks</span></span>

<span data-ttu-id="d6f92-108">Il valore dell'attributo è un membro dell'enumerazione [**MF3DVideoOutputType**](/windows/desktop/api/mftransform/ne-mftransform-mf3dvideooutputtype) .</span><span class="sxs-lookup"><span data-stu-id="d6f92-108">The value of the attribute is a member of the [**MF3DVideoOutputType**](/windows/desktop/api/mftransform/ne-mftransform-mf3dvideooutputtype) enumeration.</span></span>

<span data-ttu-id="d6f92-109">Questo attributo si applica solo se MFT restituisce **true** per l' [attributo \_ \_ 3DVIDEO del supporto MFT](mft-support-3dvideo.md) .</span><span class="sxs-lookup"><span data-stu-id="d6f92-109">This attribute applies only if the MFT returns **TRUE** for the [MFT\_SUPPORT\_3DVIDEO](mft-support-3dvideo.md) attribute.</span></span>

<span data-ttu-id="d6f92-110">Per ottenere o impostare questo attributo, chiamare [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) per ottenere l'archivio di attributi globale di MFT.</span><span class="sxs-lookup"><span data-stu-id="d6f92-110">To get or set this attribute call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) to get the global attribute store of the MFT.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6f92-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d6f92-111">Requirements</span></span>



| <span data-ttu-id="d6f92-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6f92-112">Requirement</span></span> | <span data-ttu-id="d6f92-113">Valore</span><span class="sxs-lookup"><span data-stu-id="d6f92-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6f92-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d6f92-114">Minimum supported client</span></span><br/> | <span data-ttu-id="d6f92-115">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d6f92-115">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="d6f92-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d6f92-116">Minimum supported server</span></span><br/> | <span data-ttu-id="d6f92-117">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="d6f92-117">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="d6f92-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d6f92-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6f92-119"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6f92-119"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6f92-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d6f92-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6f92-121">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d6f92-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




