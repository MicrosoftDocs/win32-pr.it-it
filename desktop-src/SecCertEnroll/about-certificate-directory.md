---
description: Un'infrastruttura a chiave pubblica (PKI) di Windows salva i certificati sul server che ospita l'autorità di certificazione (CA) e sul computer locale o sul dispositivo.
ms.assetid: b6aaafeb-30d1-453e-a70c-dcaa01fea1cf
title: Directory certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee525e4d910de1c75516c6aaa27ca41a6cfa17c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234170"
---
# <a name="certificate-directory"></a>Directory certificati

Un'infrastruttura a chiave pubblica (PKI) di Windows salva i certificati sul server che ospita l'autorità di certificazione (CA) e sul computer locale o sul dispositivo. L'archiviazione CA viene in genere definita database dei certificati e l'archiviazione locale è nota come archivio certificati.

## <a name="certificate-database"></a>Database di certificati

Quando si aggiungono servizi certificati in un server Windows e si configura una CA, viene creato un database di certificati. Per impostazione predefinita, il database è contenuto nella cartella *% systemroot%* \\ system32 \\ certlog e il nome è basato sul nome della CA con estensione edb. Il database può contenere:

-   Certificati emessi
-   Certificati revocati
-   Chiavi private archiviate
-   Richieste di certificati

Non è possibile usare l'API di registrazione del certificato per modificare il database. Il processo di registrazione crea automaticamente le voci necessarie.

## <a name="certificate-stores"></a>Archivi certificati

Servizi certificati Microsoft copia i certificati emessi e le richieste in sospeso o rifiutate a computer e dispositivi locali. Il percorso di archiviazione è denominato archivio certificati ed è costituito dai seguenti archivi logici.

| Archivio logico                                         | Descrizione                                                                                                            |
|-------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Personal<br/>                                   | Contiene i certificati associati a una chiave privata controllata dall'utente o dal computer.<br/>                     |
| Autorità di certificazione radice disponibile nell'elenco locale<br/>     | Contiene i certificati delle autorità di certificazione (CAs) implicitamente attendibili.<br/>                              |
| Attendibilità per l'organizzazione<br/>                           | Contiene elenchi di certificati attendibili in genere utilizzati per considerare attendibili i certificati autofirmati di altre organizzazioni.<br/> |
| Autorità di certificazione intermedie<br/>     | Contiene i certificati emessi per le CA subordinate nella gerarchia di certificazione.<br/>                             |
| Oggetto utente Active Directory<br/>               | Contiene il certificato dell'oggetto utente o i certificati pubblicati in Active Directory.<br/>                         |
| Autori attendibili<br/>                         | Contiene certificati provenienti da autorità di certificazione attendibili.<br/>                                                                     |
| Certificati non disponibili nell'elenco locale<br/>                     | Contiene i certificati che sono stati identificati in modo esplicito come non attendibili.<br/>                                    |
| CA principali di terze parti<br/> | Contiene certificati radice attendibili provenienti da autorità di certificazione esterne alla gerarchia di certificati interna.<br/>                     |
| Persone attendibili<br/>                             | Contiene i certificati rilasciati a utenti o entità che sono stati esplicitamente attendibili.<br/>                        |
| Altri utenti<br/>                               | Contiene i certificati rilasciati a utenti o entità considerati implicitamente attendibili.<br/>                        |
| Richieste di registrazione dei certificati<br/>            | Contiene richieste di certificato in sospeso o rifiutate.<br/>                                                          |



 

Non è possibile usare l'API di registrazione certificati per specificare o recuperare le proprietà dell'archivio o copiare i certificati in archivi specifici.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Elementi PKI](about-pki-components.md)
</dt> </dl>

 

 




