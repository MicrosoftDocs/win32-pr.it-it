---
title: Uso del preprocessore C/C++con MIDL
description: Il compilatore MIDL non pre-elabora i file di origine.
ms.assetid: 0f62d2a4-cfc3-42a7-b3a6-4e5c67c7c849
keywords:
- MIDL del compilatore MIDL, preprocessore C
- MIDL del preprocessore C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dac3952a342b101f0366d2bce8810426e758c4aa5b32fa267e685bc6d658f034
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118382795"
---
# <a name="using-cc-preprocessor-with-midl"></a>Uso del preprocessore C/C++con MIDL

Il compilatore MIDL non pre-elabora i file di origine. Il compilatore MIDL usa invece un preprocessore disponibile per preparare il flusso di input per l'analisi. Per impostazione predefinita, MIDL usa il preprocessore per il compilatore Microsoft C/C++ dallo stesso ambiente di compilazione di MIDL. L'utente può indicare un preprocessore diverso da usare da MIDL, se necessario.

MIDL genera esecuzioni del preprocessore separate per i file IDL e ACF di primo livello e per ogni file importato con la direttiva di importazione MIDL. I file inclusi nella **\# direttiva include** vengono gestiti direttamente dal preprocessore.

Gli argomenti seguenti descrivono vari aspetti delle interazioni del preprocessore MIDL:

-   [Requisiti del preprocessore C per MIDL](c-preprocessor-requirements-for-midl.md)
-   [Verifica delle opzioni del preprocessore](verifying-preprocessor-options.md)
-   [Salvataggio dell'output del preprocessore](saving-preprocessor-output.md)
-   [Gestione \# delle definisce nei file IDL](dealing-with-defines-in-idl-files-2.md)

 

 




