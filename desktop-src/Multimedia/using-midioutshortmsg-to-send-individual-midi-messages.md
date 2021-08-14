---
title: Uso di midiOutShortMsg per inviare singoli messaggi MIDI
description: Uso di midiOutShortMsg per inviare singoli messaggi MIDI
ms.assetid: 7a8f7c6c-28ac-4aa6-9073-969fc8e59f4e
keywords:
- MIDI (Musical Instrument Digital Interface), invio di messaggi
- MIDI (Musical Instrument Digital Interface), invio di messaggi
- invio di messaggi MIDI
- Funzione MIDI (Musical Instrument Digital Interface),midiOutShortMsg
- MIDI (Musical Instrument Digital Interface),funzione midiOutShortMsg
- Funzione midiOutShortMsg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: accd4f1f7482c81acdff1c950ada8947d3b1d456438dd96092ae094ae587de42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800823"
---
# <a name="using-midioutshortmsg-to-send-individual-midi-messages"></a>Uso di midiOutShortMsg per inviare singoli messaggi MIDI

L'esempio seguente usa la [**funzione midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) per inviare un evento MIDI specificato a un determinato dispositivo di output MIDI:


```C++
UINT sendMIDIEvent(HMIDIOUT hmo, BYTE bStatus, BYTE bData1, 
    BYTE bData2) 
{ 
    union { 
        DWORD dwData; 
        BYTE bData[4]; 
    } u; 
 
    // Construct the MIDI message. 
 
    u.bData[0] = bStatus;  // MIDI status byte 
    u.bData[1] = bData1;   // first MIDI data byte 
    u.bData[2] = bData2;   // second MIDI data byte 
    u.bData[3] = 0; 
 
    // Send the message. 
    return midiOutShortMsg(hmo, u.dwData); 
} 
```



> [!Note]  
> I driver di output MIDI non sono necessari per verificare i dati prima di inviarli a una porta di output. Le applicazioni devono garantire che siano inviati solo dati validi.

 

 

 