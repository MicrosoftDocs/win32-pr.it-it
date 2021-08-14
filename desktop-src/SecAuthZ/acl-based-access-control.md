---
description: Proprio come il sistema usa i descrittori di sicurezza per controllare l'accesso agli oggetti a protezione diretta, un server può usare i descrittori di sicurezza per controllare l'accesso ai relativi oggetti privati. Per altre informazioni sul modello di Windows sicurezza, vedere Modello di controllo di accesso.
ms.assetid: d6219438-711a-4eda-a893-9095bce3a07d
title: Controllo di accesso basato su ACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52867b78114474e1b7827bddf8fd17cd2f3fd71cd88b62cff25397e8bab9b4ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785166"
---
# <a name="acl-based-access-control"></a>Controllo di accesso basato su ACL

Proprio come il sistema [usa](security-descriptors.md) i descrittori di sicurezza per controllare l'accesso agli oggetti a protezione diretta, un server può usare i descrittori di sicurezza per controllare l'accesso ai relativi oggetti privati. Per altre informazioni sul modello di Windows di sicurezza, vedere [Modello di controllo di accesso](access-control-model.md).

Un server protetto può [creare un descrittore di sicurezza](security-descriptors-for-private-objects.md) con un elenco DACL che specifica i tipi di accesso consentiti per i diversi [fiduciari.](trustees.md) In un caso semplice, il server potrebbe creare un singolo descrittore di sicurezza per controllare [l'accesso](checking-access-to-private-objects.md)a tutti i dati e le funzionalità del server. Per una granularità più fine della protezione, il server può creare descrittori di sicurezza per ogni oggetto privato o per diversi tipi di funzionalità.

Ad esempio, quando un client chiede al server di creare un nuovo oggetto in un database, il server può creare un descrittore di sicurezza per il nuovo oggetto privato. Il server può quindi archiviare il descrittore di sicurezza con l'oggetto privato nel database. Quando un client tenta di accedere all'oggetto, il server recupera il descrittore di sicurezza per controllare i diritti di accesso del client. È importante notare che in un descrittore di sicurezza non è presente alcun elemento che lo associa all'oggetto o alla funzionalità che protegge. È invece il server protetto a mantenere l'associazione.

È anche possibile controllare l'accesso all'oggetto privato. Per una [descrizione, vedere Controllo](auditing-access-to-private-objects.md) dell'accesso agli oggetti privati.

 

 



