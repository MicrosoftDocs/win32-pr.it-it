---
description: Indica che le informazioni sulla lunghezza di NALU verranno inviate come BLOB con ciascun esempio H. 264 compresso.
ms.assetid: 71B50B44-6025-4EEC-8B37-53D80CF37B07
title: Attributo MF_NALU_LENGTH_SET (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a01034cf62758787747882da40ac703d205fa55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318717"
---
# <a name="mf_nalu_length_set-attribute"></a><span data-ttu-id="17908-103">\_ \_ Attributo set di lunghezza MF Nalu \_</span><span class="sxs-lookup"><span data-stu-id="17908-103">MF\_NALU\_LENGTH\_SET attribute</span></span>

<span data-ttu-id="17908-104">Indica che le informazioni sulla lunghezza di NALU verranno inviate come **BLOB** con ciascun esempio H. 264 compresso.</span><span class="sxs-lookup"><span data-stu-id="17908-104">Indicates that NALU length information will be sent as a **BLOB** with each compressed H.264 sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="17908-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="17908-105">Data type</span></span>

<span data-ttu-id="17908-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="17908-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="17908-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="17908-107">Remarks</span></span>

<span data-ttu-id="17908-108">Impostare questo attributo sul tipo di supporto di input di MEDIASUBTYPE \_ H264.</span><span class="sxs-lookup"><span data-stu-id="17908-108">Set this attribute on the input media type of MEDIASUBTYPE\_H264.</span></span>

<span data-ttu-id="17908-109">Impostare \_ \_ la lunghezza MF Nalu \_ impostata sul tipo di supporto di input del decodificatore H. 264, che indica che ogni esempio di input avrà una lunghezza di Nalu disponibile e ogni esempio di input conterrà un'immagine primaria completa.</span><span class="sxs-lookup"><span data-stu-id="17908-109">Set MF\_NALU\_LENGTH\_SET on input media type of H.264 decoder, indicating each input sample will have a NALU length available and each input sample contains one complete primary picture.</span></span>

<span data-ttu-id="17908-110">Il **BLOB** contenente le informazioni sulla lunghezza di Nalu può essere recuperato dall'attributo [MF \_ Nalu \_ length \_ Information](mf-nalu-length-information.md) nell'esempio di input.</span><span class="sxs-lookup"><span data-stu-id="17908-110">The **BLOB** containing the NALU length information can be retrieved from [MF\_NALU\_LENGTH\_INFORMATION](mf-nalu-length-information.md) attribute on the input sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="17908-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="17908-111">Requirements</span></span>



| <span data-ttu-id="17908-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="17908-112">Requirement</span></span> | <span data-ttu-id="17908-113">Valore</span><span class="sxs-lookup"><span data-stu-id="17908-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="17908-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17908-114">Minimum supported client</span></span><br/> | <span data-ttu-id="17908-115">App desktop di Windows 8 app \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="17908-115">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="17908-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="17908-116">Minimum supported server</span></span><br/> | <span data-ttu-id="17908-117">App UWP per \[ app desktop di Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="17908-117">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="17908-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="17908-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="17908-119"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="17908-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17908-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="17908-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17908-121">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="17908-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="17908-122">Attributi del tipo di supporto</span><span class="sxs-lookup"><span data-stu-id="17908-122">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




