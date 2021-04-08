---
title: Procedure consigliate per DirectComposition
description: Questo argomento descrive le procedure consigliate per l'uso di Microsoft DirectComposition.
ms.assetid: D3A1ECD4-9358-44B9-8A84-7D901219D5CD
keywords:
- procedure consigliate per DirectComposition
- procedure consigliate per DirectComposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f0d19b82b188105c7914e89282c08b12dd4bdc4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729898"
---
# <a name="best-practices-for-directcomposition"></a>Procedure consigliate per DirectComposition

> [!NOTE]
> Per le app in Windows 10, è consigliabile usare le API Windows. UI. Composition anziché DirectComposition. Per altre informazioni, vedere [modernizzare l'app desktop usando il livello visivo](/windows/uwp/composition/visual-layer-in-desktop-apps).

Questo argomento descrive le procedure consigliate per l'uso di Microsoft DirectComposition.

-   [Procedure consigliate](#best-practices-for-directcomposition)
-   [Considerazioni sulla sicurezza](#security-considerations)
-   [Argomenti correlati](#related-topics)

## <a name="best-practices"></a>Procedure consigliate

La tabella seguente illustra le procedure consigliate per l'uso degli oggetti visivi di Microsoft DirectComposition.



| Procedure consigliate                                                                                                                                                                                                                                                        | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Dopo la creazione di un dispositivo DirectComposition, chiamare il metodo [**IDCompositionDevice:: CheckDeviceState**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-checkdevicestate) in risposta a ogni messaggio di [**\_ disegno WM**](/windows/desktop/gdi/wm-paint) per verificare che il dispositivo sia ancora valido.<br/> | Se il dispositivo Microsoft DirectX Graphics Infrastructure (DXGI) viene perso, anche il dispositivo DirectComposition associato al dispositivo DXGI viene perso. Quando rileva un dispositivo smarrito, DirectComposition invia il messaggio di [**\_ disegno WM**](/windows/desktop/gdi/wm-paint) a tutte le finestre. La chiamata di [**CheckDeviceState**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-checkdevicestate) in risposta a ogni messaggio di **\_ disegno WM** consente di determinare se l'oggetto dispositivo DirectComposition è ancora valido e, in caso contrario, di eseguire le operazioni per ripristinare il contenuto. <br/> Per altre informazioni, vedere [oggetto dispositivo](basic-concepts.md).<br/> |
| Creare solo il numero di oggetti visivi necessari per una composizione o un'animazione ed eliminare gli oggetti visivi immediatamente dopo che DirectComposition termina di usarli.<br/>                                                                                            | DirectComposition usa la GPU (Graphics Processing Unit), una risorsa che l'applicazione condivide con altre applicazioni e il sistema operativo. Questa procedura garantisce che tutte le applicazioni e il sistema operativo ricevano risorse GPU adeguate.<br/> Per altre informazioni, vedere oggetti [visivi](basic-concepts.md).<br/>                                                                                                                                                                                                                                                                     |
| Non nascondere gli oggetti visivi impostando l'opacità su 0%; rimuovere invece oggetti visivi dalla struttura ad albero visuale.<br/>                                                                                                                                                          | Per impostare l'opacità su 0% è necessario disporre di più risorse di sistema rispetto alla rimozione dalla struttura ad albero visuale.<br/> Per altre informazioni, vedere [opacità](effects.md) e [struttura ad albero visuale](basic-concepts.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| Non nascondere un oggetto visivo applicando un rettangolo di ritaglio vuoto (zero size) a un oggetto visivo. Rimuovere invece l'oggetto visivo dalla struttura ad albero visuale. <br/>                                                                                                                 | La rimozione di un oggetto visivo dalla struttura ad albero visuale comporta prestazioni migliori rispetto all'applicazione di un rettangolo di ritaglio vuoto.<br/> Per ulteriori informazioni, vedere [ritaglio](clipping.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Non applicare un rettangolo di ritaglio a un oggetto visivo se il rettangolo di ritaglio non è necessario, ad esempio un rettangolo di ritaglio che include l'intero contenuto bitmap dell'oggetto visivo.<br/>                                                                                       | I rettangoli di ritaglio non necessari danno le prestazioni del sistema.<br/> Per ulteriori informazioni, vedere [ritaglio](clipping.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Se è necessaria una bitmap di grandi dimensioni a colore singolo, creare una superficie bitmap più piccola, quindi applicare una trasformazione scala anziché creare una superficie a dimensione intera. <br/>                                                                                                | L'applicazione di una trasformazione di ridimensionamento a una superficie più piccola usa un minor numero di risorse di sistema rispetto a una superficie a dimensione intera.<br/> Per altre informazioni, vedere [oggetti bitmap](bitmap-surfaces.md) e [trasformazioni](transforms.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| Evitare di applicare trasformazioni 3D a più livelli di una struttura ad albero visuale, ad esempio a un padre e ai relativi discendenti. <br/>                                                                                                                                        | L'applicazione di trasformazioni 3D a più livelli di una struttura ad albero visuale può produrre risultati imprevisti perché le trasformazioni 3D non vengono moltiplicate nell'albero. Ad esempio, una rotazione di 90 gradi intorno all'asse y su un figlio e una rotazione di 90 gradi intorno all'asse y in un elemento padre, il risultato è la rotazione di entrambi gli oggetti visivi.<br/> Per altre informazioni, vedere [Effects](effects.md) (Effetti).<br/>                                                                                                                                                                                                     |



 

## <a name="security-considerations"></a>Considerazioni relative alla sicurezza

Gli articoli seguenti forniscono indicazioni per la scrittura di codice C++ sicuro.

-   [Procedure di protezione ottimali per C++](/cpp/security/security-best-practices-for-cpp?view=vs-2019)
-   [Modelli & procedure consigliate per la sicurezza delle applicazioni](/previous-versions/msp-n-p/ff650760(v=pandp.10))

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come usare DirectComposition](how-to-use-directcomposition.md)
</dt> </dl>

 

