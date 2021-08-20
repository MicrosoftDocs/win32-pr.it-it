---
title: Supporto dell'input vocale
description: Supporto dell'input vocale
ms.assetid: 4702b941-fcc9-4d00-aba2-eca624b6d417
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd777f5dca0df91a4660249b0cdda380f2f20c37ba5c1c38a04264bb871ab3bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118746252"
---
# <a name="speech-input-support"></a>Supporto dell'input vocale

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Oltre a supportare l'interazione con mouse e tastiera, Microsoft Agent include il supporto diretto per l'input vocale. Poiché il supporto di Microsoft Agent per l'input vocale è basato su Microsoft SAPI (Speech Application Programming Interface), è possibile usare Microsoft Agent con il comando di riconoscimento vocale e i motori di controllo che includono il supporto richiesto da SAPI. Per altre informazioni sui requisiti del motore di riconoscimento vocale, vedere [Requisiti di supporto del motore di riconoscimento vocale](requirements-for-speech-recognition-engines.md).

Microsoft offre un motore di riconoscimento vocale di comando e controllo che è possibile usare con Microsoft Agent. Per altre informazioni, vedere [Selezione del motore di riconoscimento vocale](speech-engine-selection.md).

L'utente può avviare l'input vocale premendo e tenendo premuto il tasto di scelta rapida di ascolto push-to-talk. In questa modalità di ascolto, se il motore di riconoscimento vocale riceve l'inizio dell'input parlato, mantiene aperto il canale audio fino a quando non rileva la fine dell'espressione. Tuttavia, quando non riceve l'input, non blocca l'output audio. Ciò consente all'utente di eseguire più comandi vocali tenendo premuto il tasto e il carattere può rispondere quando l'utente non parla.

La modalità di ascolto si timeout quando l'utente rilascia la chiave di ascolto. L'utente può modificare il timeout per questa modalità usando le opzioni avanzate per i caratteri. Non è possibile impostare questo timeout dal codice dell'applicazione client.

Se un carattere tenta di parlare mentre l'utente parla, l'output udibile del carattere ha esito negativo anche se il testo potrebbe ancora essere visualizzato nel fumetto della parola. Se il carattere ha il canale audio mentre viene premuto il tasto Ascolto, il server trasferisce automaticamente il controllo all'utente dopo l'elaborazione del testo nel [**metodo Speak.**](speak-method.md) Viene riprodotto un tono MIDI facoltativo per incitare l'utente a iniziare a parlare. Ciò consente all'utente di fornire input anche se l'applicazione che guida il carattere non è riuscita a fornire pause logiche nell'output.

È anche possibile usare il [**metodo Listen**](listen-method.md) per avviare l'input vocale. La chiamata a questo metodo attiva il riconoscimento vocale per un periodo di tempo predefinito. Se durante questo intervallo non è presente alcun input, Microsoft Agent disattiva automaticamente il motore di riconoscimento vocale e libera il canale audio. In questo modo si evita di bloccare l'input o l'output dal dispositivo audio e si riduce al minimo il sovraccarico del processore utilizzato dal riconoscimento vocale quando è in uso. È anche possibile usare il **metodo Listen** per disattivare l'input vocale. Tenere tuttavia presente che, poiché il motore di riconoscimento vocale funziona in modo asincrono, l'effetto potrebbe non essere immediato. Di conseguenza, è possibile ricevere un evento [**Command**](command-event.md) anche dopo il codice denominato **Listen** per disattivare l'input vocale.

Per supportare l'input vocale, si definisce una *grammatica,* un set di  parole per [](/windows/desktop/lwef/the-command-object) cui il motore di riconoscimento vocale deve restare in ascolto e trovare una corrispondenza come impostazione Voce per un comando nella raccolta [**Comandi.**](/windows/desktop/lwef/the-commands-collection-object) È possibile includere parole facoltative e alternative e sequenze ripetute nella grammatica. Si noti che Agent non abilita il tasto di scelta rapida Ascolto fino a  quando uno dei relativi client non ha caricato correttamente un motore di riconoscimento vocale o non ha creato una voce per uno dei relativi **oggetti** Command.

Se l'utente preme il tasto di scelta rapida Ascolto o l'applicazione client chiama il metodo [**Listen**](listen-method.md) per avviare l'input vocale, il motore di riconoscimento vocale tenta di associare l'input di un'espressione alla grammatica per i comandi definiti e restituisce le informazioni al server. Il server invia quindi una notifica all'applicazione client usando l'evento [**Command**](command-event.md) ([**IAgentNotifySink::Command**](iagentnotifysink--command.md)); passaggio [**dell'oggetto UserInput**](/windows/desktop/lwef/iagentuserinput) che include l'ID comando della corrispondenza migliore e le due corrispondenze alternative (se presenti), un punteggio di attendibilità e il testo corrispondente per ogni corrispondenza.

Il server notifica anche all'applicazione client quando corrisponde all'input vocale a uno dei comandi forniti. Mentre l'ID comando è **NULL,** si ottengono comunque il punteggio di attendibilità e il testo corrispondente. In modalità di ascolto, il server riproduce automaticamente l'animazione assegnata allo stato di ascolto **del** carattere. Quindi, quando un'espressione viene effettivamente rilevata, il server riproduce l'animazione dello stato **Di** ascolto del carattere. Il server manterà il carattere in uno stato attento fino al termine dell'espressione. Ciò fornisce il feedback social appropriato per l'input dell'utente.

Se l'utente disabilita l'input vocale in Opzioni avanzate per i caratteri, verrà disabilitato anche il tasto di scelta rapida Ascolto. Analogamente, se si tenta di chiamare il metodo [**Listen**](listen-method.md) quando l'input vocale è disabilitato, il metodo avrà esito negativo.

 

 