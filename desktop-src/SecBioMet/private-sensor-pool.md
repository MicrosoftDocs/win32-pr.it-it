---
title: Pool di sensori privati
description: Raccolta di unità biometriche riservate per l'uso esclusivo da parte di un'applicazione client. I pool privati supportano metodi di autenticazione proprietari e consentono a un'applicazione client di accedere a un'unità biometrica usando i comandi di controllo specificati dal fornitore.
ms.assetid: f0ccbafd-e7a8-4389-bd05-0b062dfc4dc0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 306f4e0d4e28cfb29dda694e835348721113a5c23ec51054169537282ae2c365
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119480441"
---
# <a name="private-sensor-pool"></a>Pool di sensori privati

Un pool di sensori privato è una raccolta di unità biometriche riservate per l'uso esclusivo da parte di un'applicazione client. I pool privati supportano metodi di autenticazione proprietari e consentono a un'applicazione client di accedere a un'unità biometrica usando i comandi di controllo specificati dal fornitore. Unità biometriche in un pool di sensori privato:

-   Sono disponibili solo per l'applicazione client che ha creato il pool.
-   Inviare le notifiche degli eventi generate dal completamento delle operazioni biometriche direttamente all'applicazione, indipendentemente dallo stato attivo della finestra corrente.
-   Usare i GUID per identificare i modelli biometrici.
-   Condividere un singolo database modello selezionato dall'applicazione.

È necessario usare pool di sensori privati se l'applicazione client:

-   Gestisce una raccolta di unità biometriche dedicate che usano un database modello specifico dell'applicazione. Si consideri ad esempio un'applicazione di frequenza dei dipendenti in cui i dipendenti segnalano l'arrivo al lavoro scorrendo il dito su un lettore di impronta digitale. I dipendenti non hanno account Windows nel computer che esegue l'applicazione. Al contrario, le impronte digitali sono identificate da GUID gestiti dall'applicazione attendance.
-   Raccoglie campioni biometrici invece di eseguire semplicemente il mapping dei campioni ai SID.
-   Attiva la modalità di manutenzione dell'hardware dell'unità biometrica per aggiornare il firmware.
-   Invia comandi di controllo definiti dal fornitore all'hardware o al software dell'unità biometrica.
-   Tenta di configurare un'unità biometrica con archiviazione su scheda per operare in modalità avanzata, ma l'unità non può eseguire le operazioni di hashing necessarie.
-   Viene eseguito da una Desktop remoto client.

> [!Note]  
> Le applicazioni possono creare pool di sensori privati solo per la biometria con impronta digitale. Se un'applicazione tenta di crearne una per qualsiasi altro elemento (ad esempio, Viso), la richiesta avrà esito negativo.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di un pool di sensori privato](creating-a-private-sensor-pool.md)
</dt> <dt>

[Pool di sensori](sensor-pools.md)
</dt> <dt>

[Pool di sensori di sistema](system-sensor-pool.md)
</dt> </dl>

 

 




