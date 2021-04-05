---
description: Il modo in cui i certificati digitali forniscono comunicazioni sicure e come usare CryptoAPI per usare e gestire tali certificati.
ms.assetid: e523b335-0156-4f47-b55c-b80495587c4f
title: Certificati digitali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 161d200a0f8cab61594872f5182786a3e6597187
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750903"
---
# <a name="digital-certificates"></a>Certificati digitali

L'autenticazione è fondamentale per proteggere le comunicazioni. Gli utenti devono essere in grado di dimostrare la propria identità a coloro che comunicano e devono essere in grado di verificare l'identità di altri utenti. L'autenticazione dell'identità su una rete è un processo complesso poiché in questo tipo di comunicazione non esiste un riscontro fisico tra i partecipanti. Ciò potrebbe dar modo a soggetti malintenzionati di intercettare i messaggi o assumere l'identità di un'altra persona o entità. Per mantenere il livello di attendibilità necessario all'interno del processo di comunicazione, è necessario elaborare un metodo.

Il [*certificato digitale*](../secgloss/c-gly.md) è una credenziale comune che fornisce un mezzo per verificare l'identità. Questa sezione fornisce una panoramica del modo in cui i certificati forniscono comunicazioni sicure e come usare CryptoAPI per usare e gestire tali certificati.

Un certificato è un set di dati che identifica un'entità. Un'organizzazione attendibile assegna un certificato a una persona o a un'entità che associa una chiave pubblica a una persona. La persona o l'entità a cui viene emesso un certificato viene chiamata oggetto del certificato. L'organizzazione attendibile che rilascia il certificato è un' [*autorità di certificazione*](../secgloss/c-gly.md) (CA) ed è nota come emittente del certificato. Una CA attendibile emetterà un certificato solo dopo la verifica dell'identità del soggetto del certificato.

I certificati utilizzano le tecniche di crittografia per risolvere il problema della mancanza di contatto fisico tra i due utenti che comunicano. L'utilizzo di queste tecniche limita la possibilità che un utente non etico intercettare, modificare o falsificare messaggi. Queste tecniche crittografiche rendono i certificati difficili da modificare. Pertanto, è difficile per un'entità rappresentare un altro utente.

I dati di un certificato includono la chiave crittografica pubblica dalla [*coppia di chiavi pubblica/privata*](../secgloss/p-gly.md)del soggetto del certificato. Un messaggio firmato con la chiave privata del mittente può essere recuperato solo dal destinatario del messaggio utilizzando la chiave pubblica del mittente. Questa chiave si trova in una copia del certificato del mittente. Il recupero di una firma con una [*chiave pubblica*](../secgloss/p-gly.md) da un certificato dimostra che la firma è stata prodotta usando la [*chiave privata*](../secgloss/p-gly.md)del soggetto del certificato. Se il mittente è stato vigile e ha mantenuto il segreto della chiave privata, il destinatario può essere sicuro nell'identità del mittente del messaggio.

In una rete è spesso presente un'applicazione attendibile nota come [*server di certificati*](../secgloss/c-gly.md). Una CA in esecuzione su un computer protetto gestisce il server dei certificati. Questa applicazione ha accesso alla chiave pubblica di tutti i relativi client. I server di certificazione dispensano i messaggi noti come certificati, ognuno dei quali contiene la chiave pubblica di uno dei relativi utenti client. Ogni certificato è firmato con la chiave privata della CA. Pertanto, il destinatario di un certificato di questo tipo può verificare che sia stato inviato da una CA specificata.

I certificati digitali includono anche le estensioni e le proprietà estese che forniscono informazioni aggiuntive sull'oggetto del certificato, ad esempio l'indirizzo di posta elettronica dell'oggetto e le attività che possono essere eseguite dal soggetto del certificato.

 

 
