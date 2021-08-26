---
description: GUID definito dal decodificatore che identifica il formato dei metadati audio spaziali, notificando ai componenti downstream del tipo di oggetto metadati che il decodificatore restituisce.
ms.assetid: 9714A2C7-25A1-4735-A0AC-22329ECBBC46
title: MF_MT_SPATIAL_AUDIO_OBJECT_METADATA_FORMAT_ID attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b43751655f2a583d50c8de3fe108babcaa08d11d78df552b6ddf1f10e413be8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955501"
---
# <a name="mf_mt_spatial_audio_object_metadata_format_id-attribute"></a>Attributo \_ MF MT \_ SPATIAL AUDIO OBJECT METADATA FORMAT \_ \_ \_ \_ \_ ID

GUID definito dal decodificatore che identifica il formato dei metadati audio spaziali, notificando ai componenti downstream del tipo di oggetto metadati che il decodificatore restituisce.

## <a name="data-type"></a>Tipo di dati

**GUID**

## <a name="remarks"></a>Commenti

Il BLOB di metadati con il formato specificato viene scritto usando [**l'interfaccia ISpatialAudioMetadataWriter**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatawriter) e letto usando l'interfaccia [**ISpatialAudioMetadataReader.**](/windows/win32/api/spatialaudiometadata/nn-spatialaudiometadata-ispatialaudiometadatareader) Il BLOB di metadati è opaco per la pipeline Media Foundation e i componenti. L'attributo viene applicato al tipo di supporto audio spaziale. Se un componente downstream non supporta il formato dei metadati specificato dal GUID, il componente deve rifiutare il tipo di supporto di input.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1703 \[\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



 

 
