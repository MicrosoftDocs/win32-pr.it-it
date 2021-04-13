---
title: Utilizzo di C/C++-preprocessore con MIDL
description: Il compilatore MIDL non esegue la pre-elaborazione dei file di origine.
ms.assetid: 0f62d2a4-cfc3-42a7-b3a6-4e5c67c7c849
keywords:
- MIDL compilatore MIDL, C-preprocessore
- MIDL per il preprocessore C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5752bd64ee9a9b5fc26d586b5bc33c1a1fb96e83
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329564"
---
# <a name="using-cc-preprocessor-with-midl"></a>Utilizzo di C/C++-preprocessore con MIDL

Il compilatore MIDL non esegue la pre-elaborazione dei file di origine. Il compilatore MIDL usa invece un preprocessore disponibile per preparare il flusso di input per l'analisi. Per impostazione predefinita, MIDL usa il preprocessore per il compilatore Microsoft C/C++ dallo stesso ambiente di compilazione di MIDL. Se necessario, l'utente può indicare un preprocessore diverso che verrà usato da MIDL.

MIDL genera esecuzioni del preprocessore separate per i file IDL e ACF di primo livello e per ogni file importato con la direttiva di importazione MIDL. I file inclusi con la direttiva **\# include** vengono gestiti direttamente dal preprocessore.

Negli argomenti seguenti vengono descritti i vari aspetti delle interazioni del preprocessore MIDL:

-   [C-requisiti per il preprocessore MIDL](c-preprocessor-requirements-for-midl.md)
-   [Verifica delle opzioni del preprocessore](verifying-preprocessor-options.md)
-   [Salvataggio dell'output del preprocessore](saving-preprocessor-output.md)
-   [Gestione delle \# definizioni nei file IDL](dealing-with-defines-in-idl-files-2.md)

 

 




