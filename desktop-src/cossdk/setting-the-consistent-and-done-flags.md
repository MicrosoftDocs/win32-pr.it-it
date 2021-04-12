---
description: Impostazione dei flag coerenti e done
ms.assetid: d9b6096d-f93c-4f8e-a4d9-ea8309b35f0f
title: Impostazione dei flag coerenti e done
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd45d457828a222ce7f4ccbdc0080001b0f0b55f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483021"
---
# <a name="setting-the-consistent-and-done-flags"></a>Impostazione dei flag coerenti e done

È possibile impostare i flag coerenti e done richiamando i metodi nelle interfacce [**IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) o [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) . Le strategie utilizzate da queste due interfacce differiscono in modo significativo. **IObjectContext** dispone di quattro metodi che associano i flag coerenti e done in combinazioni univoche, mentre **IContextState** dispone di due metodi che consentono di impostare ogni flag in modo indipendente. I metodi di **IObjectContext** vengono esposti anche tramite l'oggetto [**ObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext) .

Per il controllo indipendente di ogni flag, [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) fornisce un metodo per impostare il flag coerente su true o false e un metodo per impostare il flag done su true o false. Questi metodi sono rispettivamente [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) e [**setDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn). L'interfaccia **IContextState** include inoltre metodi per recuperare il valore corrente di ogni flag.

Quando si imposta il valore del metodo [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) su TXCOMMIT, com+ verifica la presenza di una transazione. Se COM+ non rileva una transazione, viene generato un errore che è possibile acquisire in un file di log. Si supponga, ad esempio, che un utente configuri inavvertitamente l'attributo di transazione del componente in modo che non sia supportato, ma è previsto che sia impostato su Required. Impostando **SetMyTransactionVote** = TxCommit è possibile identificare il conflitto ed eseguire un'azione.

La tabella seguente descrive le chiamate al metodo che è possibile usare per impostare i flag coerenti e done.



| Flag coerente  | Flag done        | Metodo IObjectContext                                            | Metodi IContextState                                                                                                                                                                                    |
|------------------|------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vero<br/>  | Falso<br/> | [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit)<br/>   | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = TxCommit <br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = false<br/> |
| False<br/> | False<br/> | [**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit)<br/> | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = TxAbort <br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = false<br/>  |
| False<br/> | True<br/>  | [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)<br/>           | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = TxAbort <br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = true<br/>   |
| True<br/>  | True<br/>  | [**SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete)<br/>     | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = TxCommit <br/>[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = true              |



 

> [!Note]  
> La proprietà auto-done, impostata a livello di metodo, può influire sulla modalità di impostazione dei flag coerenti e done. Per ulteriori informazioni sulla proprietà auto-done, vedere [Abilitazione dell'operazione automatica per un metodo](enabling-auto-done-for-a-method.md) e [impostazione del bit done](setting-the-done-bit.md).

 

 

 




