---
title: Modifica della pagina delle proprietà di esempio Echo
description: Modifica della pagina delle proprietà di esempio Echo
ms.assetid: a7ebf7d7-1f70-421f-862f-bc60655bb242
keywords:
- Plug-in di Windows Media Player, pagine delle proprietà di esempio Echo
- plug-in, pagine delle proprietà di esempio Echo
- plug-in di elaborazione dei segnali digitali, pagine delle proprietà di esempio Echo
- Plug-in DSP, pagine delle proprietà di esempio Echo
- Esempio di plug-in Echo DSP, pagine delle proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f16c623f833d8d9c107c00e96fed92bab28e8b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395735"
---
# <a name="modifying-the-echo-sample-property-page"></a>Modifica della pagina delle proprietà di esempio Echo

L'implementazione predefinita della pagina delle proprietà fornita dall'esempio di plug-in della procedura guidata per il plug-in di Windows Media Player contiene un singolo controllo casella di modifica che riceve il fattore di scala dall'utente. È necessario modificare la pagina delle proprietà per ricevere i due valori di proprietà usati dall'esempio Echo.

Per una panoramica delle pagine delle proprietà del plug-in DSP, vedere [implementazione di un plug-in DSP audio](implementing-an-audio-dsp-plug-in.md).

Le sezioni seguenti illustrano il processo di modifica della pagina delle proprietà di esempio:

-   [Modifica della risorsa della finestra di dialogo Echo](modifying-the-echo-dialog-resource.md)
-   [Aggiunta e modifica degli eventi](adding-and-modifying-the-events.md)
-   [Modo in cui l'esempio Echo rende permanente i dati](how-the-echo-sample-persists-data.md)
-   [Implementazione di CEchoPropPage:: OnInitDialog](implementing-cechoproppage--oninitdialog.md)
-   [Implementazione di CEchoPropPage:: Apply](implementing-cechoproppage--apply.md)
-   [Implementazione di CEcho:: FinalConstruct](implementing-cecho--finalconstruct.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Esempio Echo**](the-echo-sample.md)
</dt> </dl>

 

 




