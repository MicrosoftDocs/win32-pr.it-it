---
title: Classe StreamSelectOperation
description: Registra un gestore eventi che viene richiamato al completamento dell'operazione asincrona avviata da GetMuteAsync e fornisce un metodo che restituisce i risultati dell'operazione. | Classe StreamSelectOperation
ms.assetid: 681142B4-AECD-42D0-A2D4-494E69A29025
keywords:
- CLASSE StreamSelectOperation API Streaming multimediale
- Classe StreamSelectOperation API Streaming multimediale, descritta
topic_type:
- apiref
api_name:
- StreamSelectOperation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 161434aad9c4eb20960950ba2dd1979c9caaa2ccc5bbe3c2683ee3e4f839a0b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461561"
---
# <a name="streamselectoperation-class"></a>Classe StreamSelectOperation

Registra un gestore eventi che viene richiamato al completamento dell'operazione asincrona avviata da [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync) e fornisce un metodo che restituisce i risultati dell'operazione.

**StreamSelectOperation** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe StreamSelectOperation** include questi metodi.



| Metodo                                                 | Descrizione                                                                                                                                       |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetResults**](streamselectoperation-getresults.md) | Restituisce i risultati dell'operazione asincrona avviata [**da SelectBestStreamAsync.**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85))<br/> |



 

### <a name="properties"></a>Proprietà

La **classe StreamSelectOperation** ha queste proprietà.



| Proprietà                                                        | Tipo di accesso           | Descrizione                                                                                                                                                                             |
|:----------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Completi**](streamselectoperation-completed.md)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta un gestore eventi richiamato quando viene completata l'operazione asincrona avviata da [**SelectBestStreamAsync.**](/previous-versions/windows/desktop/legacy/hh829002(v=vs.85))<br/> |



 

 

