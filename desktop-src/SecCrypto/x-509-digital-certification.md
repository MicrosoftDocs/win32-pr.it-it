---
description: La certificazione digitale prevede un processo per la firma del certificato. Questo processo è descritto.
ms.assetid: bb0382fd-2924-429f-933b-84ab61debf20
title: Certificazione digitale X.509
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f2f737a658e3e2c44876a23206f23a3d45ff3e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231699"
---
# <a name="x509-digital-certification"></a>Certificazione digitale X.509

Un'attività principale di un [*certificato digitale*](../secgloss/d-gly.md) consiste nel fornire l'accesso alla [*chiave pubblica*](../secgloss/p-gly.md)del soggetto. Il certificato conferma inoltre che la chiave pubblica del certificato appartiene al soggetto del certificato. Ad esempio, un' [*autorità di certificazione*](../secgloss/c-gly.md) (CA) può firmare digitalmente un messaggio speciale (le informazioni sul certificato) che contiene il nome di un utente, ad esempio "Alice" e la relativa chiave pubblica. Questa operazione deve essere eseguita in modo che chiunque possa verificare che il certificato sia stato emesso e firmato da un altro utente diverso dalla CA. Se la CA è attendibile ed è possibile verificare che il certificato di Alice sia stato emesso da tale autorità di certificazione, qualsiasi destinatario del certificato di Alice può considerare attendibile la chiave pubblica di Alice da tale certificato.

L'implementazione tipica della certificazione digitale prevede un processo per la firma del certificato.

Il processo è simile al seguente:

1.  Alice invia una [*richiesta di certificato*](../secgloss/c-gly.md) firmato contenente il nome, la chiave pubblica e probabilmente alcune informazioni aggiuntive a una CA.
2.  La CA crea un messaggio, *m*, dalla richiesta di Alice. La CA firma il messaggio con la relativa chiave privata, creando un messaggio di firma separato, *sig*. La CA restituisce il messaggio, *m* e la firma, *sig*, a Alice. Insieme, *m* e *sig* formano il certificato di Alice.
3.  Alice invia entrambe le parti del certificato a Bob per concedere l'accesso alla propria chiave pubblica.
4.  Bob verifica la firma, *sig* usando la chiave pubblica della CA. Se la firma è valida, accetta la chiave pubblica nel certificato come chiave pubblica di Alice.

Come per qualsiasi [*firma digitale*](../secgloss/d-gly.md), qualsiasi ricevitore con accesso alla chiave pubblica della CA può determinare se una CA specifica ha firmato il certificato. Questo processo non richiede l'accesso a informazioni segrete. Lo scenario appena presentato presuppone che Bob abbia accesso alla chiave pubblica dell'autorità di certificazione. Bob avrebbe accesso a tale chiave se ha una copia del certificato della CA che contiene la chiave pubblica.

I certificati digitali [*X. 509*](../secgloss/x-gly.md) includono non solo il nome e la chiave pubblica di un utente, ma anche altre informazioni sull'utente. Questi certificati sono più che l'esecuzione di calcoli in una gerarchia digitale di attendibilità. Consentono alla CA di fornire al destinatario del certificato un metodo per considerare attendibile non solo la chiave pubblica del soggetto del certificato, ma anche altre informazioni sul soggetto del certificato. Altre informazioni possono includere, tra le altre cose, un indirizzo di posta elettronica, un'autorizzazione per firmare i documenti di un determinato valore o l'autorizzazione a diventare un'autorità di certificazione e firmare altri certificati.

I certificati X. 509 e molti altri certificati hanno una durata di tempo valida. Un certificato può scadere e non essere più valido. Una CA può revocare un certificato per diversi motivi. Per gestire le revoche, un'autorità di certificazione gestisce e distribuisce un elenco di certificati revocati denominato [*elenco di revoche di certificati*](../secgloss/c-gly.md) (CRL). Gli utenti di rete accedono al CRL per determinare la validità di un certificato.

 

 
