---
description: Un componente con almeno un'interfaccia di accodamento è un componente a cui è possibile eseguire query.
ms.assetid: 8183f640-4bf3-4555-8837-90a26130c618
title: Creazione di componenti accodamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d8ca7b4717da44145121508ed3e8b208e8401a240f1a2ceb858be299bf2b32f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637841"
---
# <a name="creating-queuable-components"></a>Creazione di componenti accodamento

Un componente con almeno un'interfaccia di accodamento è un componente a cui è *possibile eseguire l'accodamento.* Perché un componente sia richiamato da una coda, le interfacce devono essere contrassegnate come accodamentabili e il componente deve essere installato in un'applicazione in coda. Tuttavia, un componente accodabile può essere un componente di un'applicazione non in coda.

Un'interfaccia di accodamento deve contenere solo parametri, ovvero nessun parametro out e nessun valore restituito. Queste caratteristiche vengono verificate analizzando le informazioni sul tipo durante l'installazione del componente. Se non è possibile eseguire query sull'interfaccia, non è possibile attivare la coda dell'applicazione contenente il componente.

Per specificare un'interfaccia COM+ come accodamento, seguire questa procedura:

1.  Nell'albero della console dello strumento di amministrazione Servizi componenti, in Servizi componenti **aprire** la cartella **Applicazioni COM+** associata al computer da gestire.

2.  Aprire la **cartella Interfacce** del componente dell'applicazione COM+ che si vuole rendere accodamentabile.

3.  Fare clic con il pulsante destro del mouse sull'interfaccia che si desidera contrassegnare come accodamento, quindi scegliere **Proprietà**.

4.  Selezionare la **scheda Accodamento** nella finestra di dialogo delle proprietà.

5.  Attivare la casella di controllo **queued**.

    > [!Note]  
    > Se la **casella di controllo** In coda è disattivata, l'interfaccia non soddisfa i vincoli di accodamento descritti in precedenza.

     

6.  Fare clic su **OK**.

    Un componente di accodamento può essere identificato come tale aggiungendo la macro dell'attributo QUEUEABLE alla sezione Interface del file di origine IDL (Interface Definition Language) per tutte le interfacce di cui è possibile eseguire la query.

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

 

 



