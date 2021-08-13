---
description: I sistemi di riconoscimento creati per l'uso con Windows Vista e Windows XP Tablet PC Edition usano un set di strutture, ognuna denominata reticolo, per passare i risultati del riconoscimento alle librerie della piattaforma Tablet PC.
ms.assetid: 628ca677-31eb-47d9-bcc6-d7777f8aaf7c
title: Struttura del reticolo del riconoscitore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc5610d60428bd3259672f43e45efa59c25f78b7ddc5909c363610eaf08520e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118716021"
---
# <a name="recognizer-lattice-structure"></a>Struttura del reticolo del riconoscitore

I sistemi di riconoscimento creati per l'uso con Windows Vista e Windows XP Tablet PC Edition usano un set di strutture, ognuna denominata reticolo, per passare i risultati del riconoscimento alle librerie della piattaforma Tablet PC. La piattaforma Tablet PC copia quindi le informazioni in queste strutture nell'oggetto [**IInkRecognitionResult,**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) nella raccolta [**IInkRecognitionAlternates**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates) e nell'oggetto [**IInkRecognitionAlternate.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate)

Un puntatore al reticolo deve essere restituito dal riconoscimento quando la piattaforma chiama la [**funzione GetLatticePtr**](/windows/desktop/api/recapis/nf-recapis-getlatticeptr) sull'handle [HRECOCONTEXT.](hrecocontext-handle.md)

Questa sezione descrive in dettaglio la struttura a reticolo. Per una panoramica dei riconoscitori e dei concetti correlati, vedere [Informazioni sul riconoscimento della grafia.](about-handwriting-recognition.md)

## <a name="the-need-for-a-lattice"></a>Necessità di un reticolo

Un riconoscitore può trovare diversi modi per suddividere un set di tratti input penna in segmenti di riconoscimento. Ciò che il riconoscimento usa come segmento di riconoscimento dipende dal tipo di riconoscimento. I riconoscitori di lingua inglese usano in genere parole come segmento di riconoscimento. Altri riconoscitori potrebbero usare caratteri, forme o movimenti come segmento di riconoscimento. La flessibilità delle strutture a reticolo consente la gestione logica del numero elevato di risultati di riconoscimento che possono essere combinati in relazioni complesse.

Internamente, i riconoscitori usano un reticolo per contenere le unità di riconoscimento di base per una determinata parte dell'input penna. Il reticolo contiene anche il punteggio, o livello di confidenza, del risultato combinato. Inoltre, il reticolo archivia il mapping dei segmenti ai tratti input penna originali.

Le strutture a reticolo sono definite nel file di intestazione RecTypes.h. Le strutture a reticolo includono le strutture seguenti:

-   [**RECO \_ LATTICE**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice)
-   [**RECO \_ LATTICE \_ COLUMN**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_column)
-   [**ELEMENTO \_ RECO \_ LATTICE**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_element)
-   [**PROPRIETÀ \_ RECO \_ LATTICE**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_properties)
-   [**RECO \_ \_ LATTICE - PROPRIETÀ**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_property)

## <a name="lattice-components"></a>Componenti del reticolo

Gli esempi seguenti usano i tratti per la parola "insieme", come illustrato nell'immagine seguente. Negli esempi i segmenti vengono valutati come una o più parole. I numeri rappresentano i singoli tratti del segmento valutato. Si noti che ognuno dei caratteri "t" contiene due tratti.

![tratti per la parola "insieme"](images/1d5fa9fb-6c38-49b8-8caa-2b6dcc1d5dec.gif)

Un reticolo è costituito da una o più colonne, una per ogni segmento. Ogni colonna contiene a sua volta uno o più elementi . Un elemento contiene un'alternativa di riconoscimento discreto. Per altre informazioni sulle colonne, vedere la [**struttura RECO \_ LATTICE \_ COLUMN.**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_column) Per altre informazioni sugli elementi, vedere la [**struttura RECO \_ LATTICE \_ ELEMENT.**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_element)

Il riconoscitore potrebbe restituire un singolo segmento durante la valutazione dell'esempio di input penna illustrato nell'esempio precedente. In questo caso il reticolo contiene una singola colonna con un singolo elemento.

Un esempio più complesso si presenta quando il riconoscimento valuta il campione di input penna e include più segmenti e più alternative per ogni segmento.

Il numero di alternative di riconoscimento può essere sfalsato, anche per un campione di input penna di piccole dimensioni. Ad esempio, "t o g e t h e r" può produrre i risultati seguenti:

-   "per ottenerla" (più alternative per ogni parola)
-   "to gather" (più alternative per ogni parola)
-   "to got her" (più alternative per ogni parola)
-   "together" (più alternative per la parola)

In questo caso, un sistema di riconoscimento potrebbe creare la struttura a reticolo seguente.

![struttura a reticolo per la parola "insieme"](images/2496c3dd-8b08-4f86-9fe3-f118be49a8c8.gif)

> [!Note]  
> Ogni colonna condivide lo stesso ordine dei tratti perché fanno tutti riferimento alla stessa [raccolta InkStrokes.](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))

 

 

 
