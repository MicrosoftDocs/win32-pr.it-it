---
title: Modifiche a Microsoft Agent in Windows Vista
description: Modifiche a Microsoft Agent in Windows Vista
ms.assetid: 2498e8d5-2274-477c-a807-77443c76afb7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f73af45553f876c413fbea906de2369e888f1483
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221560"
---
# <a name="microsoft-agent-changes-in-windows-vista"></a>Modifiche a Microsoft Agent in Windows Vista

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Windows Vista introduce alcune modifiche nel modo in cui il riconoscimento vocale e vocale interagiscono con Windows Vista.

Microsoft Agent supporta ora i componenti di riconoscimento vocale e sintesi vocale di SAPI 5. Le proprietà TTSModeID e SRModeID dell'oggetto Agent vengono ancora utilizzate per determinare quale voce o riconoscimento è selezionato per l'agente e per modificare la selezione. Le modalità SAPI 4 vengono visualizzate come stringhe GUID come "{ca141fd0-AC7F-11D1-97a3-006008273000}", mentre i token SAPI 5 (equivalenti alle modalità) vengono visualizzati come nomi regolari, ad esempio "Microsoft Anna". Come nelle versioni precedenti, l'agente effettuerà una scelta predefinita dei motori TTS e SR. Se sono installati motori SAPI 5, questi saranno sempre preferiti su tutti i motori di SAPI 4 che possono essere installati. Il motore di sintesi vocale predefinito dell'utente, come specificato nel pannello di controllo, viene usato se il sesso corrisponde a quello del carattere; in caso contrario, viene scelto un motore SAPI 5 dello stesso sesso, se disponibile. Gli ID modalità specificati direttamente sul carattere vengono ignorati se sono presenti motori SAPI 5. Le selezioni predefinite possono essere verificate leggendo le proprietà TTSModeID e SRModeID all'inizio dello script.

Come prima, TTSModeID e SRModeID restituiranno una stringa vuota se non è presente la funzionalità di riconoscimento vocale o sintesi vocale. È possibile selezionare una voce o un riconoscitore specifico impostando queste proprietà sulla stringa in modalità SAPI 4 appropriata o sul nome del token SAPI 5. Dopo aver impostato una modalità o un token specifico, è anche possibile leggere di nuovo la proprietà per verificare che il relativo valore sia stato eseguito, a indicare che la nuova modalità o il token è effettivamente disponibile ed è stato selezionato correttamente. Per gli sviluppatori che distribuiscono Agent sul Web, tenere presente che molti utenti di vista avranno già installato una o più voci SAPI 5, quindi è consigliabile evitare di scaricare automaticamente SAPI 4 Voices, a meno che lo script non le richieda in modo specifico, perché la voce scaricata non viene utilizzata.

I motori di sintesi vocale SAPI 5 usano un set di standard diverso rispetto a SAPI 4 per l'annotazione di sintesi vocale con markup, ad esempio per modificare il pitch o la velocità del discorso. In SAPI 4 si usano i comandi "Slash", ad esempio/Pit = 170/. In SAPI 5 si usano i tag XML, ad esempio <PITCH MIDDLE="5"/> . In vista, Agent accetterà entrambi i tipi di annotazioni in Speak. i comandi "Slash" verranno ignorati dai motori SAPI 5 e i tag XML verranno ignorati dai motori SAPI 4. Come per i tag barra, il supporto per i tag di SAPI 5 XML varia da fornitore a fornitore e alcuni fornitori possono supportare altri tag. Per altre informazioni sui tag XML per SAPI 5, vedere la specifica di SAPI 5.

Agent non include più il supporto per più lingue. Il linguaggio utilizzato da Agent viene sempre considerato la lingua corrente dell'utente, come registrato con il sistema operativo. La proprietà LanguageID dell'oggetto Agent è ancora scrivibile, ma il relativo valore viene ignorato da Agent in vista. Se, ad esempio, la lingua dell'utente è impostata su inglese (Stati Uniti) (&H0409) e usa un programma che imposta LanguageID su francese (&H040C), il testo del suggerimento vocale e le finestre di dialogo delle opzioni dei caratteri avanzati verranno comunque visualizzate in inglese.

 

 




