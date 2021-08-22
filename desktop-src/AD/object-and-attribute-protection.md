---
title: Protezione di oggetti e attributi
description: Un elenco di controllo di accesso (ACL) protegge tutti gli oggetti in Active Directory Domain Services.
ms.assetid: 64ac1f88-57d6-4821-bd17-f7ef1004922c
ms.tgt_platform: multiple
keywords:
- Protezione di oggetti e attributi
- sicurezza di ACTIVE Directory, protezione di oggetti e attributi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7798ca1498c3a8ffe58bf43117dfd8ae249d234115f551c636628ad5b811e04a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025615"
---
# <a name="object-and-attribute-protection"></a>Protezione di oggetti e attributi

Un elenco di controllo di accesso (ACL) protegge tutti gli oggetti in Active Directory Domain Services. Gli ACL determinano chi può visualizzare l'oggetto, quali attributi possono leggere e quali azioni ogni utente può eseguire sull'oggetto. L'esistenza di un oggetto o di un attributo non viene mai rivelata a un utente non autorizzato.

Un ACL è un elenco di voci di controllo di accesso (ACE) archiviate con l'oggetto protetto. In Windows NT e Windows 2000, un ACL viene archiviato come valore binario, denominato descrittore di sicurezza. Ogni ACE contiene un ID di sicurezza (SID), che identifica l'entità (utente o gruppo) a cui si applica la ACE e i dati sul tipo di accesso concesso o negato dalla ACE.

Gli ACL per gli oggetti directory contengono ACE applicabili all'oggetto nel suo complesso e ACE applicabili ai singoli attributi dell'oggetto. In questo modo un amministratore può controllare non solo gli utenti che possono visualizzare un oggetto, ma anche le proprietà che gli utenti possono visualizzare. Ad esempio, a tutti gli utenti potrebbe essere concesso l'accesso in lettura agli attributi relativi alla posta elettronica e al numero di telefono per tutti gli altri utenti, ma le proprietà di sicurezza degli utenti potrebbero essere negate a tutti i membri di uno speciale gruppo di amministratori della sicurezza. Ai singoli utenti potrebbe essere concesso l'accesso in scrittura agli attributi personali, ad esempio gli indirizzi telefonici e postali nei propri oggetti utente.

 

 




