---
description: Sia che si scelga di convertire i pacchetti MTS in applicazioni COM+ manualmente o che il processo di installazione di Microsoft Windows lo esegua automaticamente, è necessario tenere presenti i risultati della conversione e i problemi.
ms.assetid: 5b85aa5c-0409-4802-9335-04217ef5ddb9
title: Risultati e problemi di conversione COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ded68e8e81d2c59c90607747c5f343dac364424
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401516"
---
# <a name="com-conversion-results-and-issues"></a>Risultati e problemi di conversione COM+

Sia che si scelga di convertire i pacchetti MTS in applicazioni COM+ manualmente o che il processo di installazione di Microsoft Windows lo esegua automaticamente, è necessario tenere presenti i risultati della conversione e i problemi.

## <a name="what-is-converted"></a>Elementi convertiti

Durante la conversione, l'utilità MTSTOCOM converte i ruoli, le assegnazioni di ruolo, le interfacce, i metodi, gli utenti, l'elenco dei computer e la maggior parte delle impostazioni del computer. L'utilità MTSTOCOM converte anche l'identità e la password per un pacchetto MTS.

I nuovi attributi COM+ che non erano disponibili in MTS vengono impostati automaticamente sui valori predefiniti seguenti per tutti i componenti MTS convertiti. Queste impostazioni predefinite possono essere modificate utilizzando lo strumento di amministrazione Servizi componenti o le interfacce amministrative COM+.

-   Attivazione JIT abilitata.
-   Pool di oggetti disabilitato.
-   Sincronizzazione come impostazione di transazione.

## <a name="conversion-issues"></a>Problemi di conversione

COM+ viene installato automaticamente durante l'installazione di Windows. Non è possibile disinstallare COM+. I problemi relativi agli aggiornamenti delle installazioni MTS e COM+ esistenti includono i seguenti:

-   Se attualmente si usa MTS 1,0, MTS viene aggiornato automaticamente a COM+. Tuttavia, i pacchetti definiti dall'utente andranno perduti ed è necessario crearli di nuovo.
-   Se attualmente si usa MTS 2,0, MTS viene aggiornato automaticamente a COM+. Tutti i pacchetti definiti dall'utente verranno aggiornati alle applicazioni COM+. Tutti i componenti dovrebbero funzionare come in MTS 2,0.
-   Se si usano MTS 1,0 e MTS 2,0 e si è installata l'opzione SDK, i file dell'SDK verranno rimossi. È possibile installare la versione più recente di COM+ SDK tramite il Microsoft Windows SDK.
-   Non è possibile gestire un computer MTS remoto da un computer COM+.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Conversione automatica da MTS](automatic-conversion-from-mts.md)
</dt> <dt>

[Conversione manuale da MTS](manual-conversion-from-mts.md)
</dt> <dt>

[Libreria di amministrazione MTS](mts-administration-library.md)
</dt> </dl>

 

 



