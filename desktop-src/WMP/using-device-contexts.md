---
title: Uso dei contesti di dispositivo
description: Uso dei contesti di dispositivo
ms.assetid: 2e8de313-6218-4401-a578-73140e7fdae1
keywords:
- Visualizzazioni, contesto di dispositivo
- Visualizzazioni personalizzate, contesto di dispositivo
- Visualizzazioni, funzione render
- Visualizzazioni personalizzate, funzione render
- Funzione render, contesto di dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08c315d5004565644750f4adcd099fc165e81575
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330535"
---
# <a name="using-device-contexts"></a>Uso dei contesti di dispositivo

Il contesto di dispositivo è un handle standard per un contesto di dispositivo. Questa operazione è necessaria per molte funzioni di disegno, in modo che Microsoft Windows conosca la finestra in cui disegnare. Per creare un rettangolo, ad esempio, è necessario specificare il contesto di dispositivo.


```C++
HDC hdc;
::Rectangle( hdc, 1, 1, 100, 100 );

```



Il contesto di dispositivo viene specificato da Windows Media Player tramite la funzione **Render** . Se il plug-in viene eseguito tramite una finestra, sarà necessario usare il contesto di dispositivo di tale finestra. Usare questo contesto di dispositivo per qualsiasi strumento di disegno che richiede un contesto di dispositivo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Implementazione di rendering**](implementing-render.md)
</dt> </dl>

 

 




