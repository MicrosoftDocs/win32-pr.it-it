---
description: Se si sceglie di convertire manualmente i pacchetti MTS in applicazioni COM+ o lasciare che il processo di installazione di Microsoft Windows lo faccia automaticamente, è necessario essere a conoscenza dei risultati della conversione e dei problemi.
ms.assetid: 5b85aa5c-0409-4802-9335-04217ef5ddb9
title: Risultati e problemi della conversione COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a347df5f0ad0b16aee509c9c1b2c2c848372d0df2ccbc376814b0d14eb61d138
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129213"
---
# <a name="com-conversion-results-and-issues"></a>Risultati e problemi della conversione COM+

Se si sceglie di convertire manualmente i pacchetti MTS in applicazioni COM+ o lasciare che il processo di installazione di Microsoft Windows lo faccia automaticamente, è necessario essere a conoscenza dei risultati della conversione e dei problemi.

## <a name="what-is-converted"></a>Elementi convertiti

Durante la conversione, l'utilità MTSTOCOM converte ruoli, assegnazioni di ruolo, interfacce, metodi, utenti, elenco di computer e la maggior parte delle impostazioni del computer. L'utilità MTSTOCOM converte anche l'identità e la password per un pacchetto MTS.

I nuovi attributi COM+ non disponibili in MTS vengono impostati automaticamente sul valore predefinito seguente per tutti i componenti MTS convertiti. Queste impostazioni predefinite possono essere modificate usando lo strumento amministrativo Servizi componenti o le interfacce amministrative COM+.

-   Attivazione JIT abilitata.
-   Pool di oggetti disabilitato.
-   Sincronizzazione uguale all'impostazione transazione.

## <a name="conversion-issues"></a>Problemi di conversione

COM+ viene installato automaticamente quando si installa Windows. Non è possibile disinstallare COM+. Di seguito sono riportati i problemi relativi agli aggiornamenti di installazioni MTS e COM+ esistenti:

-   Se attualmente si usa MTS 1.0, MTS viene aggiornato automaticamente a COM+. Tuttavia, i pacchetti definiti dall'utente andranno persi ed è necessario crearli nuovamente.
-   Se attualmente si usa MTS 2.0, MTS viene aggiornato automaticamente a COM+. Tutti i pacchetti definiti dall'utente verranno aggiornati alle applicazioni COM+. Tutti i componenti dovrebbero funzionare come in MTS 2.0.
-   Se si usa MTS 1.0 e MTS 2.0 ed è stata installata l'opzione SDK, i file SDK verranno rimossi. È possibile installare l'SDK COM+ più recente tramite Microsoft Windows SDK.
-   Non è possibile gestire un computer MTS remoto da un computer COM+.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Conversione automatica da MTS](automatic-conversion-from-mts.md)
</dt> <dt>

[Conversione manuale da MTS](manual-conversion-from-mts.md)
</dt> <dt>

[Libreria di amministrazione MTS](mts-administration-library.md)
</dt> </dl>

 

 



