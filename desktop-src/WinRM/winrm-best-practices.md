---
title: Procedure consigliate di WinRM
description: In questo argomento vengono illustrate alcune delle procedure consigliate per l'utilizzo delle varie funzionalità dell'API WinRM.
ms.assetid: FC2CD030-199F-43C2-804E-9827EA2A46D5
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3452f2b8e61fb72b1fd5f99a073b48afb26dafb0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963135"
---
# <a name="winrm-best-practices"></a>Procedure consigliate di WinRM

In questo argomento vengono illustrate alcune delle procedure consigliate per l'utilizzo delle varie funzionalità dell'API WinRM.

## <a name="quotas"></a>Quote

Quando viene raggiunta una quota, il servizio gestione remota Windows restituisce un errore al client. Di conseguenza, la logica client deve ritentare in modo esplicito l'operazione in base all'errore restituito.

## <a name="event-subscriptions"></a>Sottoscrizioni di eventi

Quando si utilizzano le sottoscrizioni avviate da agente di raccolta, limitare il numero di computer remoti a 500 e isolare il servizio [raccolta eventi Windows](/windows/desktop/WEC/windows-event-collector) (wecsvc) in un processo host separato.

Un errore di connessione conterrà un thread finché non si verifica il timeout. Un numero elevato di errori di connessione simultanei può causare l'esaurimento del pool di thread e il rendering del server che non risponde.

 

 