---
description: Crea un oggetto transazionale generico che inizia una transazione.
ms.assetid: efaf1468-4973-472f-af91-85957a52b7df
title: Classe TransactionContext (ComSvcs.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransactionContext
api_type:
- COM
ms.openlocfilehash: aa0a90cee2b0af7d5ebe3679dca46aa04c6326fb5fd62fe5f57699d610b9efe8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678151"
---
# <a name="transactioncontext-class"></a>Classe TransactionContext

Crea un oggetto transazionale generico che inizia una transazione. Chiamando i metodi di questa classe, è possibile comporre il lavoro di più oggetti COM in una singola transazione ed eseguire in modo esplicito il commit o l'interruzione della transazione.

## <a name="when-to-implement"></a>Quando implementare

Questa classe viene implementata da COM+.



| Requisito | Valore |
|------------|----------------------------------------------------|
| CLSID      | CLSID \_ TransactionContext                          |
| ProgID     | L"TxCTx.TransactionContext"                        |
| Interfacce | [**ITransactionContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontext) |



 

## <a name="when-to-use"></a>Utilizzo

Un client non transazionale utilizza questa classe per avviare una transazione. Utilizzando i metodi di questa classe, il client può chiamare oggetti COM aggiuntivi che, se configurati per partecipare a una transazione, vengono eseguiti entro il limite della transazione dell'oggetto contesto di transazione. In base alla logica di business, il client può eseguire in modo esplicito il commit o l'interruzione della transazione.

La **classe TransactionContext** limita il riutilizzo della logica di business che guida la transazione. Per questo motivo, è consigliabile usare solo oggetti di cui è stata creata un'istanza dalla **classe TransactionContext.**

## <a name="remarks"></a>Commenti

Per creare questo oggetto, chiamare [**IObjectContext::CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance).

Per usare questa classe da Microsoft Visual Basic, aggiungere un riferimento alla libreria dei tipi dei servizi COM+. Un oggetto TransactionContext può essere dichiarato usando "COMSVCSLib.TransactionContext" come nome della classe.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Intestazione<br/>                   | <dl> <dt>ComSvcs.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Configurazione delle transazioni](configuring-transactions.md)
</dt> <dt>

[**ITransactionContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-itransactioncontext)
</dt> <dt>

[**TransactionContextEx**](transactioncontextex.md)
</dt> </dl>

 

 




