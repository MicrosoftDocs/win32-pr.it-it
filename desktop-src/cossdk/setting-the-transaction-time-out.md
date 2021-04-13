---
description: È possibile impostare manualmente il timeout per le transazioni utilizzando lo strumento di amministrazione Servizi componenti oppure è possibile configurare il timeout a livello di codice utilizzando le interfacce di amministrazione COM+.
ms.assetid: f7a35bdf-ea6d-40ea-b3c0-c2a3ae2276c4
title: Impostazione della transazione Time-Out
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b002448ca21e97e2e4996679d87a4b6a7680161f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483781"
---
# <a name="setting-the-transaction-time-out"></a>Impostazione della transazione Time-Out

È possibile impostare manualmente il timeout per le transazioni utilizzando lo strumento di amministrazione Servizi componenti oppure è possibile configurare il timeout a livello di codice utilizzando le [interfacce di amministrazione com+](com--administration-interfaces.md). Il timeout può essere configurato a livello di computer locale e anche per i singoli componenti.

**Per impostare il timeout della transazione per il computer locale utilizzando lo strumento di amministrazione Servizi componenti**

1.  Nell'albero della console fare clic con il pulsante destro del mouse sul computer locale che si desidera configurare, quindi scegliere **Proprietà**.

2.  Nella finestra di dialogo Proprietà computer fare clic sulla scheda **Opzioni** .

3.  In **timeout transazione** immettere il timeout della transazione in secondi. Il timeout predefinito è di 60 secondi.

4.  Fare clic su **OK**.

**Per impostare il timeout della transazione per un componente utilizzando lo strumento di amministrazione Servizi componenti**

1.  Nell'albero della console fare clic con il pulsante destro del mouse sul componente che si desidera configurare, quindi scegliere **Proprietà**.

2.  Nella finestra di dialogo Proprietà componente fare clic sulla scheda **transazioni** .

3.  Selezionare la casella **Sostituisci valore di timeout transazioni globali**.

    > [!Note]  
    > Non è possibile selezionare la casella per eseguire l'override del valore di timeout della transazione globale se il **supporto delle transazioni** è impostato su **disabilitato**, **non supportato** o **supportato**.

     

4.  In **timeout transazione** immettere il timeout della transazione in secondi. Il timeout predefinito è 0 secondi, il che significa che il componente non provocherà mai il timeout della transazione.

5.  Fare clic su **OK**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione delle transazioni automatiche in COM+](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 



