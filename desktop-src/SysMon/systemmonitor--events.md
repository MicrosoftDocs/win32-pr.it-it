---
title: Eventi SystemMonitor
description: La classe SystemMonitor presenta gli eventi seguenti
ms.assetid: 64d9befd-5ea0-4888-b0fb-cff889f1d188
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 94247cf81fcaf57f373c731cd4eaf06a3ca897ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297635"
---
# <a name="systemmonitor-events"></a>Eventi SystemMonitor

La classe [**SystemMonitor**](systemmonitor.md) presenta gli eventi seguenti:

-   [**OnCounterAdded**](systemmonitor-oncounteradded.md)
-   [**OnCounterDeleted**](-systemmonitor-oncounterdeleted.md)
-   [**OnCounterSelected**](-systemmonitor-oncounterselected.md)
-   [**OnDblClick**](-systemmonitor-ondblclick.md)
-   [**OnSampleCollected**](-systemmonitor-onsamplecollected.md)

> [!Note]  
> È necessario restituire dal gestore eventi prima della scadenza dell' [**intervallo di aggiornamento**](systemmonitor-updateinterval.md) ; in caso contrario, SYSMON Visualizza una finestra di messaggio che indica all'utente che non è stato possibile campionare i valori dei contatori per l'intervallo di aggiornamento precedente.

 

 

 




