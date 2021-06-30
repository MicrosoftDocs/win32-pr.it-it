---
title: Modifiche di Microsoft Agent in Windows Vista
description: Modifiche di Microsoft Agent in Windows Vista
ms.assetid: 2498e8d5-2274-477c-a807-77443c76afb7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 440fb8afb7acb0118c1e48669089c083e935db5b
ms.sourcegitcommit: 967ba3a2a618e6088cb607164a2a924530278645
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113102150"
---
# <a name="microsoft-agent-changes-in-windows-vista"></a>Modifiche di Microsoft Agent in Windows Vista

\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Windows Vista introduce alcune modifiche nell'interazione del riconoscimento vocale e del riconoscimento vocale con Windows Vista.

Microsoft Agent supporta ora i componenti di sintesi vocale e riconoscimento vocale di SAPI 5. Le proprietà TTSModeID e SRModeID dell'oggetto Agent vengono comunque usate per determinare quale voce o sistema di riconoscimento è selezionato per l'agente e per modificare questa selezione. Le modalità SAPI 4 vengono visualizzate come stringhe GUID, ad esempio "{ca141fd0-ac7f-11d1-97a3-006008273000}", mentre i token SAPI 5 (equivalenti alle modalità) vengono visualizzati come nomi regolari, ad esempio "Microsoft Anna". Come nelle versioni precedenti, l'agente farà una scelta predefinita di motori TTS e SR. Se sono installati motori SAPI 5, questi saranno sempre preferiti rispetto ai motori SAPI 4 che possono essere installati. Il motore di sintesi vocale predefinito dell'utente, come specificato nel pannello di controllo, viene usato se il sesso corrisponde a quello del carattere. In caso contrario, viene scelto un motore SAPI 5 dello stesso sesso, se disponibile. Gli ID modalità specificati direttamente nel carattere vengono ignorati se sono presenti motori SAPI 5. Le selezioni predefinite possono essere verificate leggendo le proprietà TTSModeID e SRModeID all'inizio dello script.

Come in precedenza, TTSModeID e SRModeID restituiranno una stringa vuota se la funzionalità Sintesi vocale o Riconoscimento vocale non è presente. È possibile selezionare una voce o un sistema di riconoscimento specifico impostando queste proprietà sulla stringa in modalità SAPI 4 o sul nome del token SAPI 5 appropriato. Dopo aver impostato una modalità o un token specifico, è anche possibile leggere di nuovo la proprietà per verificare che il relativo valore sia stato utilizzato, che indica che la nuova modalità o il nuovo token era effettivamente disponibile ed è stato selezionato correttamente. Per gli sviluppatori che distribuiscono Agent sul Web, si noti che molti utenti di Vista avranno già installato una o più voci SAPI 5, quindi è possibile evitare il download automatico delle voci SAPI 4 a meno che lo script non le chieri in modo specifico, perché la voce scaricata non verrà usata.

I motori di sintesi vocale SAPI 5 usano un set di standard diverso rispetto a SAPI 4 per annotare la voce con markup, ad esempio per modificare l'intonazione o la frequenza del parlato. In SAPI 4 si usano comandi "barra", ad esempio /pit=170/. In SAPI 5 si usano tag XML, ad esempio \<PITCH MIDDLE="5"/> . In Vista Agent accetterà entrambi i tipi di annotazioni nei comandi "slash" delle stringhe del metodo Speak, che verranno ignorati dai motori SAPI 5 e i tag XML verranno ignorati dai motori SAPI 4. Come per i tag slash, il supporto per i tag XML SAPI 5 varia da fornitore a fornitore e alcuni fornitori possono supportare tag aggiuntivi. Per altre informazioni sui tag XML di SAPI 5, vedere la specifica SAPI 5.

Agent non include più il supporto per più lingue. Si presuppone sempre che la lingua usata da Agent sia la lingua corrente dell'utente, come registrato con il sistema operativo. La proprietà LanguageID dell'oggetto Agent è ancora scrivibile, ma il relativo valore viene ignorato da Agent in Vista. Ad esempio, se la lingua dell'utente è impostata su Inglese (Stati Uniti&H0409) e usa un programma che imposta LanguageID sul francese (&H040C), il testo del suggerimento vocale e le finestre di dialogo Opzioni carattere avanzate verranno comunque visualizzate in inglese.

 

 




