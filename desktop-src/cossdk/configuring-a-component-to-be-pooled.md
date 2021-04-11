---
description: È possibile configurare un componente da raggruppare solo quando viene scritto correttamente per supportare il pool. Per informazioni dettagliate su questi requisiti, vedere Requisiti per gli oggetti pool.
ms.assetid: ffd812cc-811e-4f2a-8736-d1cb22d5abb7
title: Configurazione di un componente da raggruppare
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 780f7e1d9128b213b138e63b9dfa7e0f40642681
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127563"
---
# <a name="configuring-a-component-to-be-pooled"></a>Configurazione di un componente da raggruppare

È possibile configurare un componente da raggruppare solo quando viene scritto correttamente per supportare il pool. Per informazioni dettagliate su questi requisiti, vedere [requisiti per gli oggetti pool](requirements-for-poolable-objects.md).

> [!Note]  
> Per impostazione predefinita, un componente non è configurato per essere in pool.

 

Quando si configura un componente da raggruppare, è possibile specificare le proprietà seguenti per determinare il modo in cui COM+ gestisce il pool:

-   **Dimensioni minime del pool.** Rappresenta il numero di oggetti creati all'avvio dell'applicazione e il numero minimo di oggetti conservati nel pool mentre l'applicazione è in esecuzione. Se il numero di oggetti disponibili nel pool scende al di sotto del valore minimo specificato, vengono creati nuovi oggetti per soddisfare le richieste di oggetti in attesa e riempire il pool. Se il numero di oggetti disponibili nel pool è maggiore del numero minimo, questi oggetti surplus vengono eliminati durante un ciclo di pulizia.
-   **Dimensioni massime del pool.** Rappresenta il numero massimo di oggetti in pool che la gestione pool creerà, sia attivamente utilizzato dai client che inattivo nel pool. Quando si creano oggetti, gestione pool verifica se la dimensione massima del pool non è stata raggiunta e, in caso contrario, il gestore del pool crea una nuova istanza dell'oggetto da distribuire al client. Se è stata raggiunta la dimensione massima del pool, le richieste client verranno accodate e riceveranno il primo oggetto disponibile dal pool in base a una prima funzione. Il timeout delle richieste di creazione di oggetti avverrà dopo un periodo specificato.
-   **Timeout creazione (MS).** Specifica il tempo di attesa di un client, in millisecondi, per la restituzione di un oggetto dal pool dopo una chiamata a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance). Se la chiamata del client ha esito negativo, viene restituito l'errore E il \_ timeout.

**Per impostare le proprietà correlate al pool**

1.  Nel riquadro dei dettagli dello strumento di amministrazione Servizi componenti fare clic con il pulsante destro del mouse sul componente che si desidera configurare, quindi scegliere **Proprietà**.

2.  Nella finestra di dialogo Proprietà componente fare clic sulla scheda **attivazione** .

3.  Per abilitare il pool di oggetti per il componente, selezionare la casella di controllo **Abilita pool di oggetti** .

4.  Nella casella **dimensioni minime pool** immettere il numero minimo di oggetti di questo tipo nel pool. Il pool verrà mantenuto per avere almeno questo numero di oggetti.

5.  Nella casella u immettere il numero massimo di oggetti di questo tipo nel pool. Il numero di oggetti, sia attivato che disattivato, non supererà mai questo valore.

6.  Nella casella **timeout creazione (MS)** immettere il periodo di tempo, in millisecondi, in cui un client attenderà un oggetto in pool, se non è immediatamente disponibile.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Monitoraggio delle statistiche degli oggetti](monitoring-object-statistics.md)
</dt> </dl>

 

 
