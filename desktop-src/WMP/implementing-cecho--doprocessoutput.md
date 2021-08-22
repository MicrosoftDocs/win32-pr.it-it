---
title: Implementazione di CEcho DoProcessOutput
description: Implementazione di CEcho DoProcessOutput
ms.assetid: afd91022-4e2d-46a2-a0f4-cd2b558536d6
keywords:
- Windows Media Player plug-in, metodo DoProcessOutput di esempio Echo
- plug-in, metodo DoProcessOutput di esempio Echo
- plug-in di elaborazione del segnale digitale, metodo DoProcessOutput di esempio Echo
- Plug-in DSP, metodo DoProcessOutput di esempio Echo
- Esempio di plug-in Echo DSP,metodo DoProcessOutput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07054950cabadbc835c9904d48cdb4e6ddf5f05c0822c997558381958a9857d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135644"
---
# <a name="implementing-cechodoprocessoutput"></a>Implementazione di CEcho::D oProcessOutput

Il **metodo DoProcessOutput** esegue l'elaborazione del segnale digitale. Questo è il metodo che apporta le modifiche ai dati forniti da Windows Media Player. Sono i risultati di questo metodo che si ascolteranno come effetto echo al termine del plug-in di esempio Echo.

Per questo esempio, il plug-in eelaborare solo audio a 8 o 16 bit. È necessario apportare alcune modifiche al codice di esempio della procedura guidata plug-in per rimuovere le sezioni che elaborano audio con una maggiore profondità di bit. È tuttavia opportuno studiare queste sezioni perché è possibile decidere di aggiungere un'implementazione echo personalizzata per tali formati.

Le sezioni seguenti illustrano in dettaglio le modifiche da apportare al codice:

-   [Rimozione del codice da elaborare maggiore di 16 bit](removing-the-code-to-process-greater-than-16-bits.md)
-   [Elaborazione dei dati audio](processing-the-audio-data.md)
-   [Variabili per eseguire l'elaborazione](variables-to-perform-processing.md)
-   [Creazione dell'effetto Echo](creating-the-echo-effect.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Esempio echo**](the-echo-sample.md)
</dt> </dl>

 

 




