---
title: Eventi di SystemMonitor
description: 'La classe SystemMonitor include gli eventi seguenti:'
ms.assetid: 64d9befd-5ea0-4888-b0fb-cff889f1d188
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c3584eed86abcaef019f0fc8f8bd794a80abca1143286317189889231bbc2cc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882947"
---
# <a name="systemmonitor-events"></a>Eventi di SystemMonitor

La [**classe SystemMonitor**](systemmonitor.md) include gli eventi seguenti:

-   [**OnCounterAdded**](systemmonitor-oncounteradded.md)
-   [**OnCounterDeleted**](-systemmonitor-oncounterdeleted.md)
-   [**OnCounterSelected**](-systemmonitor-oncounterselected.md)
-   [**OnDblClick**](-systemmonitor-ondblclick.md)
-   [**OnSampleCollected**](-systemmonitor-onsamplecollected.md)

> [!Note]  
> È necessario restituire dal gestore eventi prima della scadenza [**dell'intervallo**](systemmonitor-updateinterval.md) di aggiornamento. In caso contrario, SYSMON visualizza una finestra di messaggio che indica all'utente che non è stato possibile campionare i valori dei contatori per l'intervallo di aggiornamento precedente.

 

 

 




