---
description: Elenca i valori restituiti del certificato e dell'attendibilità del certificato. Questi valori sono contenuti nel file di intestazione Winerror. h.
ms.assetid: f7d1bdcb-8e4f-493f-ad3c-9d4b9d21436b
title: Valori restituiti da certificati e trust
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e17f170c7c3aa1ac0839323b9a52767a101dd3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751074"
---
# <a name="certificate-and-trust-return-values"></a>Valori restituiti da certificati e trust

Nella tabella seguente sono elencati i valori restituiti dal certificato e dall'attendibilità del certificato. Questi valori sono contenuti nel file di intestazione Winerror. h.



| Nome                            | Descrizione                                                                                                                    | Valore      |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------|------------|
| CERTIFICATO \_ E \_ critico               | Un certificato contiene un'estensione sconosciuta contrassegnata come "critica".                                                         | 0x800B0105 |
| nome del certificato \_ E \_ non valido \_          | Il nome del certificato non è valido. Il nome non è incluso nell'elenco consentito oppure è escluso in modo esplicito. | 0x800B0114 |
| \_criterio certificato E \_ non valido \_        | Il certificato ha un criterio non valido.                                                                                | 0x800B0113 |
| CERTIFICATO \_ E \_ ISSUERCHAINING         | Un elemento padre di un determinato certificato non ha emesso il certificato figlio.                                                  | 0x800B0107 |
| CERTIFICATO \_ E \_ formato non valido              | Un certificato è mancante o ha un valore vuoto per un campo importante, ad esempio un oggetto o un nome di autorità emittente.                       | 0x800B0108 |
| CERTIFICATO \_ E \_ PATHLENCONST           | Un vincolo della lunghezza del percorso nella catena di certificazione è stato violato.                                                         | 0x800B0104 |
| CERTIFICATO \_ E \_ UNTRUSTEDCA            | Una catena di certificazione è stata elaborata correttamente, ma uno dei certificati della CA non è considerato attendibile dal provider di criteri.               | 0x800B0112 |
| CRYPT \_ E \_ nessun \_ controllo di revoca \_ | La funzione di revoca non è stata in grado di controllare la revoca del certificato.                                                    | 0x80092012 |
| TRUST \_ E \_ digest non valido \_           | La firma digitale dell'oggetto non è stata verificata.                                                                            | 0x80096010 |
| TRUST \_ E \_ vincoli di base \_    | L'estensione del vincolo di base di un certificato non è stata osservata.                                                         | 0x80096019 |
| firma ATTENDIBILe \_ E \_ certificato \_       | La firma del certificato non può essere verificata.                                                                           | 0x80096004 |
| TRUST \_ E \_ \_ firmatario contatore       | Una delle firme del contatore non è valida.                                                                                   | 0x80096003 |
| ATTENDIBILità \_ E non \_ \_ attendibilità esplicita    | Il certificato è stato contrassegnato in modo esplicito come non attendibile dall'utente.                                                                | 0x800B0111 |
| ATTENDIBILità \_ E \_ \_ criteri finanziari   | Il certificato non soddisfa o non contiene le estensioni finanziarie Authenticode.                                                | 0x8009601E |
| TRUST \_ E \_ nessun \_ certificato di firma \_      | Il certificato per il firmatario del messaggio non è valido o non è stato trovato.                                                       | 0x80096002 |
| \_errore di \_ sistema \_ E di attendibilità         | Si è verificato un errore a livello di sistema durante la verifica dell'attendibilità.                                                                           | 0x80096001 |
| timestamp di ATTENDIBILità \_ E \_ \_           | La firma con timestamp o il certificato non sono stati verificati oppure hanno un formato non corretto.                                                 | 0x80096005 |



 

 

 



