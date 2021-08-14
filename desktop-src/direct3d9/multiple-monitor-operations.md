---
description: Quando un dispositivo viene reimpostato correttamente (IDirect3DDevice9::Reset) o creato (IDirect3D9::CreateDevice) nelle operazioni a schermo intero, l'oggetto Direct3D che ha creato il dispositivo viene contrassegnato come proprietario di tutte le schede nel sistema.
ms.assetid: df3b6ed7-830b-4635-9295-fff05cc35891
title: Multiple-Monitor operazioni (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da4f175c136cd432223eeaaf32cf44bfbb08e724b54b8afe1dbb9717c2d79a4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728211"
---
# <a name="multiple-monitor-operations-direct3d-9"></a>Multiple-Monitor operazioni (Direct3D 9)

Quando un dispositivo viene reimpostato correttamente ([**IDirect3DDevice9::Reset**](/windows/desktop/api)) o creato ([**IDirect3D9::CreateDevice**](/windows/desktop/api)) nelle operazioni a schermo intero, l'oggetto Direct3D che ha creato il dispositivo viene contrassegnato come proprietario di tutte le schede nel sistema. Questo stato è noto come modalità esclusiva e l'oggetto Direct3D è proprietario della modalità esclusiva. La modalità esclusiva indica che i dispositivi creati da qualsiasi altro oggetto Direct3D non possono presupporre operazioni a schermo intero né allocare memoria video. Inoltre, quando un oggetto Direct3D assume la modalità esclusiva, tutti i dispositivi diversi da quello che è stato visualizzato a schermo intero vengono posizionati in stato perso. Per informazioni dettagliate, [vedere Dispositivi persi (Direct3D 9).](lost-devices.md)

Insieme alla modalità esclusiva, l'oggetto Direct3D viene informato della finestra attiva che verrà utilizzata dal dispositivo. La modalità esclusiva viene rilasciata quando il dispositivo a schermo intero finale di proprietà dell'oggetto Direct3D viene reimpostato sulla modalità finestra o eliminato.

I dispositivi possono essere suddivisi in due categorie quando un oggetto Direct3D è proprietario della modalità esclusiva. La prima categoria di dispositivi ha le caratteristiche seguenti.

-   Vengono creati dallo stesso oggetto Direct3D che ha creato il dispositivo a schermo intero.
-   Hanno la stessa finestra di attivazione del dispositivo a schermo intero.
-   Rappresentano un adattatore diverso da qualsiasi dispositivo a schermo intero.

I dispositivi in questa categoria non hanno restrizioni relative alla possibilità di reimpostazione o creazione e non vengono inseriti in uno stato perso. I dispositivi in questa categoria possono anche essere inseriti in modalità schermo intero.

I dispositivi che non rientrano nella prima categoria, i dispositivi creati da un altro oggetto Direct3D, creati con una finestra di attivazione diversa e creati per un adattatore con un dispositivo già a schermo intero, non possono essere reimpostati e rimangono in stato perso fino a quando non viene persa la modalità esclusiva. Di conseguenza, un'applicazione con più monitor può impostare più dispositivi in modalità schermo intero, ma solo se tutti questi dispositivi sono per schede diverse, sono stati creati dallo stesso oggetto Direct3D e condividono la stessa finestra attiva.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Presentazione di una scena](presenting-a-scene.md)
</dt> </dl>

 

 



