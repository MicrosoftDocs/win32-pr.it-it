---
description: L'attributo Transaction è una proprietà dichiarativa che gestisce automaticamente le transazioni per lo sviluppatore di componenti. Impostando questo attributo, si elimina la necessità di utilizzare controlli di transazione espliciti nel componente.
ms.assetid: ea0e4d7e-2598-4a42-993c-58815f2fa138
title: Configurazione di transazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b57f27d47836193dc5d23c44e3344cb2a81d5984
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "104554564"
---
# <a name="configuring-transactions"></a>Configurazione di transazioni

L' *attributo Transaction* è una proprietà dichiarativa che gestisce automaticamente le transazioni per lo sviluppatore di componenti. Impostando questo attributo, si elimina la necessità di utilizzare controlli di transazione espliciti nel componente.

COM+ utilizza l'attributo Transaction del componente per determinare il tipo di protezione delle transazioni richiesto per ogni oggetto attivato. A seconda del requisito, un oggetto può condividere la transazione del chiamante, richiedere una nuova transazione o operare senza la protezione delle transazioni.

COM+ fornisce i seguenti valori di attributo di transazione:

<dl> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>Disabilitato
</dt> <dd>

In generale, è consigliabile impostare questo valore di attributo solo quando si è certi che il componente non acceda mai a Resource Manager. Quando si disabilita l'attributo Transaction, COM+ ignora i requisiti transazionali del componente nella determinazione del posizionamento del contesto dell'oggetto. Di conseguenza, l'oggetto può condividere il contesto del chiamante (e la transazione). Quando si esegue la migrazione di un componente COM a COM+, è necessario disabilitare l'attributo Transaction per mantenere lo stesso comportamento transazionale del componente COM non configurato.

> [!Note]  
> Un *componente non configurato* è un componente COM che non è stato installato in un'applicazione com+.

 

</dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>Non supportato
</dt> <dd>

Quando si imposta questo valore di attributo, COM+ garantisce che tutti gli oggetti creati dal componente non partecipino mai a una transazione, indipendentemente dallo stato transazionale del chiamante. Dichiarando questo valore, si garantisce che un oggetto non voti nella transazione del chiamante né può iniziare una transazione autonomamente. Il valore predefinito per tutti i componenti non è supportato.

</dd> <dt>

<span id="Supported"></span><span id="supported"></span><span id="SUPPORTED"></span>Supportato
</dt> <dd>

Quando si imposta questo valore di attributo, COM+ garantisce che tutti gli oggetti creati dal componente partecipino a una transazione, se ne esiste una. Questo valore viene dichiarato quando si desidera che un oggetto condivida la transazione del chiamante senza che sia necessaria una transazione.

</dd> <dt>

<span id="Required"></span><span id="required"></span><span id="REQUIRED"></span>Obbligatorio
</dt> <dd>

Quando si imposta questo valore di attributo, COM+ garantisce che tutti gli oggetti creati dal componente siano transazionali. Quando COM+ attiva un oggetto con l'impostazione obbligatoria, esamina lo stato transazionale del chiamante. Se il chiamante dispone di una transazione, il nuovo oggetto verrà incluso nella transazione corrente. In caso contrario, COM+ inizia una transazione, rendendo il nuovo oggetto la radice della transazione. Si tratta dell'impostazione preferita per un componente che esegue attività di risorse, in quanto consente di garantire la protezione delle transazioni per tali attività.

</dd> <dt>

<span id="Requires_New"></span><span id="requires_new"></span><span id="REQUIRES_NEW"></span>Richiede nuovo
</dt> <dd>

Quando si imposta questo valore di attributo, COM+ garantisce che tutti gli oggetti creati dal componente debbano partecipare a una nuova transazione come radice della transazione, indipendentemente dallo stato transazionale del chiamante. COM+ avvia automaticamente una nuova transazione che è diversa dalla transazione del chiamante.

> [!Note]  
> COM+ non supporta le transazioni nidificate. Quando un oggetto transazionale chiama un altro componente contrassegnato come requires New, COM+ crea un limite transazionale indipendente per l'oggetto appena attivato. La seconda transazione non può influire sulla prima transazione, a meno che la prima transazione non specifichi in modo esplicito i risultati della seconda transazione e modifichi il voto in base a tali risultati.

 

</dd> </dl>

## <a name="transaction-attribute-dependencies"></a>Dipendenze degli attributi di transazione

Nella tabella seguente sono illustrate le caratteristiche di ogni valore di attributo di transazione COM+, incluso l'effetto del valore sulle caratteristiche della transazione. COM+ impone l'attivazione e la [sincronizzazione](com--synchronization.md) [JIT](com--just-in-time-activation.md) per tutti i componenti della transazione.



