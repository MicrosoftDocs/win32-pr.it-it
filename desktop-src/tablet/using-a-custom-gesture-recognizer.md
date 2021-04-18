---
description: È possibile utilizzare un riconoscimento di movimento personalizzato in modo indipendente o in aggiunta all'oggetto GestureRecognizer. creare il riconoscitore di movimenti personalizzato come IStylusSyncPlugin, creare CustomStylusData e includere il plug-in nello stesso StylusSyncPluginCollection dell'oggetto GestureRecognizer. In IStylusSyncPlugin, combinare notifiche di movimento da entrambi i riconoscitori in notifiche che devono essere utilizzate da un'applicazione.
ms.assetid: ed4e8f56-9137-47fd-a8f9-17eebfd06e97
title: Uso di un riconoscimento di movimenti personalizzato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 376f567680cfe7e862f280d1b8e8dc35a2017316
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306725"
---
# <a name="using-a-custom-gesture-recognizer"></a>Uso di un riconoscimento di movimenti personalizzato

È possibile utilizzare un riconoscimento di movimento personalizzato in modo indipendente o in aggiunta all'oggetto [**GestureRecognizer**](gesturerecognizer-class.md).

Creare il riconoscitore di movimenti personalizzato come [**IStylusSyncPlugin**](/windows/win32/api/rtscom/nn-rtscom-istylussyncplugin), fare in modo che crei [CustomStylusData](/previous-versions/ms575208(v=vs.100))e includa il plug-in nello stesso [StylusSyncPluginCollection](/previous-versions/ms824788(v=msdn.10)) dell'oggetto [**GestureRecognizer**](gesturerecognizer-class.md). In **IStylusSyncPlugin**, combinare notifiche di movimento da entrambi i riconoscitori in notifiche che devono essere utilizzate da un'applicazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Accesso e modifica dell'input dello stilo](accessing-and-manipulating-stylus-input.md)
</dt> </dl>

 

 
