---
description: Impostazione dei flag Coerenti e Done
ms.assetid: d9b6096d-f93c-4f8e-a4d9-ea8309b35f0f
title: Impostazione dei flag Coerenti e Done
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 518864efda3716ea9998ed306b0ca6901b70697f8cb3acabe813d3e2e3e0bcd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500051"
---
# <a name="setting-the-consistent-and-done-flags"></a>Impostazione dei flag Coerenti e Done

È possibile impostare i flag coerenti ed evasi richiamando metodi sulle [**interfacce IObjectContext**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontext) o [**IContextState.**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) Le strategie usate da queste due interfacce differiscono in modo significativo. **IObjectContext** ha quattro metodi che associano i flag coerenti e non eserciti in combinazioni univoche, mentre **IContextState** ha due metodi che consentono di impostare ogni flag in modo indipendente. I metodi di **IObjectContext** vengono esposti anche tramite [**l'oggetto ObjectContext.**](/windows/desktop/api/ComSvcs/nn-comsvcs-objectcontext)

Per il controllo indipendente di ogni flag, [**IContextState**](/windows/desktop/api/ComSvcs/nn-comsvcs-icontextstate) fornisce un metodo per impostare il flag coerente su True o False e un metodo per impostare il flag done su True o False. Questi metodi sono [**Rispettivamente SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) e [**SetDeactivateOnReturn.**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) **L'interfaccia IContextState** include anche metodi per recuperare il valore corrente di ogni flag.

Quando si imposta il [**valore del metodo SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) su TxCommit, COM+ verifica la presenza di una transazione. Se COM+ non rileva una transazione, genera un errore che è possibile acquisire in un file di log. Si supponga, ad esempio, che un utente inavvertitamente configura l'attributo della transazione del componente su Non supportato, ma che sia impostato su Obbligatorio. Impostando **SetMyTransactionVote** = TxCommit, è possibile identificare il conflitto ed eseguire un'azione.

Nella tabella seguente vengono descritte le chiamate al metodo che possono essere usate per impostare i flag coerenti e non eseciti.



| Flag coerente  | Flag Done        | Metodo IObjectContext                                            | Metodi di IContextState                                                                                                                                                                                    |
|------------------|------------------|------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vero<br/>  | Falso<br/> | [**EnableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-enablecommit)<br/>   | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = TxCommit <br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = False<br/> |
| False<br/> | False<br/> | [**DisableCommit**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-disablecommit)<br/> | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = TxAbort <br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = False<br/>  |
| False<br/> | True<br/>  | [**Setabort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)<br/>           | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = TxAbort <br/> [**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = True<br/>   |
| True<br/>  | True<br/>  | [**Setcomplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete)<br/>     | [**SetMyTransactionVote**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setmytransactionvote) *txVote* = TxCommit <br/>[**SetDeactivateOnReturn**](/windows/desktop/api/ComSvcs/nf-comsvcs-icontextstate-setdeactivateonreturn) *bDeactivate* = True              |



 

> [!Note]  
> La proprietà eseguita automaticamente, impostata a livello di metodo, può influire sul modo in cui vengono impostati i flag coerenti e non evasi. Per altre informazioni sulla proprietà con completamento automatico, vedere [Abilitazione del](enabling-auto-done-for-a-method.md) completamento automatico per un metodo e [Impostazione del bit done](setting-the-done-bit.md).

 

 

 




