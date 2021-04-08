---
description: Specifica il timestamp originale del dispositivo nell'esempio.
ms.assetid: 93BB6E41-308E-4527-A04B-C685C818FEC4
title: Attributo MFSampleExtension_DeviceReferenceSystemTime (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00af99e3d2c34d0e4cf72af519497ea04f13e62c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880070"
---
# <a name="mfsampleextension_devicereferencesystemtime-attribute"></a><span data-ttu-id="f5ed9-103">\_Attributo DeviceReferenceSystemTime di MFSampleExtension</span><span class="sxs-lookup"><span data-stu-id="f5ed9-103">MFSampleExtension\_DeviceReferenceSystemTime attribute</span></span>

<span data-ttu-id="f5ed9-104">Specifica il timestamp originale del dispositivo nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="f5ed9-104">Specifies the original device timestamp on the sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="f5ed9-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="f5ed9-105">Data type</span></span>

<span data-ttu-id="f5ed9-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="f5ed9-106">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="f5ed9-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="f5ed9-107">Remarks</span></span>

<span data-ttu-id="f5ed9-108">Si tratta del timestamp di riferimento del dispositivo degli esempi di supporti nella risoluzione 100 ns.</span><span class="sxs-lookup"><span data-stu-id="f5ed9-108">This is the a device reference time stamp of media samples in 100ns resolution.</span></span> <span data-ttu-id="f5ed9-109">Questo timestamp può contenere o meno il valore effettivo del contatore delle prestazioni della query (QPC), a seconda dell'origine che produce gli esempi.</span><span class="sxs-lookup"><span data-stu-id="f5ed9-109">This time stamp may or may not carry the actual value of the query performance counter (QPC), depending on the source producing the samples.</span></span> <span data-ttu-id="f5ed9-110">Questo valore può essere modificato da altri componenti della pipeline multimediale.</span><span class="sxs-lookup"><span data-stu-id="f5ed9-110">This value may be modified by other components in the media pipeline.</span></span> <span data-ttu-id="f5ed9-111">Questo valore non è disponibile per MFTs inserito nella pipeline di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="f5ed9-111">This value is not available to MFTs inserted into the capture pipeline.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5ed9-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5ed9-112">Requirements</span></span>



| <span data-ttu-id="f5ed9-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5ed9-113">Requirement</span></span> | <span data-ttu-id="f5ed9-114">Valore</span><span class="sxs-lookup"><span data-stu-id="f5ed9-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5ed9-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5ed9-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f5ed9-116">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f5ed9-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="f5ed9-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5ed9-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f5ed9-118">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="f5ed9-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f5ed9-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f5ed9-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5ed9-120"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5ed9-120"><dt>Mfcaptureengine.h</dt></span></span> </dl>   |
| <span data-ttu-id="f5ed9-121">IDL</span><span class="sxs-lookup"><span data-stu-id="f5ed9-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f5ed9-122"><dt>Mfcaptureengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f5ed9-122"><dt>Mfcaptureengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5ed9-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f5ed9-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5ed9-124">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f5ed9-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




