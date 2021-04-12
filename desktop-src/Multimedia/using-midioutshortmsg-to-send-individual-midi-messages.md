---
title: Uso di midiOutShortMsg per inviare singoli messaggi MIDI
description: Uso di midiOutShortMsg per inviare singoli messaggi MIDI
ms.assetid: 7a8f7c6c-28ac-4aa6-9073-969fc8e59f4e
keywords:
- MIDI (Musical Instrument Digital Interface), invio di messaggi
- MIDI (Musical Instrument Digital Interface), invio di messaggi
- invio di messaggi MIDI
- MIDI (Musical Instrument Digital Interface), funzione midiOutShortMsg
- MIDI (Musical Instrument Digital Interface), funzione midiOutShortMsg
- midiOutShortMsg (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 905b0ce924f9aebce67f515fc0714fdc855cbe33
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472974"
---
# <a name="using-midioutshortmsg-to-send-individual-midi-messages"></a>Uso di midiOutShortMsg per inviare singoli messaggi MIDI

Nell'esempio seguente viene usata la funzione [**midiOutShortMsg**](/windows/win32/api/mmeapi/nf-mmeapi-midioutshortmsg) per inviare un evento MIDI specificato a un dispositivo di output MIDI specificato:


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
> I driver di output MIDI non sono necessari per verificare i dati prima di inviarli a una porta di output. Le applicazioni devono garantire che vengano inviati solo i dati validi.

 

 

 