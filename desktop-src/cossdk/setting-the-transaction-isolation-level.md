---
description: È possibile impostare manualmente il livello di isolamento delle transazioni dei componenti utilizzando lo strumento di amministrazione Servizi componenti oppure è possibile configurare a livello di codice il livello di isolamento delle transazioni per un componente utilizzando le interfacce di amministrazione COM+.
ms.assetid: 3ef5b805-334d-4803-be67-00c9e35cdcc6
title: Impostazione del livello di isolamento delle transazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b0447af2591c4f4b3e8e76c017157c02908367
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748842"
---
# <a name="setting-the-transaction-isolation-level"></a>Impostazione del livello di isolamento delle transazioni

È possibile impostare manualmente il livello di isolamento delle transazioni dei componenti utilizzando lo strumento di amministrazione Servizi componenti oppure è possibile configurare a livello di codice il livello di isolamento delle transazioni per un componente utilizzando le [interfacce di amministrazione com+](com--administration-interfaces.md).

Per ulteriori informazioni sui livelli di isolamento delle transazioni, vedere [configurazione dei livelli di isolamento delle transazioni](configuring-transaction-isolation-levels.md).

**Per impostare il livello di isolamento della transazione utilizzando lo strumento di amministrazione Servizi componenti**

1.  Nell'albero della console fare clic con il pulsante destro del mouse sul componente che si desidera configurare, quindi scegliere **Proprietà**.

2.  Nella finestra di dialogo Proprietà componente fare clic sulla scheda **transazioni** .

3.  In **livello di isolamento transazione** selezionare il valore desiderato dalla casella di riepilogo a discesa. Il valore predefinito per tutti i componenti viene **serializzato**.

    > [!Note]  
    > Se è selezionato **disabilitato** o **non supportato** in **supporto transazioni**, non è possibile impostare il livello di isolamento della transazione.

     

4.  Fare clic su **OK**.

È necessario ripetere questa procedura per ogni componente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione di livelli di isolamento delle transazioni](configuring-transaction-isolation-levels.md)
</dt> </dl>

 

 



