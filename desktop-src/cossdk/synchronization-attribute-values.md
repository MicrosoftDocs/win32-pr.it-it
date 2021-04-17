---
description: L'attributo di sincronizzazione è una proprietà dichiarativa che specifica il tipo di sincronizzazione che si desidera che i componenti abbiano quando vengono attivati.
ms.assetid: 7f044ee5-b99e-4f0c-a680-b1e2672949fc
title: Valori degli attributi di sincronizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4606726d5202a1453e98d5bf609084982f8f824e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401420"
---
# <a name="synchronization-attribute-values"></a>Valori degli attributi di sincronizzazione

L'attributo di sincronizzazione è una proprietà dichiarativa che specifica il tipo di sincronizzazione che si desidera che i componenti abbiano quando vengono attivati. Quando si include l'attributo di sincronizzazione, COM+ gestisce i dettagli della sincronizzazione per conto dell'utente; non è necessario effettuare altre chiamate.

A seconda dei requisiti, un oggetto può condividere la sincronizzazione del chiamante, richiedere una nuova sincronizzazione o funzionare senza sincronizzazione.

COM+ fornisce i seguenti valori di attributo di sincronizzazione:

-   **Disabilitati.** Quando si disabilita l'attributo di sincronizzazione, COM+ ignora i requisiti di sincronizzazione del componente nel determinare il contesto per l'oggetto. Di conseguenza, l'oggetto può condividere o meno il contesto del chiamante (e la sincronizzazione).

    In generale, è consigliabile usare questo valore di attributo quando si sa che il componente non accede mai a una gestione risorse. Quando si esegue la migrazione di componenti COM a COM+, è necessario disabilitare l'attributo di sincronizzazione per mantenere lo stesso comportamento del componente COM non configurato. Un componente non configurato è un componente COM che non è stato installato in un'applicazione COM+.

-   **Non supportato.** Un oggetto con questo valore non fa mai parte di una sincronizzazione, a prescindere dallo stato del relativo chiamante. Questa impostazione è disponibile solo per i componenti che non sono transazionali e non utilizzano il servizio [di attivazione JIT (just-in-Time) com+](com--just-in-time-activation.md) .

-   **Supportato.** Un oggetto con questo valore partecipa alla sincronizzazione, se esistente. Questo valore viene dichiarato quando si desidera che un oggetto condivida la sincronizzazione del chiamante, ma non richiede la sincronizzazione.

    Un buon motivo per impostare l'attributo di sincronizzazione su supportato è che questa impostazione può essere meno costosa in termini di risorse di sistema. Tuttavia, è più difficile scrivere il componente a causa della necessità di proteggerlo dalle chiamate simultanee. L'implicazione dell'impostazione dell'attributo di sincronizzazione su supportato è che, in determinate circostanze, un'istanza dell'oggetto può essere creata in modo tale che non sia sincronizzata. Se il modello di threading del componente è libero o entrambi, sarà necessario proteggere i dati dell'istanza con un tipo di meccanismo di blocco. Se il modello di threading è Apartment (STA), non è necessario proteggere i dati dell'istanza.

-   **Obbligatoria.** Quando si imposta questo attributo, COM+ garantisce che tutti gli oggetti creati dal componente verranno sincronizzati. In effetti, ogni volta che COM+ crea un'istanza del componente, verifica che sia presente un solo thread attraverso questa istanza alla volta.

    Quando COM+ attiva un oggetto, esamina lo stato di sincronizzazione del chiamante. Se il chiamante è sincronizzato, COM+ scorre il limite di sincronizzazione del chiamante per includere il nuovo oggetto. In caso contrario, COM+ avvia la sincronizzazione.

-   **Richiede un nuovo.** Un oggetto con questo valore deve partecipare a una nuova sincronizzazione, in cui COM+ gestisce contesti e Apartment per conto di tutti i componenti coinvolti nella chiamata. COM+ avvia automaticamente una nuova sincronizzazione, che è diversa dalla sincronizzazione del chiamante.

    Un buon motivo per impostare l'attributo di sincronizzazione su richiede nuovo è che questa impostazione consente di effettuare in modo più efficiente chiamate esterne a un'istanza del componente. Tuttavia, effettua anche chiamate tra l'oggetto e l'oggetto che lo ha creato più costoso in termini di risorse di sistema.

    Si supponga, ad esempio, un caso in cui l'oggetto e il relativo oggetto Creator condividono lo stesso limite di sincronizzazione. Se il client A chiama l'oggetto Creator e il client B chiama l'oggetto, la seconda chiamata dovrà attendere fino al completamento della prima chiamata. Se si imposta requires New, l'oggetto viene creato in un limite di sincronizzazione separato. In questo caso, le chiamate da altri oggetti possono essere elaborate contemporaneamente. Tuttavia, le chiamate dall'oggetto Creator all'oggetto richiedono più risorse di sistema perché devono superare i limiti di sincronizzazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione dell'attributo di sincronizzazione](setting-the-synchronization-attribute.md)
</dt> <dt>

[Dipendenze di sincronizzazione](synchronization-dependencies.md)
</dt> </dl>

 

 



