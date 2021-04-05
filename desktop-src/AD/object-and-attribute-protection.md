---
title: Protezione di oggetti e attributi
description: Un elenco di controllo di accesso (ACL) protegge tutti gli oggetti in Active Directory Domain Services.
ms.assetid: 64ac1f88-57d6-4821-bd17-f7ef1004922c
ms.tgt_platform: multiple
keywords:
- Protezione di oggetti e attributi
- protezione di Active Directory, oggetti e attributi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c046df35740f21f8706120ee6e11cfad1d4f626
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707594"
---
# <a name="object-and-attribute-protection"></a>Protezione di oggetti e attributi

Un elenco di controllo di accesso (ACL) protegge tutti gli oggetti in Active Directory Domain Services. Gli ACL determinano gli utenti che possono visualizzare l'oggetto, gli attributi che possono leggere e le azioni che ogni utente può eseguire sull'oggetto. L'esistenza di un oggetto o di un attributo non viene mai rivelata a un utente non autorizzato.

Un ACL è un elenco di voci di controllo di accesso (ACE) archiviate con l'oggetto protetto. In Windows NT e Windows 2000, un ACL viene archiviato come valore binario, denominato descrittore di sicurezza. Ogni voce ACE contiene un ID di sicurezza (SID) che identifica l'entità (utente o gruppo) a cui si applica la voce ACE e i dati sul tipo di accesso concesso o negato dall'ACE.

Gli ACL per gli oggetti directory contengono ACE applicabili all'oggetto nel suo complesso e le voci ACE applicabili ai singoli attributi dell'oggetto. Questo consente a un amministratore di controllare non solo quali utenti possono visualizzare un oggetto, ma anche le proprietà che possono essere visualizzate dagli utenti. Ad esempio, a tutti gli utenti potrebbe essere concesso l'accesso in lettura agli attributi di posta elettronica e numero di telefono per tutti gli altri utenti, ma le proprietà di sicurezza degli utenti potrebbero essere negate a tutti i membri di un gruppo di amministratori della sicurezza speciale. Ai singoli utenti potrebbe essere concesso l'accesso in scrittura agli attributi personali, ad esempio il telefono e gli indirizzi di posta elettronica, sui rispettivi oggetti utente.

 

 




