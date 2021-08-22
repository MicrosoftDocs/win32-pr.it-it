---
description: È possibile impostare manualmente gli attributi delle transazioni usando lo strumento amministrativo Servizi componenti oppure aggiungere il supporto a livello di codice per le transazioni quando si scrive il componente.
ms.assetid: b0d701c7-47ef-4034-873f-dd4428efb4c7
title: Impostazione dell'attributo transaction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de6310d2544090d4b551a93782b4756b3d89f2d6d365dfc09aec4658d5d3e1b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546218"
---
# <a name="setting-the-transaction-attribute"></a>Impostazione dell'attributo transaction

È possibile impostare manualmente gli attributi delle transazioni usando lo strumento amministrativo Servizi componenti oppure aggiungere il supporto a livello di codice per le transazioni quando si scrive il componente.

Per altre informazioni sui valori degli attributi delle transazioni, [vedere Configuring Transactions](configuring-transactions.md).

**Per impostare il valore dell'attributo utilizzando lo strumento amministrativo Servizi componenti**

1.  Nell'albero della console fare clic con il pulsante destro del mouse sul componente che si desidera configurare e quindi scegliere **Proprietà.**

2.  Nella finestra di dialogo proprietà componente fare clic **sulla scheda** Transazioni .

3.  In **Supporto transazioni** selezionare l'opzione per il valore desiderato. Il valore predefinito per tutti i componenti è **Non supportato.**

4.  Fare clic su **OK**.

È necessario ripetere questa procedura per ogni componente.

## <a name="to-set-the-attribute-value-programmatically"></a>Per impostare il valore dell'attributo a livello di codice

I programmatori che usano Microsoft Visual Basic possibile impostare l'attributo della transazione con **MTSTransactionMode**, una proprietà del modulo di classe per ActiveX progetti DLL. Visual Basic esegue il mapping della selezione al valore equivalente dell'attributo di transazione COM+ e pubblica il valore nella libreria dei tipi del componente.

Nella tabella seguente viene eseguito il mapping **di ogni valore costante MTSTransactionMode** al valore di transazione COM+ equivalente.



| Costante MTSTransactionMode         | Valore della transazione COM+             |
|-------------------------------------|------------------------------------|
| NotAnMTSObject (impostazione predefinita)<br/> | Disabled<br/>                |
| NoTransactions<br/>           | Non supportato (impostazione predefinita)<br/> |
| RequiresTransaction <br/>     | Necessario<br/>                |
| UsesTransaction <br/>         | Supportato<br/>               |
| RequiresNewTransaction <br/>  | RequiresNew<br/>            |



 

È **anche possibile accedere alla proprietà MTSTransactionMode** a livello di codice usando l'API della libreria di amministrazione COM+.

 

 




