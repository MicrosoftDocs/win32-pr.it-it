---
description: Un componente COM configurato viene in genere attivato nel proprio contesto. in altre parti, COM+ fa riferimento alle informazioni del catalogo dei componenti per fornire tutti i servizi configurati.
ms.assetid: 09dc7165-22b1-4eca-9591-d83e85556f3f
title: Applicazione dell'attivazione nel contesto predefinito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d188fb50521e09c88a9c61136e33928176faa1f70a94680b31cf0cc1e75cb8eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120070761"
---
# <a name="enforcing-activation-in-the-default-context"></a>Applicazione dell'attivazione nel contesto predefinito

Un componente COM configurato viene in genere attivato nel proprio contesto. com+ fa riferimento alle informazioni del catalogo del componente per fornire tutti i servizi configurati. Tuttavia, è possibile scegliere di attivare un componente configurato nel contesto predefinito. Un componente COM di base, ovvero un componente registrato senza informazioni sul catalogo COM+, viene in genere attivato nel contesto predefinito.

L'attivazione di un componente COM nel contesto predefinito offre tre vantaggi principali in termini di prestazioni, come indicato di seguito:

-   È possibile salvare le risorse di sistema limitando il numero di contesti creati.
-   È possibile migliorare le prestazioni limitando il numero di chiamate tra contesti. Poiché le chiamate tra contesti richiedono il marshalling, è molto più veloce per un oggetto COM attivato nel contesto predefinito effettuare chiamate ad altri oggetti nel contesto predefinito. Le prestazioni in questo caso (delle chiamate all'interno dello stesso contesto) sono simili a quelle della chiamata a una subroutine.
-   È possibile importare applicazioni COM meno recenti in COM+ ed eseguirle senza problemi. Ad esempio, si potrebbero avere diverse applicazioni COM meno recenti implementate presupponendo che fosse possibile passare riferimenti a oggetti all'interno di un apartment senza effettuare il marshalling dei riferimenti. Queste applicazioni COM non funzionano quando vengono importate in COM+ perché i riferimenti agli oggetti vengono passati attraverso i limiti di contesto. Tuttavia, è possibile eseguire questo tipo di applicazione COM quando viene importato se si usa lo strumento di amministrazione Servizi componenti per contrassegnare tutte le classi dell'applicazione come Deve essere attivato nel **contesto predefinito**.

Lo svantaggio principale dell'attivazione di un componente configurato nel contesto predefinito è che COM+ non fornisce alcun servizio configurato del componente. Esiste un compromesso tra le prestazioni migliorate e la possibilità di usare i servizi COM+.

Si supponga, ad esempio, che un componente COM non richieda servizi COM+, ad esempio Transazioni [,](com--transactions.md)Attivazione [JUST-In-Time](com--just-in-time-activation.md) [,](com--events.md)Eventi [,](com--queued-components.md)Componenti in coda [,](com--synchronization.md)Sincronizzazione o [Pool di](com--object-pooling.md)oggetti , e che il componente esempli una serie di chiamate ad altri componenti COM che possono essere attivati nel contesto predefinito. In questo caso, è buona idea attivare il componente chiamante nel contesto predefinito.

Se il componente COM richiede servizi COM+, non può essere contrassegnato come **Deve essere attivato nel contesto predefinito.** Inoltre, non vi è alcun reale miglioramento delle prestazioni se un oggetto COM attivato nel contesto predefinito effettua una serie di chiamate a oggetti in altri contesti. Per altri dettagli, vedere [Contesti.](com--contexts.md)

**Per applicare l'attivazione nel contesto predefinito**

1.  Nel riquadro dei dettagli dello strumento di amministrazione Servizi componenti fare clic con il pulsante destro del mouse sul componente (che si trova nella cartella **Componenti** di qualsiasi applicazione COM+ selezionata) che si desidera attivare nel contesto predefinito e quindi scegliere **Proprietà**.

2.  Nella finestra di dialogo delle proprietà del componente fare clic **sulla scheda** Attivazione .

3.  Selezionare la **casella di controllo Deve essere attivato nel contesto** predefinito .

4.  Fare clic su **OK**.

> [!Note]  
> Quando si esegue un componente configurato nel contesto predefinito, COM+ non attiva alcun servizio configurato per tale componente. Questi servizi sono nuovamente disponibili quando si deseleziona la casella di controllo Deve essere attivato nel contesto predefinito e successivamente si esegue il componente configurato nel proprio contesto.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Concetti relativi all'attivazione just-in-time COM+](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Applicazione dell'attivazione nel contesto del chiamante](enforcing-activation-in-the-caller-s-context.md)
</dt> </dl>

 

 



