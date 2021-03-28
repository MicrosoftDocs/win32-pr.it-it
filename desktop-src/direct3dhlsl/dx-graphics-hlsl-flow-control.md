---
title: Controllo di flusso
description: La maggior parte dell'hardware è progettata per eseguire il codice dello shader riga per riga, eseguendo ogni istruzione HLSL una sola volta.
ms.assetid: 94f22e39-8e71-424b-8ca1-bafc843f843f
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 70bb7706e520818c86286947acfba6cae0759b4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329255"
---
# <a name="flow-control"></a>Controllo di flusso

La maggior parte dell'hardware è progettata per eseguire il codice dello shader riga per riga, eseguendo ogni istruzione HLSL una sola volta. Un'istruzione di controllo di flusso determina in fase di esecuzione il blocco di istruzioni HLSL da eseguire successivamente. Usando un'istruzione di controllo del flusso, uno shader può scorrere un set di istruzioni o passare a un'istruzione diversa da quella nella riga successiva. Alcune istruzioni di controllo del flusso supportano il controllo statico specificato in fase di compilazione. altri offrono un controllo predicato che è una decisione per componente effettuata in fase di esecuzione e altri ancora supportano il controllo dinamico che è una decisione presa in fase di esecuzione in base al contenuto di una variabile.

HLSL supporta le seguenti istruzioni di controllo del flusso.

-   [break](dx-graphics-hlsl-break.md)
-   [continuare](dx-graphics-hlsl-continue.md)
-   [rimuovere](dx-graphics-hlsl-discard.md)
-   [do](dx-graphics-hlsl-do.md)
-   [for](dx-graphics-hlsl-for.md)
-   [if](dx-graphics-hlsl-if.md)
-   [switch](dx-graphics-hlsl-switch.md)
-   [mentre](dx-graphics-hlsl-while.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sintassi del linguaggio (DirectX HLSL)](dx-graphics-hlsl-language-syntax.md)
</dt> </dl>

 

 




