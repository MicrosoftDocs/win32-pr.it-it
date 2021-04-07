---
description: Utilizzo di componenti non transazionali in una transazione
ms.assetid: b83b4bab-1851-48dc-b35a-6467a6dff741
title: Utilizzo di componenti non transazionali in una transazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a75cd8ebc756971a56413e371cf23de2144e5816
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748991"
---
# <a name="using-non-transactional-components-in-a-transaction"></a>Utilizzo di componenti non transazionali in una transazione

Spesso è utile inserire componenti non transazionali in una transazione per sfruttare le [proprietà ACID](acid-properties.md) delle transazioni. Se, ad esempio, si dispone di componenti legacy non transazionali utilizzati per aggiornare le password in una rete, è possibile inserire tali componenti in una transazione per garantire la coerenza degli aggiornamenti delle password in rete.

L' *oggetto di contesto di transazione* è un oggetto generico che consente ai client non transazionali di combinare il lavoro di più oggetti com in un'unica transazione, senza che sia necessario sviluppare un nuovo componente specifico a tale scopo. A differenza di una transazione automatica, l'oggetto contesto di transazione richiede che il client Esegui il commit o l'interruzione esplicita della transazione.

Per impostazione predefinita, il valore dell'attributo Transaction dell'oggetto del contesto di transazione è impostato su Required. COM+ interrompe la transazione se il client rilascia l'oggetto di contesto della transazione senza emettere esplicitamente una chiamata di commit o di interruzione.

Nell'esempio di Visual Basic seguente viene illustrato il modo in cui un client non transazionale può comporre il lavoro eseguito da più di un oggetto in un'unica transazione:


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



## <a name="limitations-of-the-transaction-context-object"></a>Limitazioni dell'oggetto del contesto di transazione

Di seguito sono riportate alcune importanti limitazioni relative all'oggetto di contesto di transazione:

-   Quando si utilizza un oggetto di contesto di transazione, la logica dell'applicazione che combina il lavoro di più oggetti in una singola transazione è associata a un'implementazione client non transazionale specifica e alcuni vantaggi derivanti dall'utilizzo di componenti COM andranno perduti. I vantaggi perduti includono i seguenti:
    -   Possibilità di riusare la logica dell'applicazione come parte di una transazione ancora più grande
    -   Imposizione della sicurezza dichiarativa
    -   Flessibilità per l'esecuzione remota della logica dal client
-   L'oggetto del contesto di transazione viene eseguito in-process con il client non transazionale, il che significa che COM+ deve essere disponibile nel computer client non transazionale. Questo potrebbe non essere un problema, ad esempio, quando l'oggetto di contesto di transazione viene utilizzato da una pagina di pagine ASP (Active Server) in esecuzione nello stesso server di COM+.
-   Non viene ottenuto un contesto per il client non transazionale quando si crea un oggetto di contesto di transazione. Il lavoro transazionale può essere eseguito solo indirettamente, tramite oggetti COM creati utilizzando l'oggetto di contesto della transazione. In particolare, il client non transazionale non può utilizzare i dispenser di risorse COM+ (ad esempio ODBC) e includere il lavoro nella transazione. Ad esempio, gli sviluppatori possono avere familiarità con la sintassi seguente per eseguire il lavoro transazionale nei sistemi di database relazionali:

    ``` syntax
    BEGIN TRANSACTION
      DoWork
    COMMIT TRANSACTION
    ```

    L'utilizzo di un oggetto di contesto di transazione in modo analogo non restituisce il risultato desiderato:

    ``` syntax
    Set objTxCtx = CreateObject ("TxCtx.TransactionContext")
      DoWork
      objTxCtx.Commit
    Set objTxCtx = Nothing
    ```

    La chiamata a DoWork in questo esempio non è integrata in una transazione. È invece necessario compilare un componente COM che chiama DoWork, creare un'istanza dell'oggetto di tale componente utilizzando l'oggetto di contesto della transazione e quindi chiamare tale oggetto dal client non transazionale affinché il lavoro faccia parte della transazione controllata dal client.

 

 



