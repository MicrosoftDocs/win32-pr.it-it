---
description: 'Il concetto di modalità a schermo intero esclusivo viene mantenuto in Direct3D 9, ma viene mantenuto completamente implicito nelle chiamate al metodo IDirect3D9:: CreateDevice e IDirect3DDevice9:: Reset.'
ms.assetid: c3503d62-d9f9-4eec-8af3-ebcbfe7064d4
title: Utilizzo di più sistemi di monitoraggio (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 184a11f06d2296100a0b546e29770f44977b4de3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303915"
---
# <a name="working-with-multiple-monitor-systems-direct3d-9"></a>Utilizzo di più sistemi di monitoraggio (Direct3D 9)

Il concetto di modalità a schermo intero esclusivo viene mantenuto in Direct3D 9, ma viene mantenuto completamente implicito nelle chiamate al metodo [**IDirect3D9:: CreateDevice**](/windows/desktop/api) e [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) . Ogni volta che un dispositivo viene reimpostato o creato in un'operazione a schermo intero, l'oggetto Direct3D che ha creato il dispositivo viene contrassegnato come proprietario di tutte le schede nel sistema. Questo stato è noto come modalità esclusiva e a questo punto l'oggetto Direct3D è proprietario della modalità esclusiva. La modalità esclusiva indica che i dispositivi creati da un altro oggetto Direct3D9 non possono presupporre operazioni a schermo intero né allocare memoria video. Inoltre, quando un oggetto Direct3D9 presuppone la modalità esclusiva, tutti i dispositivi diversi dal dispositivo che è stato a schermo intero vengono posizionati nello stato perso. Per informazioni su come gestire i dispositivi smarriti, vedere [dispositivi persi (Direct3D 9)](lost-devices.md).

Insieme alla modalità esclusiva, l'oggetto Direct3D9 viene informato della finestra messa a fuoco per l'uso da parte del dispositivo. La modalità esclusiva viene rilasciata quando l'ultimo dispositivo a schermo intero di proprietà dell'oggetto Direct3D9 viene reimpostato su modalità finestra o eliminato definitivamente.

I dispositivi possono essere divisi in due categorie quando un oggetto Direct3D9 è proprietario della modalità esclusiva. La prima categoria di dispositivi sono quelli creati dallo stesso oggetto Direct3D9 che ha creato il dispositivo che è già a schermo intero, avere la stessa finestra di messa a fuoco del dispositivo già a schermo intero e rappresentare una scheda diversa da qualsiasi dispositivo a schermo intero. I dispositivi in questa categoria non hanno alcuna restrizione relativa alla possibilità di reimpostarli o crearli e non vengono inseriti nello stato perso. I dispositivi in questa categoria possono anche essere posizionati in modalità schermo intero.

I dispositivi non presenti in questa categoria, ovvero quelli creati da un oggetto Direct3D9 diverso o con una finestra di stato attivo diversa, oppure per alcuni adapter con un dispositivo già a schermo intero non possono essere reimpostati e rimangono nello stato perduto fino a quando non viene persa la modalità esclusiva.

L'implicazione pratica è che un'applicazione con più monitor può collocare più dispositivi in modalità schermo intero, ma solo se tutti questi dispositivi sono per adattatori diversi, sono stati creati dallo stesso oggetto Direct3D9 e condividono la stessa finestra di stato attivo.

Quando si crea un nuovo dispositivo usando lo stesso oggetto [**IDirect3D9**](/windows/desktop/api) e la stessa finestra di messa a fuoco, il dispositivo originale perderà le sue superfici. Per poter usare l'applicazione, sarà necessario chiamare [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) sul primo dispositivo. Ad esempio, per creare due dispositivi, eseguire le operazioni seguenti:

1.  Creazione del dispositivo 1
2.  Creazione del dispositivo 2
3.  Reimposta dispositivo 1

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Suggerimenti per la programmazione](programming-tips.md)
</dt> </dl>

 

 
