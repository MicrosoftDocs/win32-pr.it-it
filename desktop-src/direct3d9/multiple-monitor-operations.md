---
description: "Quando un dispositivo viene reimpostato correttamente (IDirect3DDevice9:: Reset) o creato (IDirect3D9:: CreateDevice) nelle operazioni a schermo intero, l'oggetto Direct3D che ha creato il dispositivo viene contrassegnato come proprietario di tutte le schede nel sistema."
ms.assetid: df3b6ed7-830b-4635-9295-fff05cc35891
title: Operazioni di Multiple-Monitor (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04427db6c91ff85706040589a89f6fdcfb3761e3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304068"
---
# <a name="multiple-monitor-operations-direct3d-9"></a>Operazioni di Multiple-Monitor (Direct3D 9)

Quando un dispositivo viene reimpostato correttamente ([**IDirect3DDevice9:: Reset**](/windows/desktop/api)) o creato ([**IDirect3D9:: CreateDevice**](/windows/desktop/api)) nelle operazioni a schermo intero, l'oggetto Direct3D che ha creato il dispositivo viene contrassegnato come proprietario di tutte le schede nel sistema. Questo stato è noto come modalità esclusiva e l'oggetto Direct3D è proprietario della modalità esclusiva. Modalità esclusiva significa che i dispositivi creati da un altro oggetto Direct3D non possono presupporre operazioni a schermo intero né allocare memoria video. Inoltre, quando un oggetto Direct3D presuppone la modalità esclusiva, tutti i dispositivi diversi da quello a schermo intero vengono posizionati nello stato perso. Per informazioni dettagliate, vedere [dispositivi persi (Direct3D 9)](lost-devices.md).

Insieme alla modalità esclusiva, l'oggetto Direct3D viene informato della finestra messa a fuoco che verrà usata dal dispositivo. La modalità esclusiva viene rilasciata quando il dispositivo finale a schermo intero di proprietà dell'oggetto Direct3D viene reimpostato sulla modalità finestra o eliminato definitivamente.

I dispositivi possono essere divisi in due categorie quando un oggetto Direct3D è proprietario della modalità esclusiva. La prima categoria di dispositivi presenta le caratteristiche seguenti.

-   Vengono creati dallo stesso oggetto Direct3D che ha creato il dispositivo a schermo intero.
-   Hanno la stessa finestra di messa a fuoco del dispositivo a schermo intero.
-   Rappresentano un adattatore diverso da qualsiasi dispositivo a schermo intero.

I dispositivi in questa categoria non sono soggetti ad alcuna restrizione relativa alla possibilità di reimpostarli o crearli e non vengono inseriti nello stato perso. I dispositivi in questa categoria possono anche essere inseriti in modalità schermo intero.

Dispositivi che non rientrino nella prima categoria: i dispositivi creati da un altro oggetto Direct3D, creati con una finestra di stato attivo diversa e creati per un adapter con un dispositivo che è già a schermo intero, non possono essere reimpostati e rimangono nello stato perduto fino a quando non viene persa la modalità esclusiva. Di conseguenza, un'applicazione con più monitor può collocare più dispositivi in modalità schermo intero, ma solo se tutti questi dispositivi sono per adattatori diversi, sono stati creati dallo stesso oggetto Direct3D e condividono la stessa finestra di stato attivo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Presentazione di una scena](presenting-a-scene.md)
</dt> </dl>

 

 



