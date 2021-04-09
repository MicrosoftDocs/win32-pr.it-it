---
description: Un riconoscitore può trovare diversi modi per suddividere un esempio di input penna in segmenti di riconoscimento. Per questo motivo, il numero di alternative di riconoscimento può essere scaglionato, anche per un piccolo esempio di input penna.
ms.assetid: 7ecffe3f-cbe4-4e65-a1cc-9b08534b26c9
title: Segmenti di input penna e alternative
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91183f6c9628ea798b66d703a59e44b26049e692
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049461"
---
# <a name="ink-segments-and-alternates"></a>Segmenti di input penna e alternative

Un riconoscitore può trovare diversi modi per suddividere un esempio di input penna in segmenti di riconoscimento. Per questo motivo, il numero di alternative di riconoscimento può essere scaglionato, anche per un piccolo esempio di input penna.

Ad esempio, "t o g e t h e r" possono produrre i risultati seguenti:

-   "per ottenerlo" (più alternative per ogni parola)
-   "da raccogliere" (più alternative per ogni parola)
-   "tog ether" (più alternative per ogni parola)
-   "tog" (più alternative per ogni parola)
-   "insieme" (più alternative per la parola)

L'oggetto [**RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) supporta l'archiviazione efficiente di risultati di riconoscimento completi all'interno dell'oggetto [**Ink**](inkdisp-class.md) . L'oggetto **Ink** esegue il mapping delle alternative di riconoscimento ai tratti nell'oggetto **Ink** e può anche contenere altre informazioni, ad esempio la posizione della linea di base, gli indici di riga e gli intervalli di lingua.

 

 



