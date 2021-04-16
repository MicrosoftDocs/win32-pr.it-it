---
description: Motore di rendering di base
ms.assetid: 0a4fcf2a-dbad-4211-9a85-7741c8dfc95e
title: Motore di rendering di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb9b51240b43c58de99b7d6fe1f7ad61f754c7ed
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522218"
---
# <a name="basic-render-engine"></a>Motore di rendering di base

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L'oggetto motore di rendering di base esegue il rendering dell'output non compresso da una sequenza temporale. Per creare questo oggetto, chiamare **CoCreateInstance**. Per l'output compresso, usare il motore di rendering intelligente. L'identificatore di classe è CLSID \_ RenderEngine.

Il motore di rendering di base espone le interfacce seguenti:

-   [**IAMSetErrorLog**](iamseterrorlog.md)
-   IObjectWithSite
-   [**IRenderEngine**](irenderengine.md)
-   [**IRenderEngine2**](irenderengine2.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Rendering di un progetto](rendering-a-project.md)
</dt> <dt>

[Motore di rendering intelligente](smart-render-engine.md)
</dt> </dl>

 

 



