---
description: Un effetto (spesso archiviato in un file con estensione fx) dichiara lo stato della pipeline impostato da un effetto.
ms.assetid: 75b76d65-be97-41c2-8c45-4369fcfd69ce
title: Formato effetto (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0c9511304a3c24784381092017659fb1a6c593808253383443c8e9f6917c2be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852827"
---
# <a name="effect-format-direct3d-10"></a>Formato effetto (Direct3D 10)

Un effetto (spesso archiviato in un file con estensione fx) dichiara lo stato della pipeline impostato da un effetto. Lo stato dell'effetto può essere suddiviso approssimativamente in tre categorie:

-   [Variabili](d3d10-effect-variable-syntax.md), che in genere vengono dichiarate all'inizio di un effetto.
-   [Funzioni](d3d10-effect-function-syntax.md), che implementano il codice dello shader o vengono usate come funzioni helper da altre funzioni.
-   [Tecnica ,](d3d10-effect-technique-syntax.md)che implementa le sequenze di rendering usando uno o più passaggi dell'effetto. Ogni passaggio imposta uno o più [gruppi di stati e](d3d10-effect-states.md) chiama le funzioni shader.

![Diagramma delle categorie di stato dell'effetto](images/d3d10-effect-intro.png)

Il diagramma precedente mostra le categorie di stato dell'effetto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sull'effetto](d3d10-graphics-reference-effect.md)
</dt> </dl>

 

 



