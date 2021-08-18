---
description: Motore di rendering di base
ms.assetid: 0a4fcf2a-dbad-4211-9a85-7741c8dfc95e
title: Motore di rendering di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8a3e04e1ad32c163db93794e075ff7933f041c3270ab8412cbd5b5a68b4a763
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118955574"
---
# <a name="basic-render-engine"></a>Motore di rendering di base

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

L'oggetto Basic Render Engine esegue il rendering dell'output non compresso da una sequenza temporale. Per creare questo oggetto, chiamare **CoCreateInstance**. Per l'output compresso, usare il motore di rendering intelligente. L'identificatore di classe è CLSID \_ RenderEngine.

Il motore di rendering di base espone le interfacce seguenti:

-   [**IAMSetErrorLog**](iamseterrorlog.md)
-   IObjectWithSite
-   [**IRenderEngine**](irenderengine.md)
-   [**IRenderEngine2**](irenderengine2.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Rendering di un Project](rendering-a-project.md)
</dt> <dt>

[Motore di rendering intelligente](smart-render-engine.md)
</dt> </dl>

 

 



