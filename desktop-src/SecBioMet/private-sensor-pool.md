---
title: Pool di sensori privati
description: Raccolta di unità biometriche riservate per l'utilizzo esclusivo da un'applicazione client. I pool privati supportano i metodi di autenticazione proprietari e consentono a un'applicazione client di accedere a un'unità biometrica usando i comandi di controllo specificati dal fornitore.
ms.assetid: f0ccbafd-e7a8-4389-bd05-0b062dfc4dc0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf829290b0e412247b5e629a46e8c0efdafb4880
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221982"
---
# <a name="private-sensor-pool"></a>Pool di sensori privati

Un pool di sensori privati è una raccolta di unità biometriche riservate per l'uso esclusivo da un'applicazione client. I pool privati supportano i metodi di autenticazione proprietari e consentono a un'applicazione client di accedere a un'unità biometrica usando i comandi di controllo specificati dal fornitore. Unità biometriche in un pool di sensori privati:

-   Sono disponibili solo per l'applicazione client che ha creato il pool.
-   Inviare le notifiche degli eventi generati dal completamento delle operazioni biometriche direttamente all'applicazione senza considerare lo stato attivo della finestra corrente.
-   Usare i GUID per identificare i modelli biometrici.
-   Condividere un singolo database modello selezionato per l'applicazione.

I pool di sensori privati devono essere usati se l'applicazione client:

-   Gestisce una raccolta di unità biometriche dedicate che utilizzano un database modello specifico dell'applicazione. Per un esempio, si consideri un'applicazione per la partecipazione dei dipendenti in cui i dipendenti segnalano il proprio arrivo a lavoro scorrendo il dito su un lettore di impronte digitali. I dipendenti non dispongono di account di Windows nel computer in cui è in esecuzione l'applicazione. Le impronte digitali sono invece identificate dai GUID gestiti dall'applicazione di presenza.
-   Raccoglie i campioni biometrici anziché eseguire semplicemente il mapping degli esempi ai SID.
-   Inserisce l'hardware dell'unità biometrica in modalità manutenzione per aggiornare il firmware.
-   Invia comandi di controllo definiti dal fornitore all'hardware o al software dell'unità biometrica.
-   Tenta di configurare un'unità biometrica con lo spazio di archiviazione per il funzionamento in modalità avanzata ma l'unità non può eseguire le operazioni di hashing richieste.
-   Viene eseguito da una sessione client di Desktop remoto.

> [!Note]  
> Le applicazioni possono creare pool di sensori privati solo per la biometria delle impronte digitali. Se un'applicazione tenta di crearne una per qualsiasi altro elemento, ad esempio una faccia, la richiesta avrà esito negativo.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un pool di sensori privato](creating-a-private-sensor-pool.md)
</dt> <dt>

[Pool di sensori](sensor-pools.md)
</dt> <dt>

[Pool di sensori di sistema](system-sensor-pool.md)
</dt> </dl>

 

 




