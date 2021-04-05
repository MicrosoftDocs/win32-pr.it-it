---
description: Così come il sistema usa i descrittori di sicurezza per controllare l'accesso agli oggetti a protezione diretta, un server può usare i descrittori di sicurezza per controllare l'accesso ai relativi oggetti privati. Per altre informazioni sul modello di sicurezza di Windows, vedere modello di controllo di accesso.
ms.assetid: d6219438-711a-4eda-a893-9095bce3a07d
title: Controllo degli accessi basato su ACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b477f998b7866c66860b94c3ff1266392f49373
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756183"
---
# <a name="acl-based-access-control"></a>Controllo degli accessi basato su ACL

Così come il sistema usa i [descrittori di sicurezza](security-descriptors.md) per controllare l'accesso agli oggetti a protezione diretta, un server può usare i descrittori di sicurezza per controllare l'accesso ai relativi oggetti privati. Per altre informazioni sul modello di sicurezza di Windows, vedere [modello di controllo di accesso](access-control-model.md).

Un server protetto può [creare un descrittore di sicurezza](security-descriptors-for-private-objects.md) con un DACL che specifica i tipi di accesso consentiti per diversi [trustee](trustees.md). In un caso semplice, il server potrebbe creare un singolo descrittore di sicurezza per [controllare l'accesso a tutti i dati e le funzionalità del server](checking-access-to-private-objects.md). Per una maggiore granularità della protezione, il server può creare descrittori di sicurezza per ognuno dei relativi oggetti privati o per diversi tipi di funzionalità.

Ad esempio, quando un client richiede al server di creare un nuovo oggetto in un database, il server potrebbe creare un descrittore di sicurezza per il nuovo oggetto privato. Il server potrebbe quindi archiviare il descrittore di sicurezza con l'oggetto privato nel database. Quando un client tenta di accedere all'oggetto, il server recupera il descrittore di sicurezza per verificare i diritti di accesso del client. È importante notare che non c'è nulla in un descrittore di sicurezza che lo associa all'oggetto o alla funzionalità da proteggere. Al contrario, spetta al server protetto mantenere l'associazione.

È anche possibile controllare l'accesso all'oggetto privato. Per una descrizione di questo articolo, vedere [controllo dell'accesso a oggetti privati](auditing-access-to-private-objects.md) .

 

 



