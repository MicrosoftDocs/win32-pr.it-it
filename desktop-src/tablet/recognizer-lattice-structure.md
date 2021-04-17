---
description: I riconoscitori creati per l'utilizzo con Windows Vista e Windows XP Tablet PC Edition utilizzano un set di strutture, ciascuno dei quali è denominato reticolo, per passare i risultati del riconoscimento alle librerie della piattaforma Tablet PC.
ms.assetid: 628ca677-31eb-47d9-bcc6-d7777f8aaf7c
title: Struttura del reticolo del riconoscitore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46bbfe71674571ae0554509dfa8477569ef8b44d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104559476"
---
# <a name="recognizer-lattice-structure"></a>Struttura del reticolo del riconoscitore

I riconoscitori creati per l'utilizzo con Windows Vista e Windows XP Tablet PC Edition utilizzano un set di strutture, ciascuno dei quali è denominato reticolo, per passare i risultati del riconoscimento alle librerie della piattaforma Tablet PC. La piattaforma Tablet PC copia quindi le informazioni contenute in queste strutture nell'oggetto [**IInkRecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) , nella raccolta [**IInkRecognitionAlternates**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternates) e nell'oggetto [**IInkRecognitionAlternate**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate) .

Un puntatore al reticolo deve essere restituito dal riconoscimento quando la piattaforma chiama la funzione [**GetLatticePtr**](/windows/desktop/api/recapis/nf-recapis-getlatticeptr) sull'handle [HRECOCONTEXT](hrecocontext-handle.md) .

In questa sezione viene descritta in dettaglio la struttura del reticolo. Per una panoramica dei riconoscitori e dei concetti correlati, vedere [informazioni sul riconoscimento della grafia](about-handwriting-recognition.md).

## <a name="the-need-for-a-lattice"></a>Necessità di un reticolo

Un riconoscitore può trovare diversi modi per suddividere un set di tratti di input penna in segmenti di riconoscimento. Ciò che il riconoscimento USA come segmento di riconoscimento dipende dal tipo di riconoscimento. I riconoscitori della lingua inglese usano in genere parole come segmento di riconoscimento. Altri riconoscitori potrebbero usare caratteri, forme o movimenti come segmento di riconoscimento. La flessibilità delle strutture di reticolo consente la gestione logica dell'elevato numero di risultati del riconoscimento che possono essere combinati in relazioni complesse.

Internamente, i riconoscitori utilizzano un reticolo per conservare le unità di riconoscimento di base per un determinato pezzo di input penna. Il reticolo include anche il punteggio, o livello di confidenza, del risultato combinato. Inoltre, il reticolo archivia il mapping dei segmenti ai tratti di input penna originali.

Le strutture di reticolo sono definite nel file di intestazione rectypes. h. Le strutture di reticolo includono le strutture seguenti:

-   [**\_reticolo unto**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice)
-   [**\_colonna reticolo \_ unto**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_column)
-   [**\_elemento del reticolo unto \_**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_element)
-   [**\_proprietà del reticolo unto \_**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_properties)
-   [**\_Proprietà reticolo \_ unto**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_property)

## <a name="lattice-components"></a>Componenti reticolo

Negli esempi seguenti vengono usati i tratti per la parola "Together", come illustrato nella figura seguente. Negli esempi, i segmenti vengono valutati come una o più parole. I numeri rappresentano i singoli tratti del segmento valutato. Si noti che ognuno dei caratteri "t" contiene due tratti.

![tratti per la parola "Together"](images/1d5fa9fb-6c38-49b8-8caa-2b6dcc1d5dec.gif)

Un reticolo è costituito da una o più colonne, una per ogni segmento. Ogni colonna contiene a sua volta uno o più elementi. Un elemento include un'alternativa di riconoscimento discreto. Per ulteriori informazioni sulle colonne, vedere la struttura della [**\_ \_ colonna del reticolo unto**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_column) . Per ulteriori informazioni sugli elementi, vedere la struttura dell' [**\_ \_ elemento lattice unto**](/windows/win32/api/rectypes/ns-rectypes-reco_lattice_element) .

Il riconoscimento può restituire un singolo segmento durante la valutazione dell'esempio di input penna illustrato nell'esempio precedente. In questo caso il reticolo contiene una singola colonna con un singolo elemento.

Un esempio più complesso si presenta quando il riconoscimento valuta l'esempio di input penna e viene visualizzato con più segmenti e più alternative per ogni segmento.

Il numero di alternative di riconoscimento può essere scaglionato, anche per un piccolo esempio di input penna. Ad esempio, "t o g e t h e r" possono produrre i risultati seguenti:

-   "per ottenerlo" (più alternative per ogni parola)
-   "da raccogliere" (più alternative per ogni parola)
-   "per ottenerlo" (più alternative per ogni parola)
-   "insieme" (più alternative per la parola)

In questo caso, un riconoscimento potrebbe creare la struttura di reticolo seguente.

![struttura di reticolo per la parola "Together"](images/2496c3dd-8b08-4f86-9fe3-f118be49a8c8.gif)

> [!Note]  
> Ogni colonna condivide lo stesso ordine del tratto perché tutti fanno riferimento alla stessa raccolta [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) .

 

 

 
