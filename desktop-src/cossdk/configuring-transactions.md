---
description: L'attributo transaction è una proprietà dichiarativa che gestisce automaticamente le transazioni per lo sviluppatore del componente. Impostando questo attributo, si elimina la necessità di usare controlli delle transazioni espliciti nel componente.
ms.assetid: ea0e4d7e-2598-4a42-993c-58815f2fa138
title: Configurazione delle transazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9d613eb49a5f053b869e3efc90e04b9455644ea52acbaf651f33b00909e6e35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128889"
---
# <a name="configuring-transactions"></a>Configurazione delle transazioni

*L'attributo transaction* è una proprietà dichiarativa che gestisce automaticamente le transazioni per lo sviluppatore del componente. Impostando questo attributo, si elimina la necessità di usare controlli delle transazioni espliciti nel componente.

COM+ usa l'attributo transaction del componente per determinare il tipo di protezione delle transazioni necessario per ogni oggetto attivato. A seconda dei requisiti, un oggetto può condividere la transazione del chiamante, richiedere una nuova transazione o operare senza protezione delle transazioni.

COM+ fornisce i valori degli attributi di transazione seguenti:

<dl> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>Disabili
</dt> <dd>

In generale, è consigliabile impostare questo valore di attributo solo quando si è certi che il componente non accede mai a un gestore di risorse. Quando si disabilita l'attributo transaction, COM+ ignora i requisiti transazionali del componente per determinare la posizione del contesto dell'oggetto. Di conseguenza, l'oggetto può condividere il contesto (e la transazione) del chiamante. Quando si esegue la migrazione di un componente COM a COM+, è necessario disabilitare l'attributo transaction per mantenere lo stesso comportamento transazionale del componente COM non configurato.

> [!Note]  
> Un *componente non configurato è* un componente COM che non è stato installato in un'applicazione COM+.

 

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>Non supportato
</dt> <dd>

Quando si imposta questo valore di attributo, COM+ garantisce che qualsiasi oggetto creato dal componente non partecipi mai a una transazione, indipendentemente dallo stato transazionale del chiamante. Dichiarando questo valore, si garantisce che un oggetto non vota nella transazione del chiamante né possa iniziare una transazione propria. Non supportato è il valore predefinito per tutti i componenti.

</dd> <dt>

<span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>Supportati
</dt> <dd>

Quando si imposta questo valore di attributo, COM+ garantisce che qualsiasi oggetto creato dal componente partecipi a una transazione, se esistente. Questo valore viene dichiarato quando si vuole che un oggetto conosi nella transazione del chiamante senza che sia necessaria una transazione propria.

</dd> <dt>

<span id="Required"></span><span id="required"></span><span id="REQUIRED"></span>Obbligatorio
</dt> <dd>

Quando si imposta il valore di questo attributo, COM+ garantisce che qualsiasi oggetto creato dal componente sia transazionale. Quando COM+ attiva un oggetto con l'impostazione Required, esamina lo stato transazionale del chiamante. Se il chiamante dispone di una transazione, il nuovo oggetto viene incluso nella transazione corrente. In caso contrario, COM+ avvia una transazione, rendendo il nuovo oggetto la radice della transazione. Si tratta dell'impostazione preferita per un componente che esegue attività di risorse perché consente di garantire la protezione delle transazioni per tali attività.

</dd> <dt>

<span id="Requires_New"></span><span id="requires_new"></span><span id="REQUIRES_NEW"></span>Richiede nuovo
</dt> <dd>

Quando si imposta questo valore di attributo, COM+ garantisce che tutti gli oggetti creati dal componente devono partecipare a una nuova transazione come radice della transazione, indipendentemente dallo stato transazionale del chiamante. COM+ avvia automaticamente una nuova transazione distinta dalla transazione del chiamante.

> [!Note]  
> COM+ non supporta le transazioni annidate. Quando un oggetto transazionale chiama un altro componente contrassegnato come Richiede nuovo, COM+ crea un limite transazionale indipendente per l'oggetto appena attivato. La seconda transazione non può influire sulla prima transazione a meno che la prima non annoti in modo esplicito i risultati della seconda transazione e modifichi il voto in base a tali risultati.

 

</dd> </dl>

## <a name="transaction-attribute-dependencies"></a>Dipendenze degli attributi delle transazioni

