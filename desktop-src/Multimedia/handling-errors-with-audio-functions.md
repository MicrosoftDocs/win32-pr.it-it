---
title: Gestione degli errori con funzioni audio
description: Gestione degli errori con funzioni audio
ms.assetid: 76f132f1-61dc-4bfc-9e4a-7c841a487794
keywords:
- audio multimediale, errori audio della forma d'onda
- audio, errori audio della forma d'onda
- audio multimediale, errori audio ausiliari
- audio, errori audio ausiliari
- audio Waveform, errori
- audio ausiliario, errori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfcc803ae741635b3b29fb9909f530fe041e477a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337007"
---
# <a name="handling-errors-with-audio-functions"></a>Gestione degli errori con funzioni audio

Le funzioni Waveform-Audio e ausiliario-audio restituiscono un valore diverso da zero quando si verifica un errore. Windows fornisce funzioni che convertono questi valori di errore in descrizioni testuali degli errori. L'applicazione deve comunque esaminare i valori di errore per determinare il modo in cui procedere, ma le descrizioni testuali degli errori possono essere utilizzate nelle finestre di dialogo che descrivono gli errori agli utenti.

È possibile utilizzare le funzioni seguenti per recuperare le descrizioni testuali dei valori di errore audio:



| Funzione                                           | Descrizione                                                                 |
|----------------------------------------------------|-----------------------------------------------------------------------------|
| [**waveInGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-waveingeterrortext)   | Recupera una descrizione testuale di un errore di input audio e di forma d'onda specificato.  |
| [**waveOutGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgeterrortext) | Recupera una descrizione testuale di un errore di output della forma d'onda-audio specificato. |



 

Le uniche funzioni audio che non restituiscono valori di errore sono [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs), [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)e [**waveOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs). Queste funzioni restituiscono zero se non sono presenti dispositivi in un sistema o se si verificano errori.

 

 