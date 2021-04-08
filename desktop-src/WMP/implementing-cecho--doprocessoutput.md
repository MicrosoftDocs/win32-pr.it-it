---
title: Implementazione di CEcho DoProcessOutput
description: Implementazione di CEcho DoProcessOutput
ms.assetid: afd91022-4e2d-46a2-a0f4-cd2b558536d6
keywords:
- Plug-in di Windows Media Player, metodo DoProcessOutput di esempio Echo
- plug-in, esempio Echo metodo DoProcessOutput
- plug-in di elaborazione dei segnali digitali, metodo DoProcessOutput di esempio Echo
- Plug-in DSP, metodo DoProcessOutput di esempio Echo
- Esempio di plug-in Echo DSP, metodo DoProcessOutput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ff40246a6a0ccda2b3f17b12924c44cb79fa4d9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045348"
---
# <a name="implementing-cechodoprocessoutput"></a>Implementazione di CEcho::D oProcessOutput

Il metodo **DoProcessOutput** esegue l'elaborazione del segnale digitale. Si tratta del metodo che apporta le modifiche ai dati forniti da Windows Media Player. Si tratta del risultato di questo metodo che verrà visualizzato come effetto Echo quando il plug-in echo sample è completo.

Per questo esempio, il plug-in elaborerà solo audio a 8 bit o a 16 bit. È necessario apportare alcune modifiche al codice di esempio della procedura guidata plug-in per rimuovere le sezioni che elaborano un audio di profondità di bit superiore. È tuttavia utile studiare queste sezioni, perché è possibile decidere di aggiungere un'implementazione Echo personalizzata per tali formati.

Le sezioni seguenti illustrano in dettaglio le modifiche che è necessario apportare al codice:

-   [Rimozione del codice per elaborare più di 16 bit](removing-the-code-to-process-greater-than-16-bits.md)
-   [Elaborazione dei dati audio](processing-the-audio-data.md)
-   [Variabili per l'esecuzione dell'elaborazione](variables-to-perform-processing.md)
-   [Creazione dell'effetto Echo](creating-the-echo-effect.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Esempio Echo**](the-echo-sample.md)
</dt> </dl>

 

 




