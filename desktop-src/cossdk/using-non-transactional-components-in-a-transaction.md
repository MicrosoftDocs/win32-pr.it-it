---
description: Utilizzo di componenti non transazionali in una transazione
ms.assetid: b83b4bab-1851-48dc-b35a-6467a6dff741
title: Utilizzo di componenti non transazionali in una transazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 365cf6f8e5c20f328f4308366e9a98916d9277363bba815fdbc00b5e2d8203d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991351"
---
# <a name="using-non-transactional-components-in-a-transaction"></a>Utilizzo di componenti non transazionali in una transazione

Spesso è utile inserire componenti non transazionali in una transazione per sfruttare le [proprietà ACID](acid-properties.md) delle transazioni. Ad esempio, se si dispone di componenti legacy non transazionali utilizzati per aggiornare le password in una rete, è possibile inserire tali componenti in una transazione per garantire che gli aggiornamenti delle password siano coerenti in tutta la rete.

*L'oggetto* contesto di transazione è un oggetto generico che consente ai client non transazionali di combinare il lavoro di più oggetti COM in un'unica transazione, senza richiedere lo sviluppo di un nuovo componente specifico per tale scopo. A differenza di una transazione automatica, l'oggetto contesto della transazione richiede al client di eseguire in modo esplicito il commit o l'interruzione della transazione.

Per impostazione predefinita, il valore dell'attributo transaction dell'oggetto contesto di transazione è impostato su Required. COM+ interrompe la transazione se il client rilascia l'oggetto contesto della transazione senza eseguire in modo esplicito una chiamata di commit o interruzione.

Nell'Visual Basic seguente viene illustrato come un client non transazionale può comporre il lavoro eseguito da più di un oggetto in una singola transazione:


```VB
Dim objTxCtx As TransactionContext
Dim objCat As MyDLL.Ccat  ' Ccat is a user-defined component.
Dim objDog As MyDLL.Cdog  ' Cdog is a user-defined component.

' Get TransactionContext object.
Set objTxCtx = _
  CreateObject ("TxCtx.TransactionContext")

' Create instances of Cat and Dog.
Set objCat = _ 
  objTxCtx.CreateInstance ("MyDLL.Ccat")
Set objDog = _ 
  objTxCtx.CreateInstance ("MyDLL.Cdog")

' Both objects do work.
objDog.Bark
objCat.Hiss

' Commit the transaction.
objTxCtx.Commit

```



## <a name="limitations-of-the-transaction-context-object"></a>Limitazioni dell'oggetto contesto di transazione

Di seguito sono riportate alcune importanti limitazioni dell'oggetto contesto di transazione:

-   Quando si usa un oggetto contesto di transazione, la logica dell'applicazione che combina il lavoro di più oggetti in una singola transazione è associata a un'implementazione client non transazionale specifica e alcuni vantaggi dell'uso dei componenti COM vengono persi. Questi vantaggi persi includono i seguenti:
    -   Possibilità di riutilizzare la logica dell'applicazione come parte di una transazione ancora più grande
    -   Imposizione della sicurezza dichiarativa
    -   Flessibilità di esecuzione della logica in remoto dal client
-   L'oggetto contesto di transazione viene eseguito in-process con il client non transazionale, il che significa che COM+ deve essere disponibile nel computer client non transazionale. Questo potrebbe non essere un problema, ad esempio, quando l'oggetto contesto di transazione viene usato da una pagina ASP (Active Server Pages) in esecuzione nello stesso server di COM+.
-   Non si ottiene un contesto per il client non transazionale quando si crea un oggetto contesto di transazione. Le operazioni transazionali possono essere eseguite solo indirettamente, tramite oggetti COM creati utilizzando l'oggetto contesto di transazione. In particolare, il client non transazionale non può usare i dispenser di risorse COM+ (ad esempio ODBC) e includere il lavoro nella transazione. Ad esempio, gli sviluppatori potrebbero avere familiarità con la sintassi seguente per eseguire operazioni transazionali su sistemi di database relazionali:

    ``` syntax
    BEGIN TRANSACTION
      DoWork
    COMMIT TRANSACTION
    ```

    L'uso dell'oggetto contesto di transazione in modo simile non produce il risultato desiderato:

    ``` syntax
    Set objTxCtx = CreateObject ("TxCtx.TransactionContext")
      DoWork
      objTxCtx.Commit
    Set objTxCtx = Nothing
    ```

    La chiamata a DoWork in questo esempio non è integrata in una transazione. È invece necessario compilare un componente COM che chiama DoWork, creare un'istanza dell'oggetto di tale componente usando l'oggetto contesto di transazione e quindi chiamare tale oggetto dal client non transazionale perché il lavoro faccia parte della transazione controllata dal client.

 

 



