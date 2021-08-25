---
description: Come i certificati digitali forniscono comunicazioni protette e come usare CryptoAPI per usare e gestire tali certificati.
ms.assetid: e523b335-0156-4f47-b55c-b80495587c4f
title: Certificati digitali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 467f2df1a529d94fa5a04385c7f91f5aefbb40c0488ef0c5c484fe98c3874358
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119875301"
---
# <a name="digital-certificates"></a>Certificati digitali

L'autenticazione è fondamentale per proteggere le comunicazioni. Gli utenti devono essere in grado di dimostrare la propria identità a coloro con cui comunicano e devono essere in grado di verificare l'identità di altri utenti. L'autenticazione dell'identità su una rete è un processo complesso poiché in questo tipo di comunicazione non esiste un riscontro fisico tra i partecipanti. Ciò potrebbe dar modo a soggetti malintenzionati di intercettare i messaggi o assumere l'identità di un'altra persona o entità. È necessario elaborare un metodo per mantenere il livello di attendibilità necessario all'interno del processo di comunicazione.

Il [*certificato digitale*](../secgloss/c-gly.md) è una credenziale comune che consente di verificare l'identità. Questa sezione offre una panoramica del modo in cui i certificati forniscono comunicazioni protette e di come usare CryptoAPI per usare e gestire tali certificati.

Un certificato è un set di dati che identifica un'entità. Un'organizzazione attendibile assegna un certificato a una persona o a un'entità che associa una chiave pubblica all'utente. La persona o l'entità a cui viene emesso un certificato è denominata oggetto di tale certificato. L'organizzazione attendibile che emettere il certificato è un'autorità [*di*](../secgloss/c-gly.md) certificazione (CA) ed è nota come autorità emittente del certificato. Una CA attendibile emettere un certificato solo dopo aver verificato l'identità del soggetto del certificato.

I certificati usano tecniche crittografiche per risolvere il problema della mancanza di contatto fisico tra gli utenti che comunicano. L'uso di queste tecniche limita la possibilità di intercettazione, modifica o contraffazione di messaggi da parte di una persona non etica. Queste tecniche di crittografia rendono i certificati difficili da modificare. Di conseguenza, è difficile per un'entità rappresentare un altro utente.

I dati in un certificato includono la chiave crittografica pubblica della coppia di chiavi [*pubblica/privata*](../secgloss/p-gly.md)del soggetto del certificato. Un messaggio firmato con la chiave privata del mittente può essere recuperato solo dal destinatario del messaggio usando la chiave pubblica del mittente. Questa chiave è disponibile in una copia del certificato del mittente. Il recupero di una firma con [*una*](../secgloss/p-gly.md) chiave pubblica da un certificato dimostra che la firma è stata prodotta usando la chiave privata del soggetto [*del certificato.*](../secgloss/p-gly.md) Se il mittente è stato vigile e ha mantenuto il segreto della chiave privata, il ricevitore può essere sicuro dell'identità del mittente del messaggio.

In una rete è spesso presente un'applicazione attendibile nota come [*server dei certificati*](../secgloss/c-gly.md). Un'autorità di certificazione in esecuzione in un computer sicuro gestisce il server dei certificati. Questa applicazione ha accesso alla chiave pubblica di tutti i client. I server dei certificati erogano messaggi noti come certificati, ognuno dei quali contiene la chiave pubblica di uno degli utenti client. Ogni certificato viene firmato con la chiave privata della CA. Il destinatario di un certificato di questo tipo può quindi verificare che sia stato inviato da una CA specificata.

I certificati digitali includono anche estensioni e proprietà estese che forniscono informazioni aggiuntive sul soggetto del certificato, ad esempio l'indirizzo di posta elettronica del soggetto e le attività che il soggetto del certificato può eseguire.

 

 