La tabella seguente illustra le caratteristiche di ogni valore dell'attributo di transazione COM+, incluso l'effetto del valore sulle caratteristiche della transazione. COM+ applica [l'attivazione e la sincronizzazione JIT](com--just-in-time-activation.md) [per](com--synchronization.md) tutti i componenti delle transazioni.



| Valore dell'attributo          | Nuova transazione   | Transazione del client                 | Radice transazione                        | Attivazione JIT      | Sincronizzazione     |
|--------------------------|-------------------|--------------------------------------|-----------------------------------------|---------------------|---------------------|
| Disabled<br/>      | Mai<br/>  | È possibile<br/>                     | Mai<br/>                        | Facoltativo<br/> | Facoltativo<br/> |
| Non supportato<br/> | Mai<br/>  | Mai<br/>                     | Mai<br/>                        | Facoltativo<br/> | Facoltativo<br/> |
| Supportato<br/>     | Mai<br/>  | Se il client ha una transazione<br/> | Mai<br/>                        | Obbligatoria<br/> | Obbligatoria<br/> |
| Obbligatoria<br/>      | È possibile<br/>  | Se il client ha una transazione<br/> | Se il client non dispone di alcuna transazione<br/> | Obbligatoria<br/> | Obbligatoria<br/> |
| RequiresNew<br/>  | Sempre<br/> | Mai<br/>                     | Sempre<br/>                       | Obbligatoria<br/> | Obbligatoria<br/> |



 

## <a name="transaction-boundaries"></a>Limiti delle transazioni

Una transazione ha un inizio, una fine e si verifica esattamente una volta. Durante l'esecuzione, una transazione può chiamare su una risorsa, ad esempio un database o una coda, per eseguire una o più attività. Ogni risorsa rientra nel limite *della transazione*. Tutte le risorse all'interno di un limite di transazione, che possono estendersi su più limiti di processi e computer, condividono una singola transazione. La gestione della coerenza tra questi limiti di processo e computer è importante.

COM+ garantisce la coerenza gestendo automaticamente i limiti delle transazioni, in base al valore dell'attributo della transazione impostato per ogni componente. Una transazione COM+ passa automaticamente agli oggetti a cui viene richiesto di partecipare a una transazione e ignora gli oggetti a cui viene richiesto di eseguire all'esterno di una transazione. COM+ non supporta le transazioni annidate. Le transazioni COM+ sono invece distinte e di breve durata.

Il primo oggetto in un limite della transazione è speciale per la transazione e viene chiamato *oggetto radice* della transazione. In una transazione può essere presente un solo oggetto radice. Tutti gli altri oggetti nella gerarchia transazionale all'interno dell'oggetto radice sono denominati *oggetti interni.*

## <a name="mapping-transactions"></a>Mapping delle transazioni

Un modo per assicurarsi che un oggetto venga incluso nel limite di transazione corretto è eseguire il mapping delle transazioni prima di iniziare a scrivere i componenti. Tramite il mapping delle transazioni è possibile determinare l'impostazione migliore per ogni componente scritto. Più si è certi di come devono essere usati i componenti, più facile è selezionare il valore corretto dell'attributo della transazione.

In fase di esecuzione COM+ esamina l'attributo della transazione per determinare se un oggetto deve essere la radice di una nuova transazione, deve essere creato in una transazione esistente o come oggetto non transazionale.

Nella figura seguente viene illustrato un possibile mapping delle transazioni. Nella figura il client crea l'oggetto 1, che richiede una transazione. Poiché non esiste alcuna transazione, COM+ crea la transazione 1 e vi inserisce l'oggetto 1 come oggetto radice. L'oggetto 1 crea l'oggetto 2, che supporta le transazioni e viene pertanto inserito nella transazione 1. L'oggetto 2 crea l'oggetto 3, che non supporta le transazioni e pertanto viene inserito all'esterno di tutte le transazioni. L'oggetto 2 crea anche l'oggetto 4, che richiede una transazione e pertanto viene inserito nella transazione 1. L'oggetto 3 crea l'oggetto 5, che supporta le transazioni. Tuttavia, poiché l'oggetto 5 viene creato da un oggetto che non esiste all'interno di una transazione, viene inserito anche all'esterno di tutte le transazioni. L'oggetto 4 crea l'oggetto 6, che richiede una nuova transazione, quindi COM+ crea la transazione 2 e inserisce l'oggetto 6 come oggetto radice. L'oggetto 6 crea l'oggetto 7, che supporta le transazioni e pertanto viene inserito nella transazione 2.

![Diagramma che mostra un'interazione client con la transazione 1 e la transazione 2.](images/fc7e2d03-94c2-40d9-a79b-1e05ca31dd80.png)

La figura precedente mostra due potenziali aree problematiche. In primo luogo, la maggior parte del lavoro è suddivisa tra due transazioni distinte. Se la transazione 1 ha esito negativo dopo la creazione dell'oggetto 6 da parte dell'oggetto 4, la transazione 2 viene eseguita in modo non interessato dal risultato della transazione 1. Se questo risultato non è intenzionale, è preferibile convertire le operazioni di entrambe le transazioni in una singola transazione, operazione che è possibile eseguire modificando l'attributo della transazione dell'oggetto 6 in Richiesto.

La figura di mapping mostra anche che l'oggetto 3 e l'oggetto 5 sono non transazionali, eseguiti completamente all'esterno dell'ambito delle transazioni 1 e 2. Se Object 5 aggiorna i dati persistenti, può essere necessario riconsiderarne lo stato non transazionale. L'oggetto 5 può essere inserito all'interno di una transazione impostandone l'attributo su Required.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione dell'attributo transaction](setting-the-transaction-attribute.md)
</dt> </dl>

 

 




