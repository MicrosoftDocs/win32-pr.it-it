---
description: È possibile abilitare la funzionalità di completamento automatico per qualsiasi metodo esposto da un componente per cui è abilitata l'attivazione JIT COM+. Se l'attivazione JIT è disabilitata, l'esecuzione automatica non è disponibile.
ms.assetid: d699b85c-441f-4ea6-8d03-d1fa9a8a357f
title: Abilitazione del completamento automatico per un metodo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58eec7a7b87284145ea880338bfe61db2aa1afca06f1f83ee811e4375a1e473c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637691"
---
# <a name="enabling-auto-done-for-a-method"></a>Abilitazione del completamento automatico per un metodo

È possibile abilitare la funzionalità di completamento automatico per qualsiasi metodo esposto da un componente per cui è abilitata l'attivazione JIT COM+. Se l'attivazione JIT è disabilitata, l'esecuzione automatica non è disponibile.

È consigliabile abilitare l'esecuzione automatica solo per un metodo che è stato intenzionalmente scritto per sfruttarlo perché questa funzionalità può potenzialmente modificare il comportamento previsto del metodo.

Quando si abilita l'esecuzione automatica, si modifica il comportamento predefinito dell'attivazione JIT e delle transazioni automatiche per tale metodo. È possibile usare questa funzionalità perché può rimuovere la necessità di dichiarare in modo esplicito coerenza e coerenza. Questa operazione può invece essere eseguita semplicemente tramite la restituzione di un valore HRESULT quando è abilitata l'esecuzione automatica. Essenzialmente, quando si abilita l'esecuzione automatica, si indica a COM+ di eseguire le operazioni seguenti:

-   Impostare il bit done su True per impostazione predefinita nel contesto in cui viene eseguito l'oggetto ogni volta che viene chiamato questo metodo.
-   Esaminare il valore HRESULT restituito dal metodo . Se indica SUCCESS o FAILURE, impostare il bit di coerenza di conseguenza. Ciò può comportare una chiamata automatica a [**IObjectContext::SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) o [**IObjectContext::SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort), a seconda delle attività del metodo internamente.

**Per abilitare l'esecuzione automatica per un metodo**

1.  Nel riquadro dei dettagli dello strumento di amministrazione Servizi componenti fare clic con il pulsante destro del mouse sul metodo che si desidera configurare e quindi scegliere **Proprietà.**

2.  Nella finestra di dialogo delle proprietà del metodo fare clic **sulla scheda** Generale .

3.  Per abilitare l'esecuzione automatica, selezionare la casella di controllo Disattiva automaticamente questo oggetto quando **viene restituito questo** metodo. Se la casella di controllo non è disponibile, è prima necessario abilitare l'attivazione JIT per il componente. Per istruzioni[dettagliate, vedere Abilitazione](enabling-jit-activation-for-a-component.md) dell'attivazione JIT per un componente.

4.  Fare clic su **OK**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti relativi all'attivazione just-in-time COM+](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Abilitazione dell'attivazione JIT per un componente](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[Impostazione del bit done](setting-the-done-bit.md)
</dt> </dl>

 

 



