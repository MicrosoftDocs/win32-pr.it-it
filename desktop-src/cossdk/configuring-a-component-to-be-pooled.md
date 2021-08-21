---
description: È possibile configurare un componente per il pool solo quando viene scritto correttamente per supportare il pool. Per informazioni dettagliate su questi requisiti, vedere Requisiti per gli oggetti in pool.
ms.assetid: ffd812cc-811e-4f2a-8736-d1cb22d5abb7
title: Configurazione di un componente da creare in pool
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2640a9c038a8d0d12e1447adafbaaea91c3addddffd04bccdfad0ba4180740f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118102383"
---
# <a name="configuring-a-component-to-be-pooled"></a>Configurazione di un componente da creare in pool

È possibile configurare un componente per il pool solo quando viene scritto correttamente per supportare il pool. Per informazioni dettagliate su questi requisiti, vedere [Requisiti per gli oggetti in pool.](requirements-for-poolable-objects.md)

> [!Note]  
> Per impostazione predefinita, un componente non è configurato per il pool.

 

Quando si configura un componente per il pool, è possibile specificare le proprietà seguenti per determinare il modo in cui COM+ gestisce il pool:

-   **Dimensioni minime del pool.** Rappresenta il numero di oggetti creati all'avvio dell'applicazione e il numero minimo di oggetti mantenuti nel pool mentre l'applicazione è in esecuzione. Se il numero di oggetti disponibili nel pool scende al di sotto del minimo specificato, vengono creati nuovi oggetti per soddisfare eventuali richieste di oggetti in sospeso e riempire nuovamente il pool. Se il numero di oggetti disponibili nel pool è maggiore del numero minimo, tali oggetti in eccesso vengono distrutti durante un ciclo di pulizia.
-   **Dimensioni massime del pool.** Rappresenta il numero massimo di oggetti in pool che verranno creati dal gestore di pool, sia utilizzati attivamente dai client che inattivi nel pool. Durante la creazione di oggetti, il gestore del pool verifica che le dimensioni massime del pool non siano state raggiunte e, in caso contrario, crei una nuova istanza dell'oggetto da elarne al client. Se è stata raggiunta la dimensione massima del pool, le richieste client verranno accodati e riceveranno il primo oggetto disponibile dal pool in base al primo utilizzo. Le richieste di creazione di oggetti avranno un timeout dopo un periodo specificato.
-   **Timeout di creazione (ms).** Specifica per quanto tempo un client attenderà, in millisecondi, che un oggetto sia restituito dal pool dopo una chiamata a [**CoCreateInstance.**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) Se la chiamata client non riesce, viene restituito l'errore E \_ TIMEOUT.

**Per impostare le proprietà correlate al pool**

1.  Nel riquadro dei dettagli dello strumento di amministrazione Servizi componenti fare clic con il pulsante destro del mouse sul componente che si desidera configurare, quindi scegliere **Proprietà.**

2.  Nella finestra di dialogo delle proprietà del componente fare clic **sulla scheda** Attivazione .

3.  Per abilitare il pool di oggetti per il componente, selezionare la **casella di controllo** Abilita pool di oggetti .

4.  Nella casella **Dimensioni minime pool** immettere il numero minimo di oggetti di questo tipo nel pool. Il pool verrà mantenuto in modo da avere almeno questo numero di oggetti.

5.  Nella casella u immettere il numero massimo di oggetti di questo tipo nel pool. Il numero di oggetti, sia attivati che disattivati, non supererà mai questo valore.

6.  Nella casella **Timeout creazione (ms)** immettere la quantità di tempo, in millisecondi, per cui un client attenderà un oggetto in pool se non è immediatamente disponibile.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Monitoraggio delle statistiche degli oggetti](monitoring-object-statistics.md)
</dt> </dl>

 

 
