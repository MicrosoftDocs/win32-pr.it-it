---
title: Identificatori di oggetto (AD DS)
description: Gli identificatori di oggetto (OID) sono valori numerici univoci emessi da varie autorità emittenti per identificare in modo univoco elementi dati, sintassi e altre parti di applicazioni distribuite.
ms.assetid: a8f5a1c7-eda3-4430-b959-daef13c00a1b
ms.tgt_platform: multiple
keywords:
- identificatori di oggetto AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2253a6173e06f5d7b0c136a520db3e1e5a5e798e
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/11/2019
ms.locfileid: "106299325"
---
# <a name="object-identifiers-ad-ds"></a>Identificatori di oggetto (AD DS)

Gli identificatori di oggetto (OID) sono valori numerici univoci emessi da varie autorità emittenti per identificare in modo univoco elementi dati, sintassi e altre parti di applicazioni distribuite. OID si trovano in applicazioni OSI, directory X. 500, SNMP e altre applicazioni in cui l'unicità è importante. OID sono basati su una struttura ad albero, in cui un'autorità emittente superiore, ad esempio l'immagine ISO, alloca un ramo della struttura ad albero a una sottoautorizzazione, che a sua volta può allocare sottorami.

Il protocollo LDAP (RFC 2251) richiede un servizio directory per identificare classi di oggetti, attributi e sintassi con OID. Questa operazione fa parte dell'Legacy X. 500 LDAP.

OID in Active Directory Domain Services includono alcuni rilasciati dall'ISO per le classi e gli attributi X. 500 e alcuni emessi da Microsoft e da altre autorità emittenti. La notazione OID è una stringa punteggiata di numeri, ad esempio "1.2.840.113556.1.5.9", descritta nella tabella seguente.



| Valore  | Significato          | Descrizione                                              |
|--------|------------------|----------------------------------------------------------|
| 1      | ISO              | Identifica l'autorità radice.                           |
| 2      | ANSI             | Designazione del gruppo assegnata da ISO.                       |
| 840    | USA              | Designazione del paese/area geografica assegnata dal gruppo.        |
| 113556 | Microsoft        | Designazione dell'organizzazione assegnata dal paese/area geografica. |
| 1      | Active Directory | Assegnati dall'organizzazione.                            |
| 5      | Classi          | Assegnati dall'organizzazione.                            |
| 9      | classe **User**   | Assegnati dall'organizzazione.                            |



 

Per ulteriori informazioni e per una descrizione di due procedure utilizzate per ottenere OID validi da usare per l'estensione dello schema di Active Directory, vedere [ottenere un identificatore di oggetto](obtaining-an-object-identifier.md).

 

 




