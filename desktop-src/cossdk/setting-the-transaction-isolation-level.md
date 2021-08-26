---
description: È possibile impostare manualmente il livello di isolamento delle transazioni dei componenti usando lo strumento di amministrazione Servizi componenti oppure configurare a livello di codice il livello di isolamento delle transazioni per un componente tramite le interfacce di amministrazione COM+.
ms.assetid: 3ef5b805-334d-4803-be67-00c9e35cdcc6
title: Impostazione del livello di isolamento delle transazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96af7017f8a46f11428bfacf7282a7d4ae61b4dc3c1fd5bb7e82588f8fff6110
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029461"
---
# <a name="setting-the-transaction-isolation-level"></a>Impostazione del livello di isolamento delle transazioni

È possibile impostare manualmente il livello di isolamento delle transazioni dei componenti tramite lo strumento di amministrazione Servizi componenti oppure configurare a livello di codice il livello di isolamento della transazione per un componente utilizzando le interfacce di amministrazione [COM+.](com--administration-interfaces.md)

Per altre informazioni sui livelli di isolamento delle transazioni, vedere [Configurazione dei livelli di isolamento delle transazioni.](configuring-transaction-isolation-levels.md)

**Per impostare il livello di isolamento delle transazioni utilizzando lo strumento di amministrazione Servizi componenti**

1.  Nell'albero della console fare clic con il pulsante destro del mouse sul componente che si desidera configurare e quindi scegliere **Proprietà.**

2.  Nella finestra di dialogo proprietà componente fare clic **sulla scheda** Transazioni .

3.  In **Livello di isolamento transazione** selezionare il valore desiderato dalla casella di riepilogo a discesa. Il valore predefinito per tutti i componenti è **Serializzato.**

    > [!Note]  
    > Se si seleziona **Disabilitato** o **Non supportato** in **Supporto transazioni**, non è possibile impostare il livello di isolamento della transazione.

     

4.  Fare clic su **OK**.

È necessario ripetere questa procedura per ogni componente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione dei livelli di isolamento delle transazioni](configuring-transaction-isolation-levels.md)
</dt> </dl>

 

 



