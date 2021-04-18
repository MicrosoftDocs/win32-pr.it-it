---
description: Motore di rendering intelligente
ms.assetid: 279be879-9728-4fa1-bdf7-6b48485fc75f
title: Motore di rendering intelligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fa727397f21aeba754cfe41f2dc4f9c1da1c91b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304170"
---
# <a name="smart-render-engine"></a>Motore di rendering intelligente

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L'oggetto motore di rendering intelligente esegue il rendering dell'output compresso da una sequenza temporale. Per creare questo oggetto, chiamare **CoCreateInstance**. Per l'output non compresso, usare il motore di rendering di base. L'identificatore di classe è CLSID \_ SmartRenderEngine.

Il motore di rendering intelligente espone le interfacce seguenti:

-   [**IAMSetErrorLog**](iamseterrorlog.md)
-   **IObjectWithSite**
-   [**IRenderEngine**](irenderengine.md)
-   [**IRenderEngine2**](irenderengine2.md)
-   [**ISmartRenderEngine**](ismartrenderengine.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Rendering di un progetto](rendering-a-project.md)
</dt> <dt>

[Motore di rendering di base](basic-render-engine.md)
</dt> </dl>

 

 



