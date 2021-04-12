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
# <a name="mf_mt_spatial_audio_object_metadata_length-attribute"></a>\_Attributo della \_ \_ \_ \_ lunghezza dei metadati dell'oggetto audio \_ spaziale MF mt

Valore che specifica la dimensione, in byte, del tipo di oggetto dei metadati audio spaziali che il decodificatore genererà come output.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Il BLOB di metadati con il formato specificato viene scritto usando l'interfaccia [**ISpatialAudioMetadataWriter**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter) e viene letto usando l'interfaccia [**ISpatialAudioMetadataReader**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader) . Il BLOB dei metadati è opaco per i componenti e la pipeline Media Foundation. L'attributo viene applicato al tipo di supporti audio spaziali.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1703 \[\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 
