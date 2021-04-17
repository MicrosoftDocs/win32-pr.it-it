---
description: Un effetto (spesso archiviato in un file con estensione FX) dichiara lo stato della pipeline impostato da un effetto.
ms.assetid: 75b76d65-be97-41c2-8c45-4369fcfd69ce
title: Formato effetto (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5671750d7b4146ae5da8b0ba61ceae390b60a35
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401509"
---
# <a name="effect-format-direct3d-10"></a>Formato effetto (Direct3D 10)

Un effetto (spesso archiviato in un file con estensione FX) dichiara lo stato della pipeline impostato da un effetto. Lo stato dell'effetto può essere suddiviso approssimativamente in tre categorie:

-   [Variabili](d3d10-effect-variable-syntax.md), generalmente dichiarate all'inizio di un effetto.
-   [Funzioni](d3d10-effect-function-syntax.md), che implementano il codice dello shader, o vengono usate come funzioni di supporto da altre funzioni.
-   [Una tecnica](d3d10-effect-technique-syntax.md), che implementa sequenze di rendering usando uno o più passaggi di effetto. Ogni sessione imposta uno o più [gruppi di stati](d3d10-effect-states.md) e chiama funzioni shader.

![diagramma delle categorie dello stato degli effetti](images/d3d10-effect-intro.png)

Il diagramma precedente mostra le categorie dello stato dell'effetto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento a effetti](d3d10-graphics-reference-effect.md)
</dt> </dl>

 

 



