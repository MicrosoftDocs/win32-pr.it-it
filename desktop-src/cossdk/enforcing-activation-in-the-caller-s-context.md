---
description: Applicazione dell'attivazione nel contesto chiamanti
ms.assetid: bb228f39-0e04-497a-8404-18f7bc027bea
title: Applicazione dell'attivazione nel contesto chiamanti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e42cb657ad7d11f61de0737ca7ac935d1d570649c3e0da9db9b63c79edea38cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119567421"
---
# <a name="enforcing-activation-in-the-callers-context"></a>Applicazione dell'attivazione nel contesto del chiamante

È possibile controllare se un oggetto viene attivato nel proprio contesto. Quando si usa lo strumento amministrativo Servizi componenti per richiedere l'attivazione del componente nel contesto del chiamante, quando COM+ attiva un'istanza del componente in un contesto:

-   L'oggetto viene attivato nel contesto dell'autore, se possibile.
-   L'attivazione dell'oggetto ha esito negativo se richiede il proprio contesto. Viene restituito CO \_ E ATTEMPT TO CREATE OUTSIDE CLIENT \_ \_ \_ \_ \_ \_ CONTEXT.

Il fatto che l'oggetto richieda o meno il proprio contesto dipende dalla configurazione relativa allo stato corrente delle proprietà di contesto del chiamante. Per altre informazioni, vedere [Contesti COM+.](com--contexts.md)

È necessario controllare l'attivazione a tale livello se alcuni aspetti dell'oggetto non funzionerebbero correttamente se ha un proprio contesto. Ad esempio, se il componente non supporta il marshalling e dispone di un proprio contesto, le chiamate al componente avranno esito negativo perché le chiamate tra contesti vengono intercettate e viene eseguito un marshalling leggero.

**Per applicare l'attivazione nel contesto del chiamante**

1.  Nel riquadro dei dettagli dello strumento amministrativo Servizi componenti fare clic con il pulsante destro del mouse sul componente (che si trova nella cartella **Componenti** di qualsiasi applicazione COM+ selezionata) per cui si impostano le proprietà di attivazione e quindi scegliere **Proprietà**.

2.  Nella finestra di dialogo proprietà componente fare clic sulla **scheda** Attivazione.

3.  Selezionare la **casella di controllo Deve essere attivato nel contesto chiamanti.**

4.  Fare clic su **OK**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti relativi all'attivazione just-in-time di COM+](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Applicazione dell'attivazione nel contesto predefinito](enforcing-activation-in-the-default-context.md)
</dt> </dl>

 

 



