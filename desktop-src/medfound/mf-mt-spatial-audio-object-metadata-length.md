---
description: Valore che specifica la dimensione, in byte, del tipo di oggetto dei metadati audio spaziali che il decodificatore genererà come output.
ms.assetid: C133693D-A8D5-4520-B561-57BF11074257
title: Attributo MF_MT_SPATIAL_AUDIO_OBJECT_METADATA_LENGTH (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2cd0b3cab788dbc724ab896d2cbfeb0d42f633f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231775"
---
# <a name="mf_mt_spatial_audio_object_metadata_length-attribute"></a><span data-ttu-id="75426-103">\_Attributo della \_ \_ \_ \_ lunghezza dei metadati dell'oggetto audio \_ spaziale MF mt</span><span class="sxs-lookup"><span data-stu-id="75426-103">MF\_MT\_SPATIAL\_AUDIO\_OBJECT\_METADATA\_LENGTH attribute</span></span>

<span data-ttu-id="75426-104">Valore che specifica la dimensione, in byte, del tipo di oggetto dei metadati audio spaziali che il decodificatore genererà come output.</span><span class="sxs-lookup"><span data-stu-id="75426-104">A value specifying the size, in bytes, of the spatial audio metadata object type that the decoder will output.</span></span>

## <a name="data-type"></a><span data-ttu-id="75426-105">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="75426-105">Data type</span></span>

<span data-ttu-id="75426-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="75426-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="75426-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="75426-107">Remarks</span></span>

<span data-ttu-id="75426-108">Il BLOB di metadati con il formato specificato viene scritto usando l'interfaccia [**ISpatialAudioMetadataWriter**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter) e viene letto usando l'interfaccia [**ISpatialAudioMetadataReader**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader) .</span><span class="sxs-lookup"><span data-stu-id="75426-108">The metadata blob with the specified format is written using the [**ISpatialAudioMetadataWriter**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter) interface and read using the [**ISpatialAudioMetadataReader**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader) interface.</span></span> <span data-ttu-id="75426-109">Il BLOB dei metadati è opaco per i componenti e la pipeline Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="75426-109">The metadata blob is opaque to the Media Foundation pipeline and components.</span></span> <span data-ttu-id="75426-110">L'attributo viene applicato al tipo di supporti audio spaziali.</span><span class="sxs-lookup"><span data-stu-id="75426-110">The attribute is applied to the spatial audio media type.</span></span>

## <a name="requirements"></a><span data-ttu-id="75426-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="75426-111">Requirements</span></span>



| <span data-ttu-id="75426-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="75426-112">Requirement</span></span> | <span data-ttu-id="75426-113">Valore</span><span class="sxs-lookup"><span data-stu-id="75426-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="75426-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75426-114">Minimum supported client</span></span><br/> | <span data-ttu-id="75426-115">Solo app desktop Windows 10 versione 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="75426-115">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="75426-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="75426-116">Minimum supported server</span></span><br/> | <span data-ttu-id="75426-117">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="75426-117">None supported</span></span><br/>                                                          |
| <span data-ttu-id="75426-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="75426-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="75426-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="75426-119"><dt>Mfapi.h</dt></span></span> </dl> |



 

 
