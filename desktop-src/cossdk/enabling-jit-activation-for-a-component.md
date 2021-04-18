---
description: Abilitazione dell'attivazione JIT per un componente
ms.assetid: ccf7c98b-8b1a-431d-b417-83f79734f691
title: Abilitazione dell'attivazione JIT per un componente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f61cc5c79270a926bb50e3408766df63f4484c8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304951"
---
# <a name="enabling-jit-activation-for-a-component"></a>Abilitazione dell'attivazione JIT per un componente

È necessario configurare un componente per l'attivazione JIT solo quando viene scritto correttamente per supportare il servizio di attivazione JIT (just-in-Time) COM+. Se un componente viene disattivato tra le chiamate al metodo, perderà qualsiasi stato associato. Dato il comportamento predefinito dell'attivazione JIT, questo errore si verifica quando non è previsto, ma è necessario conoscere i requisiti di un componente prima di modificarne la configurazione e le aspettative dei client che chiameranno il componente.

> [!Note]  
> Se un componente è configurato per richiedere transazioni, il servizio di attivazione JIT COM+ viene abilitato automaticamente. In questo caso, non è possibile disabilitarlo. Per informazioni dettagliate, vedere [configurazione di transazioni](configuring-transactions.md).

 

Quando si Abilita l'attivazione JIT per un componente, il relativo attributo di sincronizzazione viene impostato su Required per quel componente. In questo caso, non è possibile modificare l'impostazione di sincronizzazione. Per informazioni dettagliate, vedere [dipendenze di sincronizzazione](synchronization-dependencies.md).

**Per abilitare l'attivazione JIT**

1.  Nel riquadro dei dettagli dello strumento di amministrazione Servizi componenti fare clic con il pulsante destro del mouse sul componente che si desidera configurare, quindi scegliere **Proprietà**.

2.  Nella finestra di dialogo Proprietà componente fare clic sulla scheda **attivazione** .

3.  Per abilitare l'attivazione JIT per il componente, selezionare la casella di controllo **Abilita attivazione Just-in-Time** .

4.  Fare clic su **OK**.

Quando è stata abilitata l'attivazione JIT per un componente, è possibile abilitare la funzionalità auto-done per qualsiasi metodo esposto da tale componente. Per ulteriori informazioni, vedere [Abilitazione dell'operazione automatica per un metodo](enabling-auto-done-for-a-method.md) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Abilitazione dell'operazione automatica per un metodo](enabling-auto-done-for-a-method.md)
</dt> <dt>

[Impostazione del bit completato](setting-the-done-bit.md)
</dt> </dl>

 

 



