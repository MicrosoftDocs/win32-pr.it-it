---
description: Crea un oggetto transazionale generico che avvia una transazione. Chiamando i metodi di questa classe, è possibile comporre il lavoro di più oggetti COM in una singola transazione e confermare o interrompere in modo esplicito la transazione.
ms.assetid: 5f3f83e0-33fc-4c43-9327-59485c0d8bd3
title: Classe TransactionContextEx (ComSvcs. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransactionContextEx
api_type:
- COM
ms.openlocfilehash: 8cf5c3aaa7ffe126124a909498a7c54cfb012c65
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748839"
---
# <a name="transactioncontextex-class"></a>Classe TransactionContextEx

Crea un oggetto transazionale generico che avvia una transazione. Chiamando i metodi di questa classe, è possibile comporre il lavoro di più oggetti COM in una singola transazione e confermare o interrompere in modo esplicito la transazione.

## <a name="when-to-implement"></a>Quando implementare

Questa classe è implementata da COM+.



| Requisito | Valore |
|------------|--------------------------------------------------------|
| CLSID      | \_TRANSACTIONCONTEXTEX CLSID                            |
| ProgID     | L "TxCTx. TransactionContextEx"                          |
| Interfacce | [**ITransactionContextEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontextex) |



 

## <a name="when-to-use"></a>Utilizzo

Un client non transazionale utilizza questa classe per avviare una transazione. Utilizzando i metodi di questa classe, il client può chiamare oggetti COM aggiuntivi che, se configurati per partecipare a una transazione, vengono eseguiti all'interno del limite della transazione dell'oggetto del contesto di transazione. In base alla logica di business, il client può eseguire in modo esplicito il commit o l'interruzione della transazione.

La classe **TransactionContextEx** limita il riutilizzo della logica di business che guida la transazione. Per questo motivo, è consigliabile usare sporadicamente gli oggetti di cui è stata creata un'istanza dalla classe **TransactionContextEx** .

## <a name="remarks"></a>Commenti

Per creare questo oggetto, chiamare [**IObjectContext:: CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).

La classe **TransactionContextEx** non è stata progettata per essere utilizzata in Visual Basic. In alternativa, usare la classe [**TransactionContext**](transactioncontext.md) .

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

[**ITransactionContextEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontextex)
</dt> <dt>

[**TransactionContext**](transactioncontext.md)
</dt> </dl>

 

 




