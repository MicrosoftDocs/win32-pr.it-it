---
description: Completa tutte le operazioni necessarie sul buffer dei metadati e rilascia l'oggetto ISpatialAudioMetadataItems specificato.
ms.assetid: 2417E624-6535-49E2-9CF4-F927F731BE41
title: 'Metodo ISpatialAudioMetadataWriter:: Close'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISpatialAudioMetadataWriter.Close
api_type:
- COM
api_location:
- spatialaudiometadata.h
ms.openlocfilehash: 719c0d156c616c623d3e9a0d8a78620b735a7151
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127311"
---
# <a name="ispatialaudiometadatawriterclose-method"></a><span data-ttu-id="0f87f-103">Metodo ISpatialAudioMetadataWriter:: Close</span><span class="sxs-lookup"><span data-stu-id="0f87f-103">ISpatialAudioMetadataWriter::Close method</span></span>

<span data-ttu-id="0f87f-104">Completa tutte le operazioni necessarie sul buffer dei metadati e rilascia l'oggetto [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems) specificato.</span><span class="sxs-lookup"><span data-stu-id="0f87f-104">Completes any needed operations on the metadata buffer and releases the specified [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f87f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0f87f-105">Syntax</span></span>


```C++
HRESULT Close();
```



## <a name="parameters"></a><span data-ttu-id="0f87f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0f87f-106">Parameters</span></span>

<span data-ttu-id="0f87f-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="0f87f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0f87f-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0f87f-108">Return value</span></span>

<span data-ttu-id="0f87f-109">Se il metodo ha esito positivo, restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0f87f-109">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="0f87f-110">Se ha esito negativo, i codici restituiti possibili includono, ma non sono limitati, i valori mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="0f87f-110">If it fails, possible return codes include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="0f87f-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="0f87f-111">Return code</span></span>                                                                                                                     | <span data-ttu-id="0f87f-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0f87f-112">Description</span></span>                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0f87f-113"><dt>**SPTLAUD \_ MD \_ CLNT \_ E \_ nessun \_ elemento \_ aperto**</dt></span><span class="sxs-lookup"><span data-stu-id="0f87f-113"><dt>**SPTLAUD\_MD\_CLNT\_E\_NO\_ITEMS\_OPEN**</dt></span></span> </dl>            | <span data-ttu-id="0f87f-114">Il [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems) specificato non è stato aperto con una chiamata a [**Open**](/windows/desktop/api/SpatialAudioMetadata/nf-spatialaudiometadata-ispatialaudiometadatawriter-open).</span><span class="sxs-lookup"><span data-stu-id="0f87f-114">The supplied [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems) has not been opened with a call to [**Open**](/windows/desktop/api/SpatialAudioMetadata/nf-spatialaudiometadata-ispatialaudiometadatawriter-open).</span></span><br/> |
| <dl> <span data-ttu-id="0f87f-115"><dt>**SPTLAUD \_ MD \_ CLNT \_ E \_ nessun \_ elemento \_ scritto**</dt></span><span class="sxs-lookup"><span data-stu-id="0f87f-115"><dt>**SPTLAUD\_MD\_CLNT\_E\_NO\_ITEMS\_WRITTEN**</dt></span></span> </dl>         | <span data-ttu-id="0f87f-116">Nessun elemento di metadati scritto nel [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems)fornito.</span><span class="sxs-lookup"><span data-stu-id="0f87f-116">No metadata items have been written to the supplied [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems).</span></span><br/>                                              |
| <dl> <span data-ttu-id="0f87f-117"><dt>**l' \_ elemento SPTLAUD MD \_ CLNT \_ E \_ \_ deve \_ avere \_ comandi**</dt></span><span class="sxs-lookup"><span data-stu-id="0f87f-117"><dt>**SPTLAUD\_MD\_CLNT\_E\_ITEM\_MUST\_HAVE\_COMMANDS**</dt></span></span> </dl> | <span data-ttu-id="0f87f-118">Nessun comando di metadati scritto nel [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems)fornito.</span><span class="sxs-lookup"><span data-stu-id="0f87f-118">No metadata commands have been written to the supplied [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems).</span></span><br/>                                           |



 

## <a name="see-also"></a><span data-ttu-id="0f87f-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0f87f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f87f-120">**ISpatialAudioMetadataWriter**</span><span class="sxs-lookup"><span data-stu-id="0f87f-120">**ISpatialAudioMetadataWriter**</span></span>](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadatawriter)
</dt> </dl>

 

 




