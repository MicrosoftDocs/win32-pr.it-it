---
title: Classe StreamSelectOperation
description: Registra un gestore eventi che viene richiamato al completamento dell'operazione asincrona avviata da GetMuteAsync e fornisce un metodo che restituisce i risultati dell'operazione. | Classe StreamSelectOperation
ms.assetid: 681142B4-AECD-42D0-A2D4-494E69A29025
keywords:
- API di streaming multimediale della classe StreamSelectOperation
- API di streaming multimediale della classe StreamSelectOperation, descritta
topic_type:
- apiref
api_name:
- StreamSelectOperation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a4a19ff2826f0f2ea3e5ef01841ce482d2f293a3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104234791"
---
# <a name="streamselectoperation-class"></a>Classe StreamSelectOperation

Registra un gestore eventi che viene richiamato al completamento dell'operazione asincrona avviata da [**GetMuteAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-getmuteasync) e fornisce un metodo che restituisce i risultati dell'operazione.

**StreamSelectOperation** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe **StreamSelectOperation** dispone di questi metodi.



| Metodo                                                 | Descrizione                                                                                                                                       |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetResults**](streamselectoperation-getresults.md) | Restituisce i risultati dell'operazione asincrona avviata da [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)).<br/> |



 

### <a name="properties"></a>Proprietà

La classe **StreamSelectOperation** dispone di queste proprietà.



| Proprietà                                                        | Tipo di accesso           | Descrizione                                                                                                                                                                             |
|:----------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Completi**](streamselectoperation-completed.md)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta un gestore eventi che viene richiamato quando viene completata l'operazione asincrona avviata da [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829002(v=vs.85)) .<br/> |



 

 

