---
description: Specifica il numero massimo di oggetti audio dinamici che possono essere sottoposti a rendering dall'endpoint audio simulataneously.
ms.assetid: 6B6D73C1-C2E6-4C23-BBAD-7B51E8441C71
title: Attributo MF_MT_SPATIAL_AUDIO_MAX_DYNAMIC_OBJECTS (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 358045079fb9cf52ad1fd0c8969f54723c7f02d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313044"
---
# <a name="mf_mt_spatial_audio_max_dynamic_objects-attribute"></a><span data-ttu-id="e90e2-103">\_ \_ \_ \_ \_ \_ Attributo massimo oggetti dinamici di MF mt spatial audio</span><span class="sxs-lookup"><span data-stu-id="e90e2-103">MF\_MT\_SPATIAL\_AUDIO\_MAX\_DYNAMIC\_OBJECTS attribute</span></span>

<span data-ttu-id="e90e2-104">Specifica il numero massimo di oggetti audio dinamici che possono essere sottoposti a rendering dall'endpoint audio simulataneously.</span><span class="sxs-lookup"><span data-stu-id="e90e2-104">Specifies the maximum number of dynamic audio objects that can be rendered by the audio endpoint simulataneously.</span></span>

## <a name="data-type"></a><span data-ttu-id="e90e2-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="e90e2-105">Data type</span></span>

<span data-ttu-id="e90e2-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="e90e2-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="e90e2-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="e90e2-107">Remarks</span></span>

<span data-ttu-id="e90e2-108">Un [**IMFSpatialAudioSample**](/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudiosample) può contenere un numero di campioni inferiore al numero specificato da questo attributo.</span><span class="sxs-lookup"><span data-stu-id="e90e2-108">An [**IMFSpatialAudioSample**](/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudiosample) may contain fewer samples than the number specified by this attribute.</span></span> <span data-ttu-id="e90e2-109">Se un esempio contiene più oggetti audio rispetto a quanto specificato da questo attributo, il comportamento non è definito.</span><span class="sxs-lookup"><span data-stu-id="e90e2-109">If a sample contains more audio objects than specified by this attribute, the behavior is undefined.</span></span>

## <a name="requirements"></a><span data-ttu-id="e90e2-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e90e2-110">Requirements</span></span>



| <span data-ttu-id="e90e2-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="e90e2-111">Requirement</span></span> | <span data-ttu-id="e90e2-112">Valore</span><span class="sxs-lookup"><span data-stu-id="e90e2-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e90e2-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e90e2-113">Minimum supported client</span></span><br/> | <span data-ttu-id="e90e2-114">Solo app desktop Windows 10 versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="e90e2-114">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e90e2-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e90e2-115">Minimum supported server</span></span><br/> | <span data-ttu-id="e90e2-116">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="e90e2-116">None supported</span></span><br/>                                                          |
| <span data-ttu-id="e90e2-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e90e2-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="e90e2-118"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e90e2-118"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




