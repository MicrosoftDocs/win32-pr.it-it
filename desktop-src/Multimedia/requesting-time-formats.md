---
title: Formati di ora richieste
description: Formati di ora richieste
ms.assetid: 3492dfe3-ed54-405a-aa4f-b17abbd1e07f
keywords:
- MIDI (Musical Instrument Digital Interface), formati di ora
- MIDI (Musical Instrument Digital Interface), formati di ora
- Servizi MIDI, formati di ora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf191c857c45896c916ace4656d33bd3dd558f04
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724807"
---
# <a name="requesting-time-formats"></a>Formati di ora richieste

Windows utilizza la struttura [**MMTIME**](/previous-versions//dd757347(v=vs.85)) per rappresentare l'ora in uno o più formati diversi, tra cui i formati di millisecondi, Samples, SMPTE e Midi song pointer. Il membro **wType** specifica il formato dell'ora.

La funzione [**midiStreamPosition**](/windows/win32/api/mmeapi/nf-mmeapi-midistreamposition) usa la struttura **MMTIME** . Prima di chiamare questa funzione, è necessario impostare il membro **wType** per indicare il formato di tempo richiesto. Per verificare se il formato ora richiesto è supportato, controllare **wType** dopo la chiamata. Se il formato tempo richiesto non è supportato, l'ora viene specificata in un formato di ora alternativo selezionato dal driver di dispositivo e il membro **wType** viene modificato per indicare il formato di ora selezionato.

Per ulteriori informazioni sulla struttura **MMTIME** , vedere la pagina relativa ai [timer multimediali](multimedia-timers.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Servizi MIDI](midi-services.md)
</dt> </dl>

 

 