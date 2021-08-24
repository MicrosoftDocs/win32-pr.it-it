---
description: Abilitazione dell'attivazione JIT per un componente
ms.assetid: ccf7c98b-8b1a-431d-b417-83f79734f691
title: Abilitazione dell'attivazione JIT per un componente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9beac51cd4f97a451b372d8eeee8ef419ead3140a672ca85dcdc3740d8c52de4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637701"
---
# <a name="enabling-jit-activation-for-a-component"></a>Abilitazione dell'attivazione JIT per un componente

È necessario configurare un componente per l'attivazione JIT solo quando viene scritto correttamente per supportare il servizio di attivazione JIT COM+. Se un componente viene disattivato tra le chiamate al metodo, perderà qualsiasi stato associato. Dato il comportamento predefinito dell'attivazione JIT, è improbabile che si verifichi quando non lo si prevede, ma è necessario tenere presenti i requisiti di un componente prima di modificarne la configurazione e delle aspettative dei client che chiameranno il componente.

> [!Note]  
> Se un componente è configurato per richiedere transazioni, il servizio Attivazione JIT COM+ viene abilitato automaticamente. Non è possibile disabilitarlo in questo caso. Per altre informazioni, vedere [Configurazione delle transazioni](configuring-transactions.md).

 

Quando si abilita l'attivazione JIT per un componente, il relativo attributo di sincronizzazione viene impostato su required per tale componente. In questo caso non è possibile modificare l'impostazione di sincronizzazione. Per altre informazioni, vedere [Dipendenze di sincronizzazione](synchronization-dependencies.md).

**Per abilitare l'attivazione JIT**

1.  Nel riquadro dei dettagli dello strumento amministrativo Servizi componenti fare clic con il pulsante destro del mouse sul componente che si desidera configurare e quindi scegliere **Proprietà**.

2.  Nella finestra di dialogo proprietà componente fare clic sulla **scheda** Attivazione.

3.  Per abilitare l'attivazione JIT per il componente, selezionare la casella di controllo Abilita attivazione **JIT.**

4.  Fare clic su **OK**.

Dopo aver abilitato l'attivazione JIT per un componente, è possibile abilitare la funzionalità di completamento automatico per qualsiasi metodo esposto da tale componente. Per [altre informazioni, vedere Abilitazione del](enabling-auto-done-for-a-method.md) completamento automatico per un metodo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Abilitazione del completamento automatico per un metodo](enabling-auto-done-for-a-method.md)
</dt> <dt>

[Impostazione del bit done](setting-the-done-bit.md)
</dt> </dl>

 

 



