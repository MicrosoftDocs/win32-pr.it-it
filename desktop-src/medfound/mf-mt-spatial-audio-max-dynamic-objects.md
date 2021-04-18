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
# <a name="mf_mt_spatial_audio_max_dynamic_objects-attribute"></a>\_ \_ \_ \_ \_ \_ Attributo massimo oggetti dinamici di MF mt spatial audio

Specifica il numero massimo di oggetti audio dinamici che possono essere sottoposti a rendering dall'endpoint audio simulataneously.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Un [**IMFSpatialAudioSample**](/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudiosample) può contenere un numero di campioni inferiore al numero specificato da questo attributo. Se un esempio contiene più oggetti audio rispetto a quanto specificato da questo attributo, il comportamento non è definito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1703 \[\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



 

 




