---
description: È possibile abilitare la funzionalità auto-done per qualsiasi metodo esposto da un componente per cui è abilitata l'attivazione JIT COM+. Se l'attivazione JIT è disabilitata, l'operazione di completamento automatico non è disponibile.
ms.assetid: d699b85c-441f-4ea6-8d03-d1fa9a8a357f
title: Abilitazione dell'operazione automatica per un metodo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0130e5f8b2fde6c6755ef4174892aa35be8a24cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305142"
---
# <a name="enabling-auto-done-for-a-method"></a>Abilitazione dell'operazione automatica per un metodo

È possibile abilitare la funzionalità auto-done per qualsiasi metodo esposto da un componente per cui è abilitata l'attivazione JIT COM+. Se l'attivazione JIT è disabilitata, l'operazione di completamento automatico non è disponibile.

È necessario abilitare il completamento automatico solo per un metodo che è stato scritto intenzionalmente per sfruttarlo perché questa funzionalità può modificare il comportamento previsto del metodo.

Quando si Abilita l'operazione automatica, si modifica il comportamento predefinito dell'attivazione JIT e delle transazioni automatiche per il metodo. Questa funzionalità può essere utile perché può rimuovere la necessità di dichiarare in modo esplicito la coerenza e la fine. Questa operazione può essere eseguita semplicemente restituendo un HRESULT quando l'operazione di completamento automatico è abilitata. In pratica, quando si Abilita l'operazione automatica, si indica a COM+ di eseguire le operazioni seguenti:

-   Impostare il bit done su true per impostazione predefinita nel contesto in cui viene eseguito l'oggetto ogni volta che viene chiamato questo metodo.
-   Controllare HRESULT restituito dal metodo; Se viene indicato l'ESITo positivo o negativo, impostare di conseguenza il bit di coerenza. Ciò può comportare una chiamata automatica a [**IObjectContext:: Tocomplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) o [**IObjectContext:: SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort), a seconda di ciò che il metodo esegue internamente.

**Per abilitare l'operazione automatica per un metodo**

1.  Nel riquadro dei dettagli dello strumento di amministrazione Servizi componenti fare clic con il pulsante destro del mouse sul metodo che si desidera configurare, quindi scegliere **Proprietà**.

2.  Nella finestra di dialogo Proprietà metodo fare clic sulla scheda **generale** .

3.  Per abilitare il completamento automatico, selezionare la casella di controllo **Disattiva automaticamente questo oggetto quando il metodo restituisce** un risultato. Se la casella di controllo non è disponibile, è necessario abilitare prima l'attivazione JIT per il componente. Per istruzioni dettagliate, vedere[Abilitazione dell'attivazione JIT per un componente](enabling-jit-activation-for-a-component.md) .

4.  Fare clic su **OK**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti relativi all'attivazione JIT di COM+](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Abilitazione dell'attivazione JIT per un componente](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[Impostazione del bit completato](setting-the-done-bit.md)
</dt> </dl>

 

 



