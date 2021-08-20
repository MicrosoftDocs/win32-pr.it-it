---
title: Gestione degli errori con funzioni audio
description: Gestione degli errori con funzioni audio
ms.assetid: 76f132f1-61dc-4bfc-9e4a-7c841a487794
keywords:
- audio multimediale, errori audio waveform
- audio, errori audio waveform
- audio multimediale, errori audio ausiliari
- audio, errori audio ausiliari
- audio waveform, errori
- audio ausiliario, errori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dbb332ed0be06a829c169bdf333f3f4ce73a6e9dff81b22949174216dd4017d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141084"
---
# <a name="handling-errors-with-audio-functions"></a>Gestione degli errori con funzioni audio

Le funzioni waveform-audio e auxiliary-audio restituiscono un valore diverso da zero quando si verifica un errore. Windows fornisce funzioni che convertono questi valori di errore in descrizioni testuali degli errori. L'applicazione deve comunque esaminare i valori di errore per determinare come procedere, ma è possibile usare descrizioni testuali degli errori nelle finestre di dialogo che descrivono gli errori per gli utenti.

È possibile usare le funzioni seguenti per recuperare descrizioni testuali dei valori di errore audio:



| Funzione                                           | Descrizione                                                                 |
|----------------------------------------------------|-----------------------------------------------------------------------------|
| [**waveInGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-waveingeterrortext)   | Recupera una descrizione testuale di un errore di input audio-forma d'onda specificato.  |
| [**waveOutGetErrorText**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgeterrortext) | Recupera una descrizione testuale di un errore di output audio-forma d'onda specificato. |



 

Le uniche funzioni audio che non restituiscono valori di errore sono [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs), [**waveInGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveingetnumdevs)e [**waveOutGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutgetnumdevs). Queste funzioni restituiscono zero se non sono presenti dispositivi in un sistema o se si verificano errori.

 

 