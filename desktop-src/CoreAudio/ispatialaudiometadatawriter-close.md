---
description: Completa tutte le operazioni necessarie sul buffer dei metadati e rilascia l'oggetto ISpatialAudioMetadataItems specificato.
ms.assetid: 2417E624-6535-49E2-9CF4-F927F731BE41
title: 'Metodo ISpatialAudioMetadataWriter:: Close'
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
ms.openlocfilehash: 719c0d156c616c623d3e9a0d8a78620b735a7151
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127311"
---
# <a name="ispatialaudiometadatawriterclose-method"></a>Metodo ISpatialAudioMetadataWriter:: Close

Completa tutte le operazioni necessarie sul buffer dei metadati e rilascia l'oggetto [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems) specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Close();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce S \_ OK. Se ha esito negativo, i codici restituiti possibili includono, ma non sono limitati, i valori mostrati nella tabella seguente.



| Codice restituito                                                                                                                     | Descrizione                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SPTLAUD \_ MD \_ CLNT \_ E \_ nessun \_ elemento \_ aperto**</dt> </dl>            | Il [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems) specificato non è stato aperto con una chiamata a [**Open**](/windows/desktop/api/SpatialAudioMetadata/nf-spatialaudiometadata-ispatialaudiometadatawriter-open).<br/> |
| <dl> <dt>**SPTLAUD \_ MD \_ CLNT \_ E \_ nessun \_ elemento \_ scritto**</dt> </dl>         | Nessun elemento di metadati scritto nel [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems)fornito.<br/>                                              |
| <dl> <dt>**l' \_ elemento SPTLAUD MD \_ CLNT \_ E \_ \_ deve \_ avere \_ comandi**</dt> </dl> | Nessun comando di metadati scritto nel [**ISpatialAudioMetadataItems**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadataitems)fornito.<br/>                                           |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISpatialAudioMetadataWriter**](/windows/desktop/api/SpatialAudioMetadata/nn-spatialaudiometadata-ispatialaudiometadatawriter)
</dt> </dl>

 

 




