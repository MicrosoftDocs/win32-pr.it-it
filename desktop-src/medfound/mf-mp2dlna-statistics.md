---
description: Ottiene le statistiche dal sink di supporti Digital Living Network Alliance (DLNA).
ms.assetid: 1fa6ea9f-fd30-4fa2-a0e6-1647273bcc35
title: Attributo MF_MP2DLNA_STATISTICS (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a51620c1ca093a422a5e4657edcfbfaa66ae6cd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528255"
---
# <a name="mf_mp2dlna_statistics-attribute"></a><span data-ttu-id="3d9f8-103">\_ \_ Attributo Statistics MF MP2DLNA</span><span class="sxs-lookup"><span data-stu-id="3d9f8-103">MF\_MP2DLNA\_STATISTICS attribute</span></span>

<span data-ttu-id="3d9f8-104">Ottiene le statistiche dal sink di supporti Digital Living Network Alliance (DLNA).</span><span class="sxs-lookup"><span data-stu-id="3d9f8-104">Gets statistics from the Digital Living Network Alliance (DLNA) media sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="3d9f8-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="3d9f8-105">Data type</span></span>

<span data-ttu-id="3d9f8-106">**[**MFMPEG2DLNASINKSTATS**](/windows/desktop/api/mfmp2dlna/ns-mfmp2dlna-mfmpeg2dlnasinkstats)** archiviato come **byte \[ \]**</span><span class="sxs-lookup"><span data-stu-id="3d9f8-106">**[**MFMPEG2DLNASINKSTATS**](/windows/desktop/api/mfmp2dlna/ns-mfmp2dlna-mfmpeg2dlnasinkstats)** stored as **BYTE\[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="3d9f8-107">Ottenere/impostare</span><span class="sxs-lookup"><span data-stu-id="3d9f8-107">Get/set</span></span>

<span data-ttu-id="3d9f8-108">Per ottenere questo attributo, chiamare [**IMFAttributes:: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="3d9f8-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

## <a name="remarks"></a><span data-ttu-id="3d9f8-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="3d9f8-109">Remarks</span></span>

<span data-ttu-id="3d9f8-110">Durante lo streaming, il sink multimediale DLNA aggiorna questo attributo con le statistiche relative alla codifica e al multiplexing dei flussi MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="3d9f8-110">During streaming, the DLNA media sink updates this attribute with statistics about the encoding and multiplexing of the MPEG-2 streams.</span></span> <span data-ttu-id="3d9f8-111">L'applicazione può eseguire una query su questo attributo in qualsiasi momento per ottenere i valori più recenti.</span><span class="sxs-lookup"><span data-stu-id="3d9f8-111">The application can query this attribute at any time to get the latest values.</span></span>

<span data-ttu-id="3d9f8-112">L'impostazione di questo attributo sul sink multimediale DLNA non ha alcun effetto.</span><span class="sxs-lookup"><span data-stu-id="3d9f8-112">Setting this attribute on the DLNA media sink has no effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d9f8-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3d9f8-113">Requirements</span></span>



| <span data-ttu-id="3d9f8-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d9f8-114">Requirement</span></span> | <span data-ttu-id="3d9f8-115">Valore</span><span class="sxs-lookup"><span data-stu-id="3d9f8-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d9f8-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d9f8-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3d9f8-117">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3d9f8-117">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3d9f8-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3d9f8-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3d9f8-119">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="3d9f8-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3d9f8-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3d9f8-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d9f8-121"><dt>Mfmp2dlna. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d9f8-121"><dt>Mfmp2dlna.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d9f8-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3d9f8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d9f8-123">Elenco alfabetico degli attributi di Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3d9f8-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




