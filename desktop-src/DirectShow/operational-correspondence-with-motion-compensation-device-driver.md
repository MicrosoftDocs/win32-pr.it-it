---
description: Corrispondenza operativa con driver di dispositivo compensazione movimento
ms.assetid: bd92a0f4-98d9-497a-99b9-0cf432347daf
title: Corrispondenza operativa con driver di dispositivo compensazione movimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cca960ed8cbdae212bbe5e9f3b25316125a7456
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225362"
---
# <a name="operational-correspondence-with-motion-compensation-device-driver"></a>Corrispondenza operativa con driver di dispositivo compensazione movimento

Questa sezione contiene una descrizione del lato driver del dispositivo di compensazione del movimento dell'interfaccia di DirectX VA. (Riferimento: Windows 2000 DDK-driver grafica-Guida alla progettazione-3,0 DirectDraw DDI-3,12 compensazione di movimento. Vedere il DDK di Windows per la documentazione sulle strutture in grassetto.

Gli elementi seguenti si riferiscono alle voci a cui si accede tramite la struttura **DD \_ MOTIONCOMPCALLBACKS** :

1.  All'inizio dell'elaborazione pertinente, il **DdMoCompCreate** del driver di dispositivo viene usato per notificare al driver che il decodificatore software inizierà a usare un oggetto accelerazione video.
2.  I GUID ricevuti da [**IAMVideoAccelerator:: GetVideoAcceleratorGUIDs**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getvideoacceleratorguids) provengono dal **DdMoCompGetGUIDs** del driver di dispositivo.
3.  Una chiamata al pin di input downstream [**IAMVideoAccelerator:: GetUncompFormatsSupported**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getuncompformatssupported) restituisce i dati dal **DdMoCompGetFormats** del driver di dispositivo.
4.  La \_ struttura dei dati DXVA connectMode dal decodificatore [**IAMVideoAcceleratorNotify:: GetCreateVideoAcceleratorData**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getcreatevideoacceleratordata) viene passata al **DdMoCompCreate** del driver di dispositivo.
5.  I dati restituiti da [**IAMVideoAccelerator:: GetCompBufferInfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getcompbufferinfo) provengono dal **DdMoCompGetBuffInfo** del driver di dispositivo.
6.  I buffer inviati con [**IAMVideoAccelerator:: Execute**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-execute) vengono ricevuti dal **DdMoCompRender** del driver di dispositivo.
7.  L'uso di [**IAMVideoAccelerator:: QueryRenderStatus**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus) richiama il **DdMoCompQueryStatus** del driver di dispositivo. Un codice restituito di DDERR \_ WASSTILLDRAWING da DdMoCompQueryStatus verrà visualizzato dal decodificatore host come codice restituito di E \_ in sospeso da **IAMVideoAccelerator:: QueryRenderStatus**.
8.  I dati inviati a [**IAMVideoAccelerator:: BeginFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) vengono ricevuti dal **DdMoCompBeginFrame** del driver di dispositivo. Un codice restituito di E in \_ sospeso è necessario da DdMoCompBeginFrame per la visualizzazione di e in \_ sospeso dal decodificatore host in risposta a **IAMVideoAccelerator:: BeginFrame**.
9.  I dati inviati a [**IAMVideoAccelerator:: EndFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe) vengono ricevuti dal **DdMoCompEndFrame** del driver di dispositivo.
10. Al termine dell'elaborazione pertinente, il **DdMoCompDestroy** del driver di dispositivo viene utilizzato per notificare al driver che l'oggetto accelerazione video corrente non verrà più utilizzato, in modo che il driver possa eseguire le operazioni di pulizia necessarie.

 

 



