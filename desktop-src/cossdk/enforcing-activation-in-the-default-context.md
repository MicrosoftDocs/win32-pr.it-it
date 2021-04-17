---
description: Un componente COM configurato viene in genere attivato nel relativo contesto; COM+ fa riferimento alle informazioni del catalogo dei componenti per fornire i servizi configurati.
ms.assetid: 09dc7165-22b1-4eca-9591-d83e85556f3f
title: Applicazione dell'attivazione nel contesto predefinito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41599f71dc37c37c1a9a574d274ca2858835e2df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524362"
---
# <a name="enforcing-activation-in-the-default-context"></a>Applicazione dell'attivazione nel contesto predefinito

Un componente COM configurato viene in genere attivato nel relativo contesto; COM+ fa riferimento alle informazioni del catalogo del componente per fornire i servizi configurati. Tuttavia, è possibile scegliere di attivare un componente configurato nel contesto predefinito. Un componente COM di base, ovvero un componente registrato senza informazioni sul catalogo COM+, viene in genere attivato nel contesto predefinito.

L'attivazione di un componente COM nel contesto predefinito offre tre vantaggi principali in termini di prestazioni, come indicato di seguito:

-   È possibile salvare le risorse di sistema limitando il numero di contesti creati.
-   Si aumentano le prestazioni limitando il numero di chiamate tra più contesti. Poiché le chiamate tra contesti richiedono il marshalling, è molto più veloce per un oggetto COM attivato nel contesto predefinito per effettuare chiamate ad altri oggetti nel contesto predefinito. Le prestazioni in questo caso (di chiamate all'interno dello stesso contesto) sono simili a quelle della chiamata a una subroutine.
-   È possibile importare le applicazioni COM meno recenti in COM+ ed eseguirle senza problemi. È possibile, ad esempio, che si disponga di più applicazioni COM meno recenti implementate in base al presupposto che sia possibile passare riferimenti a oggetti all'interno di un Apartment senza effettuare il marshalling dei riferimenti. Queste applicazioni COM non funzionano quando vengono importate in COM+ perché i riferimenti agli oggetti vengono passati tra i limiti del contesto. Tuttavia, è possibile eseguire questo tipo di applicazione COM quando viene importato se si utilizza lo strumento di amministrazione Servizi componenti per contrassegnare tutte le classi nell'applicazione come **deve essere attivato nel contesto predefinito**.

Lo svantaggio principale dell'attivazione di un componente configurato nel contesto predefinito è che COM+ non fornisce alcun servizio configurato per il componente. Si verifica un compromesso tra prestazioni migliorate e la possibilità di utilizzare i servizi COM+.

Si supponga, ad esempio, che un componente COM non richieda alcun servizio COM+, ad esempio [transazioni](com--transactions.md), [attivazione JIT](com--just-in-time-activation.md), [eventi](com--events.md), componenti in [coda](com--queued-components.md), [sincronizzazione](com--synchronization.md)o pool di [oggetti](com--object-pooling.md), e che il componente effettua un certo numero di chiamate ad altri componenti com che possono essere attivati nel contesto predefinito. In questo caso, è consigliabile attivare il componente chiamante nel contesto predefinito.

Se il componente COM richiede servizi COM+, non può essere contrassegnato come **deve essere attivato nel contesto predefinito**. Inoltre, non esiste un miglioramento delle prestazioni reale se un oggetto COM attivato nel contesto predefinito esegue una serie di chiamate a oggetti in altri contesti. Per informazioni dettagliate, vedere [contesti](com--contexts.md).

**Per applicare l'attivazione nel contesto predefinito**

1.  Nel riquadro dei dettagli dello strumento di amministrazione Servizi componenti fare clic con il pulsante destro del mouse sul componente (che si trova all'interno della cartella **componenti** di qualsiasi applicazione COM+ selezionata) che si desidera attivare nel contesto predefinito, quindi fare clic su **Proprietà**.

2.  Nella finestra di dialogo Proprietà componente fare clic sulla scheda **attivazione** .

3.  Selezionare la casella **di controllo deve essere attivato nel contesto predefinito**.

4.  Fare clic su **OK**.

> [!Note]  
> Quando si esegue un componente configurato nel contesto predefinito, COM+ non attiva alcuno dei servizi configurati per tale componente. Questi servizi sono nuovamente disponibili quando si deseleziona la casella **di controllo deve essere attivato nel contesto predefinito** ed eseguire successivamente il componente configurato nel relativo contesto.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti relativi all'attivazione JIT di COM+](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Applicazione dell'attivazione nel contesto del chiamante](enforcing-activation-in-the-caller-s-context.md)
</dt> </dl>

 

 



