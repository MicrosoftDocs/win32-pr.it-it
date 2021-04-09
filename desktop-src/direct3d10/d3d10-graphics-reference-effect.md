---
description: L'API Direct3D definisce diversi elementi API per semplificare la creazione e la gestione del sistema di effetti.
ms.assetid: d3b0b7a2-0820-4bb1-8b9e-c6b55a039963
title: Guida di riferimento agli effetti (grafica Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c903959096e1192555fd813a256d03fb1969fa9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966102"
---
# <a name="effect-reference-direct3d-10-graphics"></a>Guida di riferimento agli effetti (grafica Direct3D 10)

L'API Direct3D definisce diversi elementi API per semplificare la creazione e la gestione del sistema di effetti.

-   [Interfacce](d3d10-graphics-reference-effect-interfaces.md)
-   [Funzioni](d3d10-graphics-reference-effect-functions.md)
-   [Strutture](d3d10-graphics-reference-effect-structures.md)
-   [Costanti](d3d10-graphics-reference-effect-constants.md)

Il sistema di effetti incapsula le assegnazioni di stato in un effetto. Ogni effetto è una raccolta dello stato della pipeline che può essere suddivisa in assegnazioni di stato usando blocchi di stato, risorse e shader. A seconda delle dimensioni di un effetto, è possibile scegliere di implementarne una in una stringa di testo ASCII o un file di effetti (. FX). Per organizzare le informazioni in un effetto, vedere il [formato dell'effetto](d3d10-effect-format.md).

Avendo progettato un effetto, usare l'API Effect per impostare lo stato nel dispositivo durante il rendering. Inoltre, il sistema degli effetti supporta una serie di API di reflection per ottenere e impostare i dati effettivi. Per altre informazioni, vedere [Effect System Interfaces (Direct3D 10)](d3d10-graphics-programming-guide-effects-interfaces.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento a Direct3D](d3d10-graphics-reference-d3d10.md)
</dt> </dl>

 

 