| Valore dell'attributo          | Nuova transazione   | Transazione del client                 | Radice transazione                        | Attivazione JIT      | Sincronizzazione     |
|--------------------------|-------------------|--------------------------------------|-----------------------------------------|---------------------|---------------------|
| Disabled<br/>      | Mai<br/>  | È possibile<br/>                     | Mai<br/>                        | Facoltativo<br/> | Facoltativo<br/> |
| Non supportato<br/> | Mai<br/>  | Mai<br/>                     | Mai<br/>                        | Facoltativo<br/> | Facoltativo<br/> |
| Supportato<br/>     | Mai<br/>  | Se il client ha una transazione<br/> | Mai<br/>                        | Obbligatoria<br/> | Obbligatoria<br/> |
| Obbligatoria<br/>      | È possibile<br/>  | Se il client ha una transazione<br/> | Se il client non dispone di alcuna transazione<br/> | Obbligatoria<br/> | Obbligatoria<br/> |
| RequiresNew<br/>  | Always<br/> | Mai<br/>                     | Always<br/>                       | Obbligatoria<br/> | Obbligatoria<br/> |



 

## <a name="transaction-boundaries"></a>Limiti delle transazioni

Una transazione ha un inizio, un'entità finale e si verifica esattamente una volta. Durante l'esecuzione, una transazione può chiamare su una risorsa, ad esempio un database o una coda, per eseguire una o più attività. Ogni risorsa rientra nel *limite della transazione*. Tutte le risorse all'interno di un limite di transazione, che può estendersi su più limiti di processi e computer, condividono una singola transazione. È importante gestire la coerenza tra questi limiti di processo e computer.

COM+ garantisce la coerenza gestendo automaticamente i limiti delle transazioni, in base al valore dell'attributo di transazione impostato per ogni componente. Una transazione COM+ passa automaticamente agli oggetti a cui è stato richiesto di partecipare a una transazione e ignora gli oggetti a cui è stato richiesto di eseguire all'esterno di una transazione. COM+ non supporta le transazioni nidificate. Al contrario, le transazioni COM+ sono distinte e di breve durata.

Il primo oggetto in un limite di transazione è speciale per la transazione e viene chiamato *oggetto radice* della transazione. In una transazione può essere presente un solo oggetto radice. Tutti gli altri oggetti nella gerarchia transazionale sotto l'oggetto radice sono detti *oggetti interni*.

## <a name="mapping-transactions"></a>Transazioni di mapping

Un modo per garantire che un oggetto sia incluso nel limite di transazioni corretto consiste nel mappare le transazioni prima di iniziare a scrivere i componenti. Eseguendo il mapping delle transazioni, è possibile determinare l'impostazione migliore per ogni componente che si scrive. Maggiore è il modo in cui vengono usati i componenti, più è semplice selezionare il valore corretto dell'attributo Transaction.

In fase di esecuzione, COM+ esamina l'attributo Transaction per determinare se un oggetto deve essere la radice di una nuova transazione, essere creato in una transazione esistente o essere creato come oggetto non transazionale.

Nella figura seguente viene illustrato un possibile mapping delle transazioni. Nell'illustrazione, il client crea l'oggetto 1, che richiede una transazione. Poiché non esiste alcuna transazione, COM+ crea la transazione 1 e inserisce l'oggetto 1 come oggetto radice. L'oggetto 1 crea l'oggetto 2, che supporta le transazioni e pertanto viene inserito nella transazione 1. L'oggetto 2 crea l'oggetto 3, che non supporta le transazioni e pertanto viene inserito all'esterno di tutte le transazioni. Nell'oggetto 2 viene inoltre creato l'oggetto 4, che richiede una transazione ed è quindi inserito nella transazione 1. L'oggetto 3 crea l'oggetto 5 che supporta le transazioni. Tuttavia, poiché l'oggetto 5 viene creato da un oggetto che non esiste all'interno di una transazione, viene inserito anche al di fuori di tutte le transazioni. L'oggetto 4 crea l'oggetto 6, che richiede una nuova transazione, quindi COM+ crea la transazione 2 e inserisce l'oggetto 6 come oggetto radice. L'oggetto 6 crea l'oggetto 7, che supporta le transazioni, quindi viene inserito nella transazione 2.

![Diagramma che mostra un'interazione del client con la transazione 1 e la transazione 2.](images/fc7e2d03-94c2-40d9-a79b-1e05ca31dd80.png)

Nella figura precedente vengono illustrate due potenziali aree problematiche. In primo luogo, la maggior parte del lavoro viene suddivisa tra due transazioni distinte. Se la transazione 1 ha esito negativo dopo che l'oggetto 4 crea l'oggetto 6, la transazione 2 viene eseguita in base al risultato della transazione 1. Se il risultato non è previsto, potrebbe essere preferibile ridurre le operazioni di entrambe le transazioni in un'unica transazione, operazione che è possibile eseguire cambiando l'attributo Transaction dell'oggetto 6 in required.

Nell'illustrazione di mapping viene inoltre illustrato che l'oggetto 3 e l'oggetto 5 sono non transazionali, in esecuzione completamente al di fuori dell'ambito delle transazioni 1 e 2. Se l'oggetto 5 aggiorna i dati persistenti, potrebbe essere necessario riconsiderarne lo stato non transazionale. È possibile inserire l'oggetto 5 all'interno di una transazione modificando il relativo attributo Transaction su Required.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione dell'attributo Transaction](setting-the-transaction-attribute.md)
</dt> </dl>

 

 




