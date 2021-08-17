---
description: È possibile usare un riconoscitore di movimenti personalizzato in modo indipendente o in aggiunta a GestureRecognizer. Creare il riconoscitore di movimenti personalizzato come IStylusSyncPlugin, fare in modo che crei CustomStylusData e includa il plug-in nello stesso StylusSyncPluginCollection di GestureRecognizer. In IStylusSyncPlugin combinare le notifiche dei movimenti di entrambi i riconoscitori in notifiche che devono essere utilizzate da un'applicazione.
ms.assetid: ed4e8f56-9137-47fd-a8f9-17eebfd06e97
title: Uso di un sistema di riconoscimento movimenti personalizzato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa4c58dd93bdb19f1f930be38e40f0068fa02239f09603035b572559d1f8a916
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091308"
---
# <a name="using-a-custom-gesture-recognizer"></a>Uso di un sistema di riconoscimento movimenti personalizzato

È possibile usare un sistema di riconoscimento movimenti personalizzato in modo indipendente o in aggiunta a [**GestureRecognizer.**](gesturerecognizer-class.md)

Creare il riconoscitore di movimenti personalizzato come [**IStylusSyncPlugin,**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin)fare in modo che crei [CustomStylusData](/previous-versions/ms575208(v=vs.100))e includa il plug-in nello stesso [StylusSyncPluginCollection](/previous-versions/ms824788(v=msdn.10)) di [**GestureRecognizer.**](gesturerecognizer-class.md) In **IStylusSyncPlugin** combinare le notifiche dei movimenti di entrambi i riconoscitori in notifiche che devono essere utilizzate da un'applicazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accesso e modifica dell'input dello stilo](accessing-and-manipulating-stylus-input.md)
</dt> </dl>

 

 
