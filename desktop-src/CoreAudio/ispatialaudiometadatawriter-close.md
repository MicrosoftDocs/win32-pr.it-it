---
description: Completa le operazioni necessarie sul buffer dei metadati e rilascia l'oggetto ISpatialAudioMetadataItems specificato.
ms.assetid: 2417E624-6535-49E2-9CF4-F927F731BE41
title: Metodo ISpatialAudioMetadataWriter::Close
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
ms.openlocfilehash: 4b29efb38cf11ba718a631f676323eb3db93aab042c70691dfb89ce957266e86
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875421"
---
# <a name="ispatialaudiometadatawriterclose-method"></a>Metodo ISpatialAudioMetadataWriter::Close

Completa le operazioni necessarie sul buffer dei metadati e rilascia [**l'oggetto ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems) specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Close();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce S \_ OK. In caso di esito negativo, i possibili codici restituiti includono, ma non sono limitati, i valori illustrati nella tabella seguente.



| Codice restituito                                                                                                                     | Descrizione                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SPTLAUD \_ MD \_ CLNT E NESSUN ELEMENTO \_ \_ \_ \_ APERTO**</dt> </dl>            | L'oggetto [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems) fornito non è stato aperto con una chiamata a [**Open.**](/windows/desktop/api/SpatialAudioMetadata/nf-spatialaudiometadata-ispatialaudiometadatawriter-open)<br/> |
| <dl> <dt>**SPTLAUD \_ MD \_ CLNT E NESSUN ELEMENTO \_ \_ \_ \_ SCRITTO**</dt> </dl>         | Non sono stati scritti elementi di metadati [**nell'oggetto ISpatialAudioMetadataItems fornito.**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems)<br/>                                              |
| <dl> <dt>**L'ELEMENTO CLNT E DI SPTLAUD \_ MD \_ DEVE AVERE \_ \_ \_ \_ \_ COMANDI**</dt> </dl> | Non sono stati scritti comandi di metadati [**nell'oggetto ISpatialAudioMetadataItems fornito.**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems)<br/>                                           |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISpatialAudioMetadataWriter**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadatawriter)
</dt> </dl>

 

 




