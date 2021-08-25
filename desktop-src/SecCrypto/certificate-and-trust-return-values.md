---
description: Elenca i valori restituiti dal certificato e dall'attendibilità del certificato. Questi valori sono contenuti nel file di intestazione Winerror.h.
ms.assetid: f7d1bdcb-8e4f-493f-ad3c-9d4b9d21436b
title: Valori restituiti da certificati e attendibilità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf575df785160682c132f38ccc280bb8b9377b15b64ed3efda163c68c1ef52e0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127241"
---
# <a name="certificate-and-trust-return-values"></a>Valori restituiti da certificati e attendibilità

Nella tabella seguente sono elencati i valori restituiti dal certificato e dall'attendibilità del certificato. Questi valori sono contenuti nel file di intestazione Winerror.h.



| Nome                            | Descrizione                                                                                                                    | Valore      |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------|------------|
| CERT \_ E \_ CRITICAL               | Un certificato contiene un'estensione sconosciuta contrassegnata come "critica".                                                         | 0x800B0105 |
| NOME CERT \_ E \_ NON \_ VALIDO          | Il nome del certificato non è valido. Il nome non è incluso nell'elenco consentito oppure è escluso in modo esplicito. | 0x800B0114 |
| CRITERIO CERT \_ E \_ NON \_ VALIDO        | Il certificato ha criteri non validi.                                                                                | 0x800B0113 |
| CERT \_ E \_ ISSUERCHAINING         | Un elemento padre di un determinato certificato non ha infatti emettere tale certificato figlio.                                                  | 0x800B0107 |
| CERT \_ E IN FORMATO NON \_ VALIDO              | Un certificato è mancante o ha un valore vuoto per un campo importante, ad esempio un oggetto o un nome dell'autorità emittente.                       | 0x800B0108 |
| CERT \_ E \_ PATHLENCONST           | Un vincolo della lunghezza del percorso nella catena di certificazione è stato violato.                                                         | 0x800B0104 |
| CERT \_ E \_ UNTRUSTEDCA            | Una catena di certificazione elaborata correttamente, ma uno dei certificati ca non è considerato attendibile dal provider di criteri.               | 0x800B0112 |
| CRYPT \_ E NESSUN CONTROLLO DI \_ \_ REVOCA \_ | La funzione di revoca non è stata in grado di controllare la revoca del certificato.                                                    | 0x80092012 |
| TRUST \_ E \_ BAD \_ DIGEST           | La firma digitale dell'oggetto non è stata verificata.                                                                            | 0x80096010 |
| VINCOLI DI BASE DI TRUST \_ E \_ \_    | L'estensione del vincolo di base di un certificato non è stata osservata.                                                         | 0x80096019 |
| TRUST \_ E \_ CERT \_ SIGNATURE       | La firma del certificato non può essere verificata.                                                                           | 0x80096004 |
| TRUST \_ E \_ COUNTER \_ SIGNER       | Una delle firme del contatore non è valida.                                                                                   | 0x80096003 |
| TRUST \_ E \_ EXPLICIT \_ DISTRUST    | Il certificato è stato contrassegnato in modo esplicito come non attendibile dall'utente.                                                                | 0x800B0111 |
| TRUST \_ E \_ CRITERI \_ FINANZIARI   | Il certificato non soddisfa o contiene le estensioni finanziarie Authenticode.                                                | 0x8009601E |
| TRUST \_ E \_ NO \_ SIGNER \_ CERT      | Il certificato per il firmatario del messaggio non è valido o non è stato trovato.                                                       | 0x80096002 |
| ERRORE \_ DI SISTEMA \_ TRUST E \_         | Si è verificato un errore a livello di sistema durante la verifica dell'attendibilità.                                                                           | 0x80096001 |
| TIMESTAMP \_ TRUST E \_ \_           | La firma con timestamp o il certificato non sono stati verificati oppure hanno un formato non corretto.                                                 | 0x80096005 |



 

 

 



