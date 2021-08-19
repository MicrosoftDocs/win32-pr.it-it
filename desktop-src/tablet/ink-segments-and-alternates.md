---
description: Un riconoscitore può trovare diversi modi per suddividere un campione di input penna in segmenti di riconoscimento. Per questo, il numero di alternative di riconoscimento può essere sfalsato, anche per un piccolo campione di input penna.
ms.assetid: 7ecffe3f-cbe4-4e65-a1cc-9b08534b26c9
title: Segmenti e alternative di input penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 702c2da4984afd22490827acdf65962abc789d7ad9f0ddab3e602bc688ac6542
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883991"
---
# <a name="ink-segments-and-alternates"></a>Segmenti e alternative di input penna

Un riconoscitore può trovare diversi modi per suddividere un campione di input penna in segmenti di riconoscimento. Per questo, il numero di alternative di riconoscimento può essere sfalsato, anche per un piccolo campione di input penna.

Ad esempio, "t o g e t h e r" può produrre i risultati seguenti:

-   "per ottenerla" (più alternative per ogni parola)
-   "to gather" (più alternative per ogni parola)
-   "tog ether" (più alternative per ogni parola)
-   "tog at her" (più alternative per ogni parola)
-   "together" (più alternative per la parola)

[**L'oggetto RecognitionResult**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionresult) supporta un'archiviazione efficiente dei risultati del riconoscimento completo all'interno [**dell'oggetto**](inkdisp-class.md) Ink. **L'oggetto Ink** esegue il mapping delle alternative di riconoscimento ai tratti nell'oggetto **Ink** e può contenere anche altre informazioni, ad esempio la posizione della linea di base, gli indici di linea e gli intervalli di lingua.

 

 



