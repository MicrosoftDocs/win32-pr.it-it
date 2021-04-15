---
description: GUID definito dal decodificatore che identifica il formato dei metadati audio spaziali, inviando una notifica ai componenti downstream del tipo di oggetto di metadati che il decodificatore genererà come output.
ms.assetid: 9714A2C7-25A1-4735-A0AC-22329ECBBC46
title: Attributo MF_MT_SPATIAL_AUDIO_OBJECT_METADATA_FORMAT_ID (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed16188a24b4c61facf1e325867d093b9b5cc869
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231776"
---
# <a name="mf_mt_spatial_audio_object_metadata_format_id-attribute"></a><span data-ttu-id="a5787-103">\_ \_ \_ \_ \_ \_ Attributo ID formato dei metadati degli oggetti audio spaziali MF mt \_</span><span class="sxs-lookup"><span data-stu-id="a5787-103">MF\_MT\_SPATIAL\_AUDIO\_OBJECT\_METADATA\_FORMAT\_ID attribute</span></span>

<span data-ttu-id="a5787-104">GUID definito dal decodificatore che identifica il formato dei metadati audio spaziali, inviando una notifica ai componenti downstream del tipo di oggetto di metadati che il decodificatore genererà come output.</span><span class="sxs-lookup"><span data-stu-id="a5787-104">A decoder-defined GUID that identifies the spatial audio metadata format, notifying downstream components of the metadata object type that the decoder will output.</span></span>

## <a name="data-type"></a><span data-ttu-id="a5787-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a5787-105">Data type</span></span>

<span data-ttu-id="a5787-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="a5787-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="a5787-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="a5787-107">Remarks</span></span>

<span data-ttu-id="a5787-108">Il BLOB di metadati con il formato specificato viene scritto usando l'interfaccia [**ISpatialAudioMetadataWriter**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter) e viene letto usando l'interfaccia [**ISpatialAudioMetadataReader**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader) .</span><span class="sxs-lookup"><span data-stu-id="a5787-108">The metadata blob with the specified format is written using the [**ISpatialAudioMetadataWriter**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter) interface and read using the [**ISpatialAudioMetadataReader**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader) interface.</span></span> <span data-ttu-id="a5787-109">Il BLOB dei metadati è opaco per i componenti e la pipeline Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="a5787-109">The metadata blob is opaque to the Media Foundation pipeline and components.</span></span> <span data-ttu-id="a5787-110">L'attributo viene applicato al tipo di supporti audio spaziali.</span><span class="sxs-lookup"><span data-stu-id="a5787-110">The attribute is applied to the spatial audio media type.</span></span> <span data-ttu-id="a5787-111">Se un componente downstream non supporta il formato dei metadati specificato dal GUID, il componente deve rifiutare il tipo di supporto di input.</span><span class="sxs-lookup"><span data-stu-id="a5787-111">If a downstream component does not support the metadata format specified by the GUID, the component should reject the input media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5787-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a5787-112">Requirements</span></span>



| <span data-ttu-id="a5787-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5787-113">Requirement</span></span> | <span data-ttu-id="a5787-114">Valore</span><span class="sxs-lookup"><span data-stu-id="a5787-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a5787-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a5787-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a5787-116">Solo app desktop Windows 10 versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="a5787-116">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a5787-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a5787-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a5787-118">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="a5787-118">None supported</span></span><br/>                                                          |
| <span data-ttu-id="a5787-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a5787-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5787-120"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5787-120"><dt>Mfapi.h</dt></span></span> </dl> |



 

 
