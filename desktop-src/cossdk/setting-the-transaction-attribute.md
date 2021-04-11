---
description: È possibile impostare manualmente gli attributi delle transazioni utilizzando lo strumento di amministrazione Servizi componenti oppure è possibile aggiungere il supporto programmatico per le transazioni quando si scrive il componente.
ms.assetid: b0d701c7-47ef-4034-873f-dd4428efb4c7
title: Impostazione dell'attributo Transaction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0690a50f79c77a18b089cec1865dfbb9e7f428
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127394"
---
# <a name="setting-the-transaction-attribute"></a>Impostazione dell'attributo Transaction

È possibile impostare manualmente gli attributi delle transazioni utilizzando lo strumento di amministrazione Servizi componenti oppure è possibile aggiungere il supporto programmatico per le transazioni quando si scrive il componente.

Per ulteriori informazioni sui valori degli attributi delle transazioni, vedere [Configuring Transactions](configuring-transactions.md).

**Per impostare il valore dell'attributo utilizzando lo strumento di amministrazione Servizi componenti**

1.  Nell'albero della console fare clic con il pulsante destro del mouse sul componente che si desidera configurare, quindi scegliere **Proprietà**.

2.  Nella finestra di dialogo Proprietà componente fare clic sulla scheda **transazioni** .

3.  In **supporto transazioni** selezionare l'opzione per il valore desiderato. Il valore predefinito per tutti i componenti **non è supportato**.

4.  Fare clic su **OK**.

È necessario ripetere questa procedura per ogni componente.

## <a name="to-set-the-attribute-value-programmatically"></a>Per impostare il valore dell'attributo a livello di codice

I programmatori che utilizzano Microsoft Visual Basic possono impostare l'attributo Transaction con **MTSTransactionMode**, una proprietà del modulo di classe per i progetti DLL ActiveX. Visual Basic esegue il mapping della selezione al valore dell'attributo di transazione COM+ equivalente e pubblica il valore nella libreria dei tipi del componente.

Nella tabella seguente viene eseguito il mapping di ogni valore costante **MTSTransactionMode** al valore di transazione com+ equivalente.



| Costante MTSTransactionMode         | Valore transazione COM+             |
|-------------------------------------|------------------------------------|
| NotAnMTSObject (impostazione predefinita)<br/> | Disabled<br/>                |
| Notransacts<br/>           | Non supportato (impostazione predefinita)<br/> |
| RequiresTransaction <br/>     | Necessario<br/>                |
| UsesTransaction <br/>         | Supportato<br/>               |
| RequiresNewTransaction <br/>  | RequiresNew<br/>            |



 

È inoltre possibile accedere alla proprietà **MTSTransactionMode** a livello di codice tramite l'API della libreria di amministrazione com+.

 

 




