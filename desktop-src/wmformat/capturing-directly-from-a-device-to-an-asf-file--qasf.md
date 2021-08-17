---
title: Acquisizione diretta da un dispositivo a un file ASF (QASF)
description: Acquisizione diretta da un dispositivo a un file ASF (QASF)
ms.assetid: 684a11e3-d507-4219-bc0b-6dfe5e85dad1
keywords:
- Windows Media Format SDK, acquisizione da dispositivi a file ASF (QASF)
- Windows Media Format SDK,DirectShow
- Advanced Systems Format (ASF), acquisizione da dispositivi (QASF)
- ASF (Advanced Systems Format), acquisizione da dispositivi (QASF)
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- DirectShow,acquisizione da dispositivi a file ASF (QASF)
- Windows Media Format SDK, QASF
- Advanced Systems Format (ASF), QASF
- ASF (Advanced Systems Format), QASF
- DirectShow,QASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 570e773e39b4c2d76bd95f0a4ac90269be295585ef91e6e50f653b121cbc8d9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118705091"
---
# <a name="capturing-directly-from-a-device-to-an-asf-file-qasf"></a>Acquisizione diretta da un dispositivo a un file ASF (QASF)

Quando si acquisiscono audio o video direttamente in un file ASF, il grafico dei filtri è simile al diagramma seguente, a seconda del tipo di dispositivo di acquisizione usato.

![Grafico di acquisizione da webcam a wmv](images/asf-webcam.png)

La documentazione di DirectShow SDK descrive in dettaglio come creare grafici di acquisizione, ma è importante ricordare quando si creano grafici di acquisizione usando WM ASF Writer: WM ASF Writer non verrà eseguito a meno che non siano connessi tutti i relativi pin. Se si configura WM ASF Writer con il profilo di sistema predefinito (scelta non consigliata) o qualsiasi profilo con flussi audio e video, verrà creato un pin di input per ogni flusso e ognuno di questi pin deve essere connesso. Se ad esempio non si intende acquisire l'audio, assicurarsi di configurare il filtro con un profilo solo video in modo che non sia stato creato alcun pin audio.

 

 




