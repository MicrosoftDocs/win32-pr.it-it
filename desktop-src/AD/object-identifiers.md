---
title: Identificatori di oggetto (Ad DS)
description: Gli identificatori di oggetto (OID) sono valori numerici univoci emessi da varie autorità emittente per identificare in modo univoco gli elementi dati, le sintassi e altre parti delle applicazioni distribuite.
ms.assetid: a8f5a1c7-eda3-4430-b959-daef13c00a1b
ms.tgt_platform: multiple
keywords:
- identificatori di oggetto AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af458a003c5a5a8586c32449674019fb6b241d52c4300e107898d91c75047214
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185512"
---
# <a name="object-identifiers-ad-ds"></a>Identificatori di oggetto (Ad DS)

Gli identificatori di oggetto (OID) sono valori numerici univoci emessi da varie autorità emittente per identificare in modo univoco gli elementi dati, le sintassi e altre parti delle applicazioni distribuite. Gli OID si trovano in applicazioni OSI, directory X.500, SNMP e altre applicazioni in cui l'univocità è importante. Gli OID sono basati su una struttura ad albero, in cui un'autorità emittente superiore, ad esempio l'ISO, alloca un ramo dell'albero a una sottoautorità, che a sua volta può allocare sottobranchi.

Il protocollo LDAP (RFC 2251) richiede un servizio directory per identificare classi di oggetti, attributi e sintassi con OID. Fa parte della legacy LDAP X.500.

Gli OID in Active Directory Domain Services includono alcuni rilasciati dall'ISO per classi e attributi X.500 e altri rilasciati da Microsoft e altre autorità emittente. La notazione OID è una stringa tratteggiata di numeri, ad esempio "1.2.840.113556.1.5.9", descritta nella tabella seguente.



| Valore  | Significato          | Descrizione                                              |
|--------|------------------|----------------------------------------------------------|
| 1      | ISO              | Identifica l'autorità radice.                           |
| 2      | ANSI             | Designazione di gruppo assegnata da ISO.                       |
| 840    | USA              | Designazione del paese/area geografica assegnata dal gruppo.        |
| 113556 | Microsoft        | Designazione dell'organizzazione assegnata dal paese/area geografica. |
| 1      | Active Directory | Assegnato dall'organizzazione.                            |
| 5      | Classi          | Assegnato dall'organizzazione.                            |
| 9      | **classe** utente   | Assegnato dall'organizzazione.                            |



 

Per altre informazioni e per una descrizione di due procedure usate per ottenere OID validi da usare per l'estensione dello schema di Active Directory, vedere [Recupero di un](obtaining-an-object-identifier.md)identificatore di oggetto .

 

 




