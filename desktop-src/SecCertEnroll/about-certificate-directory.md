---
description: Un Windows'infrastruttura a chiave pubblica (PKI) salva i certificati nel server che ospita l'autorità di certificazione (CA) e nel computer locale o nel dispositivo.
ms.assetid: b6aaafeb-30d1-453e-a70c-dcaa01fea1cf
title: Directory certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b77a7c63e234460394005aac416d41ff7845470139ba2cb8b700132bea0118c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904830"
---
# <a name="certificate-directory"></a>Directory certificati

Un Windows'infrastruttura a chiave pubblica (PKI) salva i certificati nel server che ospita l'autorità di certificazione (CA) e nel computer locale o nel dispositivo. L'archiviazione CA viene in genere definita database dei certificati e l'archiviazione locale è nota come archivio certificati.

## <a name="certificate-database"></a>Database dei certificati

Quando si aggiungono Servizi certificati in un server Windows e si configura una CA, viene creato un database dei certificati. Per impostazione predefinita, il database è contenuto nella cartella *%SystemRoot%* \\ System32 Certlog e il nome è basato sul nome della CA con estensione \\ edb. Il database può contenere:

-   Certificati rilasciati
-   Certificati revocati
-   Chiavi private archiviate
-   Richieste di certificati

Non è possibile usare l'API di registrazione certificati per modificare il database. Il processo di registrazione crea automaticamente le voci necessarie.

## <a name="certificate-stores"></a>Archivi certificati

Servizi certificati Microsoft copia i certificati emessi e le richieste in sospeso o rifiutate a computer e dispositivi locali. Il percorso di archiviazione è denominato archivio certificati ed è costituito dai seguenti archivi logici.

| Archivio logico                                         | Descrizione                                                                                                            |
|-------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Personal<br/>                                   | Contiene i certificati associati a una chiave privata controllata dall'utente o dal computer.<br/>                     |
| Autorità di certificazione radice disponibile nell'elenco locale<br/>     | Contiene i certificati provenienti da autorità di certificazione (CA) implicitamente attendibili.<br/>                              |
| Attendibilità per l'organizzazione<br/>                           | Contiene elenchi di certificati attendibili in genere usati per considerare attendibili i certificati autofirmati di altre organizzazioni.<br/> |
| Autorità di certificazione intermedie<br/>     | Contiene i certificati rilasciati alle CA subordinate nella gerarchia di certificazione.<br/>                             |
| Oggetto utente Active Directory<br/>               | Contiene il certificato dell'oggetto utente o i certificati pubblicati in Active Directory.<br/>                         |
| Autori attendibili<br/>                         | Contiene i certificati provenienti da AUTORITÀ di certificazione attendibili.<br/>                                                                     |
| Certificati non disponibili nell'elenco locale<br/>                     | Contiene i certificati identificati in modo esplicito come non attendibili.<br/>                                    |
| CA principali di terze parti<br/> | Contiene certificati radice trusted provenienti da CA esterne alla gerarchia di certificati interna.<br/>                     |
| Persone attendibili<br/>                             | Contiene i certificati rilasciati a utenti o entità che sono state esplicitamente attendibili.<br/>                        |
| Altri utenti<br/>                               | Contiene i certificati rilasciati a utenti o entità considerati implicitamente attendibili.<br/>                        |
| Richieste di registrazione dei certificati<br/>            | Contiene le richieste di certificato in sospeso o rifiutate.<br/>                                                          |



 

Non è possibile usare l'API di registrazione certificati per specificare o recuperare le proprietà dell'archivio o copiare i certificati in archivi specifici.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Elementi PKI](about-pki-components.md)
</dt> </dl>

 

 




