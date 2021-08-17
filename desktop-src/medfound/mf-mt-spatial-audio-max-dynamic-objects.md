---
description: Specifica il numero massimo di oggetti audio dinamici di cui l'endpoint audio può eseguire il rendering in modo simulato.
ms.assetid: 6B6D73C1-C2E6-4C23-BBAD-7B51E8441C71
title: MF_MT_SPATIAL_AUDIO_MAX_DYNAMIC_OBJECTS attributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42ae239354076dae309ba9e1c63f9c19b408994958b2523a2c0e170f460188e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104397"
---
# <a name="mf_mt_spatial_audio_max_dynamic_objects-attribute"></a>Attributo \_ MF MT \_ SPATIAL AUDIO MAX DYNAMIC \_ \_ \_ \_ OBJECTS

Specifica il numero massimo di oggetti audio dinamici di cui l'endpoint audio può eseguire il rendering in modo simulato.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="remarks"></a>Commenti

Un [**oggetto IMFSpatialAudioSample**](/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudiosample) può contenere un numero di campioni inferiore al numero specificato da questo attributo. Se un esempio contiene più oggetti audio di quelli specificati da questo attributo, il comportamento non è definito.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1703 \[\]<br/>                          |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



 

 




