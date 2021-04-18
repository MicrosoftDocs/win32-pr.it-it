---
title: Supporto per input vocale
description: Supporto per input vocale
ms.assetid: 4702b941-fcc9-4d00-aba2-eca624b6d417
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8ecb6f2ddfbbe10f8b892ce922cd466eca96890
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299794"
---
# <a name="speech-input-support"></a>Supporto per input vocale

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Oltre a supportare l'interazione con il mouse e la tastiera, Microsoft Agent include il supporto diretto per l'input vocale. Poiché il supporto per l'input vocale di Microsoft Agent è basato su Microsoft SAPI (Speech Application Programming Interface), è possibile usare l'agente Microsoft con i motori di comando e controllo di riconoscimento vocale che includono il supporto di SAPI-required. Per ulteriori informazioni sui requisiti del motore vocale, vedere [requisiti del supporto del motore vocale](requirements-for-speech-recognition-engines.md).

Microsoft fornisce un motore di riconoscimento vocale con comando e controllo che è possibile utilizzare con Microsoft Agent. Per ulteriori informazioni, vedere [selezione del motore di riconoscimento vocale](speech-engine-selection.md).

L'utente può avviare l'input vocale tenendo premuto il tasto di scelta rapida per l'ascolto push-to-Talk. In questa modalità di ascolto, se il motore di riconoscimento vocale riceve l'inizio dell'input vocale, il canale audio rimane aperto fino a quando non rileva la fine dell'espressione. Tuttavia, quando non riceve l'input, non blocca l'output audio. Ciò consente all'utente di emettere più comandi vocali tenendo premuto il tasto e il carattere può rispondere quando l'utente non parla.

La modalità di ascolto scade quando l'utente rilascia il tasto di attesa. L'utente può regolare il timeout per questa modalità usando le opzioni per i caratteri avanzati. Non è possibile impostare questo timeout dal codice dell'applicazione client.

Se un carattere tenta di parlare mentre l'utente sta parlando, l'output udibile del carattere ha esito negativo, anche se il testo può comunque essere visualizzato nella relativa bolla di Word. Se il carattere dispone del canale audio mentre viene premuto il tasto ascolto, il server trasferisce automaticamente il controllo all'utente dopo l'elaborazione del testo nel metodo [**Speak**](speak-method.md) . Viene riprodotto un tono MIDI facoltativo per fare in modo che l'utente inizi a pronunciare. Ciò consente all'utente di fornire l'input anche se l'applicazione che guida il carattere non è riuscita a fornire pause logiche nell'output.

È anche possibile usare il metodo [**Listen**](listen-method.md) per avviare l'input vocale. La chiamata a questo metodo attiva il riconoscimento vocale per un periodo di tempo predefinito. Se non è presente alcun input durante questo intervallo, Microsoft Agent disattiva automaticamente il motore di riconoscimento vocale e libera il canale audio. In questo modo si evita il blocco dell'input o dell'output dal dispositivo audio e si riduce al minimo l'overhead del processore usato dal riconoscimento vocale quando è acceso. È anche possibile usare il metodo **Listen** per disattivare l'input vocale. Tuttavia, tenere presente che, poiché il motore di riconoscimento vocale opera in modo asincrono, l'effetto potrebbe non essere immediato. Di conseguenza, è possibile ricevere un evento di [**comando**](command-event.md) anche dopo che il codice ha chiamato **Listen** per disattivare l'input vocale.

Per supportare l'input vocale, si definisce una *grammatica*, un set di parole per cui il motore di riconoscimento vocale è in ascolto e la corrispondenza come impostazione **vocale** per un [**comando**](/windows/desktop/lwef/the-command-object) nella raccolta di [**comandi**](/windows/desktop/lwef/the-commands-collection-object) . È possibile includere parole opzionali e alternative e sequenze ripetute nella grammatica. Si noti che Agent non Abilita il tasto di scelta rapida in ascolto fino a quando uno dei client non ha caricato correttamente un motore vocale o ha creato una **voce** per uno degli oggetti **Command** .

Indica se l'utente preme la scelta rapida in ascolto o se l'applicazione client chiama il metodo [**Listen**](listen-method.md) per avviare l'input vocale, il motore di riconoscimento vocale tenta di trovare la corrispondenza con l'input di un enunciato alla grammatica per i comandi definiti e passa le informazioni al server. Il server invia quindi una notifica all'applicazione client utilizzando l'evento di [**comando**](command-event.md) ([**IAgentNotifySink:: Command**](iagentnotifysink--command.md)); passaggio all'oggetto [**userinput**](/windows/desktop/lwef/iagentuserinput) che include l'ID del comando della corrispondenza migliore e due corrispondenze alternative (se presenti), un punteggio di confidenza e il testo corrispondente per ogni corrispondenza.

Il server invia anche una notifica all'applicazione client quando corrisponde all'input vocale a uno dei comandi forniti. Mentre l'ID del comando è **null**, si ottengono comunque il Punteggio di confidenza e il testo corrispondenti. In modalità di ascolto, il server riproduce automaticamente l'animazione assegnata allo stato di **ascolto** del carattere. Quindi, quando viene effettivamente rilevato un enunciato, il server riproduce l'animazione dello stato di **udito** del carattere. Il server manterrà il carattere in uno stato attento fino alla fine dell'espressione. Questo fornisce il feedback sociale appropriato per l'input da parte dell'utente.

Se l'utente disabilita l'input vocale nelle opzioni per caratteri avanzati, verrà disabilitato anche il tasto di scelta rapida in ascolto. Analogamente, se si tenta di chiamare il metodo [**Listen**](listen-method.md) quando l'input vocale è disabilitato, il metodo avrà esito negativo.

 

 