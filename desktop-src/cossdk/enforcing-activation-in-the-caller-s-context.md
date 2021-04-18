---
description: Applicazione dell'attivazione nel contesto dei chiamanti
ms.assetid: bb228f39-0e04-497a-8404-18f7bc027bea
title: Applicazione dell'attivazione nel contesto dei chiamanti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70af40f92056e679a9211964b8a614cbeaeb4a6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304618"
---
# <a name="enforcing-activation-in-the-callers-context"></a>Applicazione dell'attivazione nel contesto del chiamante

È possibile controllare se un oggetto viene attivato in un contesto. Quando si utilizza lo strumento di amministrazione Servizi componenti per richiedere l'attivazione del componente nel contesto del chiamante, si verifica quanto segue quando COM+ attiva un'istanza del componente in un contesto:

-   Se possibile, l'oggetto viene attivato nel contesto del creatore.
-   L'attivazione dell'oggetto ha esito negativo se richiede il proprio contesto; \_ \_ \_ Viene restituito il tentativo di \_ creare il \_ \_ contesto client esterno \_ .

Il fatto che l'oggetto richieda il proprio contesto dipende dalla configurazione relativa allo stato corrente delle proprietà di contesto del chiamante. Per informazioni dettagliate, vedere [contesti com+](com--contexts.md).

È possibile controllare l'attivazione a tale livello se un aspetto dell'oggetto non funziona correttamente se dispone di un contesto. Se, ad esempio, il componente non supporta il marshalling e ha il proprio contesto, le chiamate a tale componente avranno esito negativo perché le chiamate tra i contesti vengono intercettate e viene eseguito un marshalling leggero.

**Per applicare l'attivazione nel contesto del chiamante**

1.  Nel riquadro dei dettagli dello strumento di amministrazione Servizi componenti fare clic con il pulsante destro del mouse sul componente (che si trova nella cartella **componenti** di qualsiasi applicazione COM+ selezionata) per la quale si stanno impostando le proprietà di attivazione e quindi fare clic su **Proprietà**.

2.  Nella finestra di dialogo Proprietà componente fare clic sulla scheda **attivazione** .

3.  Selezionare la casella **di controllo deve essere attivato nel contesto dei chiamanti** .

4.  Fare clic su **OK**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti relativi all'attivazione JIT di COM+](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Applicazione dell'attivazione nel contesto predefinito](enforcing-activation-in-the-default-context.md)
</dt> </dl>

 

 



