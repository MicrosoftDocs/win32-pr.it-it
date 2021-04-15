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
# <a name="mf_mt_spatial_audio_object_metadata_format_id-attribute"></a>\_ \_ \_ \_ \_ \_ Attributo ID formato dei metadati degli oggetti audio spaziali MF mt \_

GUID definito dal decodificatore che identifica il formato dei metadati audio spaziali, inviando una notifica ai componenti downstream del tipo di oggetto di metadati che il decodificatore genererà come output.

## <a name="data-type"></a>Tipo di dati

**GUID**

## <a name="remarks"></a>Commenti

Il BLOB di metadati con il formato specificato viene scritto usando l'interfaccia [**ISpatialAudioMetadataWriter**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter) e viene letto usando l'interfaccia [**ISpatialAudioMetadataReader**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader) . Il BLOB dei metadati è opaco per i componenti e la pipeline Media Foundation. L'attributo viene applicato al tipo di supporti audio spaziali. Se un componente downstream non supporta il formato dei metadati specificato dal GUID, il componente deve rifiutare il tipo di supporto di input.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1703 \[\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 
