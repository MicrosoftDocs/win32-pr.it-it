---
title: Controllo di flusso
description: La maggior parte dell'hardware è progettata per eseguire codice shader riga per riga, eseguendo ogni istruzione HLSL una sola volta.
ms.assetid: 94f22e39-8e71-424b-8ca1-bafc843f843f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4aebaf63613aeb3a1d14607971db16602745883ab6b7b9db4723dfa2367f9bd2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120285"
---
# <a name="flow-control"></a>Controllo di flusso

La maggior parte dell'hardware è progettata per eseguire codice shader riga per riga, eseguendo ogni istruzione HLSL una sola volta. Un'istruzione di controllo del flusso determina in fase di esecuzione quale blocco di istruzioni HLSL eseguire successivamente. Usando un'istruzione di controllo di flusso, uno shader può scorrere in ciclo un set di istruzioni o passare (ramo) a un'istruzione diversa da quella nella riga successiva. Alcune istruzioni di controllo di flusso supportano il controllo statico specificato in fase di compilazione. altri offrono un controllo predicato che è una decisione per componente presa in fase di esecuzione e altri ancora supportano il controllo dinamico che è una decisione presa in fase di esecuzione in base al contenuto di una variabile.

HLSL supporta le istruzioni di controllo di flusso seguenti.

-   [break](dx-graphics-hlsl-break.md)
-   [Continuare](dx-graphics-hlsl-continue.md)
-   [Scartare](dx-graphics-hlsl-discard.md)
-   [do](dx-graphics-hlsl-do.md)
-   [for](dx-graphics-hlsl-for.md)
-   [if](dx-graphics-hlsl-if.md)
-   [switch](dx-graphics-hlsl-switch.md)
-   [Mentre](dx-graphics-hlsl-while.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sintassi del linguaggio (DirectX HLSL)](dx-graphics-hlsl-language-syntax.md)
</dt> </dl>

 

 




