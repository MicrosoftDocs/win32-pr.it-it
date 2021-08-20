---
description: Valore che specifica le dimensioni, in byte, del tipo di oggetto dei metadati audio spaziali restituito dal decodificatore.
ms.assetid: C133693D-A8D5-4520-B561-57BF11074257
title: MF_MT_SPATIAL_AUDIO_OBJECT_METADATA_LENGTH attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 784e1b210b616f4c42c2c3d410a207adc9c8c8ccaf751432cb027a7cc30cf951
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117876812"
---
# <a name="mf_mt_spatial_audio_object_metadata_length-attribute"></a>Attributo \_ MF MT \_ SPATIAL AUDIO OBJECT METADATA \_ \_ \_ \_ LENGTH

Valore che specifica le dimensioni, in byte, del tipo di oggetto dei metadati audio spaziali restituito dal decodificatore.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Il BLOB di metadati con il formato specificato viene scritto usando [**l'interfaccia ISpatialAudioMetadataWriter**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter) e letto usando l'interfaccia [**ISpatialAudioMetadataReader.**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader) Il BLOB di metadati è opaco per la pipeline Media Foundation e i componenti. L'attributo viene applicato al tipo di supporto audio spaziale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1703 \[\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



 

 
