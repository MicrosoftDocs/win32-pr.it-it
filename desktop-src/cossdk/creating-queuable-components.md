---
description: Un componente con almeno un'interfaccia accodabile è un componente accodabile.
ms.assetid: 8183f640-4bf3-4555-8837-90a26130c618
title: Creazione di componenti accodabili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03533168a24da1e1f7279a6f2108e25717054103
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401435"
---
# <a name="creating-queuable-components"></a>Creazione di componenti accodabili

Un componente con almeno un'interfaccia accodabile è un *componente accodabile*. Affinché un componente venga richiamato da una coda, le interfacce devono essere contrassegnate come accodabili e il componente deve essere installato in un'applicazione in coda. Un componente accodabile, tuttavia, può essere un componente di un'applicazione non accodata.

Un'interfaccia accodabile deve contenere solo parametri in, senza parametri out e valori restituiti. Queste caratteristiche vengono verificate analizzando le informazioni sul tipo durante l'installazione del componente. Se l'interfaccia non è accodabile, non è possibile attivare la coda dell'applicazione contenente il componente.

Per specificare un'interfaccia COM+ come accodabile, attenersi alla procedura seguente:

1.  Nell'albero della console dello strumento di amministrazione Servizi componenti, in **Servizi componenti**, aprire la cartella **applicazioni com+** associata al computer che si desidera gestire.

2.  Aprire la cartella **interfacce** del componente dell'applicazione com+ che si desidera rendere accodabile.

3.  Fare clic con il pulsante destro del mouse sull'interfaccia che si desidera contrassegnare come accodabile, quindi scegliere **Proprietà**.

4.  Selezionare la scheda **Accodamento** nella finestra di dialogo Proprietà.

5.  Attivare la casella di controllo con l'etichetta **accodata**.

    > [!Note]  
    > Se la casella di controllo in **coda** è disabilitata, l'interfaccia non soddisfa i vincoli accodabili descritti in precedenza.

     

6.  Fare clic su **OK**.

    È possibile identificare un componente accodabile aggiungendo la macro dell'attributo QUEUEable alla sezione Interface del file di origine IDL (Interface Definition Language) per tutte le interfacce che sono accodabili.

    ``` syntax
#include "mtxattr.h"
    [ object, dual, uuid(), helpstring(IShiphip"), QUEUEABLE ]
    interface IShip:IDispatch{
       [propput, id(1)] HRESULT CustomerId ([in] long CustId);
       [propput, id(2)] HRESULT OrderId ([in] long OrderID);
       [id(3)] HRESULT LineItem ([in] long Qty);
       [id(4)] HRESULT Process ();
    }
    ```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di code di componenti](creating-component-queues.md)
</dt> <dt>

[Sviluppo di componenti in coda](developing-queued-components.md)
</dt> </dl>

 

 



