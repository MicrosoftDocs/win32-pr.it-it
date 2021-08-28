---
title: Procedure consigliate per WinRM
description: Questo argomento illustra alcune delle procedure consigliate per l'uso delle varie funzionalità dell'API Gestione remota Windows.
ms.assetid: FC2CD030-199F-43C2-804E-9827EA2A46D5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dc780ec299c3249006085d348d983f8dab5b76a462c991a2d3665fed7d18f123
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733801"
---
# <a name="winrm-best-practices"></a>Procedure consigliate per WinRM

Questo argomento illustra alcune delle procedure consigliate per l'uso delle varie funzionalità dell'API Gestione remota Windows.

## <a name="quotas"></a>Quote

Quando viene raggiunta una quota, il servizio Gestione remota Windows restituisce un errore al client. Di conseguenza, la logica client deve ripetere in modo esplicito l'operazione in base all'errore restituito.

## <a name="event-subscriptions"></a>Sottoscrizioni di eventi

Quando si usano sottoscrizioni avviate dall'agente di raccolta, limitare il numero di computer remoti a 500 e isolare il servizio agente di raccolta eventi di [Windows](/windows/desktop/WEC/windows-event-collector) (wecsvc) in un processo host separato.

Un errore di connessione contenerà un thread fino al timeout. Un numero elevato di errori di connessione simultanei può causare l'esaurimento del pool di thread e il server non risponde.

 

 