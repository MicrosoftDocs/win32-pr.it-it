---
description: Crea un oggetto transazionale generico che avvia una transazione.
ms.assetid: efaf1468-4973-472f-af91-85957a52b7df
title: Classe TransactionContext (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransactionContext
api_type:
- COM
ms.openlocfilehash: 595b5a3192b87420855eb43f1e1e33df37a45c23
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225754"
---
# <a name="transactioncontext-class"></a>Classe TransactionContext

Crea un oggetto transazionale generico che avvia una transazione. Chiamando i metodi di questa classe, è possibile comporre il lavoro di più oggetti COM in una singola transazione e confermare o interrompere in modo esplicito la transazione.

## <a name="when-to-implement"></a>Quando implementare

Questa classe è implementata da COM+.



| Requisito | Valore |
|------------|----------------------------------------------------|
| CLSID      | \_TRANSACTIONCONTEXT CLSID                          |
| ProgID     | L "TxCTx. TransactionContext"                        |
| Interfacce | [**ITransactionContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontext) |



 

## <a name="when-to-use"></a>Utilizzo

Un client non transazionale utilizza questa classe per avviare una transazione. Utilizzando i metodi di questa classe, il client può chiamare oggetti COM aggiuntivi che, se configurati per partecipare a una transazione, vengono eseguiti all'interno del limite della transazione dell'oggetto del contesto di transazione. In base alla logica di business, il client può eseguire in modo esplicito il commit o l'interruzione della transazione.

La classe **TransactionContext** limita il riutilizzo della logica di business che guida la transazione. Per questo motivo, è consigliabile usare sporadicamente gli oggetti di cui è stata creata un'istanza dalla classe **TransactionContext** .

## <a name="remarks"></a>Commenti

Per creare questo oggetto, chiamare [**IObjectContext:: CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).

Per utilizzare questa classe da Microsoft Visual Basic, aggiungere un riferimento alla libreria dei tipi di servizi COM+. Un oggetto TransactionContext può essere dichiarato con "COMSVCSLib. TransactionContext" come nome della classe.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>ComSvcs. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Configurazione di transazioni](configuring-transactions.md)
</dt> <dt>

[**ITransactionContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontext)
</dt> <dt>

[**TransactionContextEx**](transactioncontextex.md)
</dt> </dl>

 

 




