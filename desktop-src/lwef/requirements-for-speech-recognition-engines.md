---
title: Requisiti per i motori di riconoscimento vocale
description: Requisiti per i motori di riconoscimento vocale
ms.assetid: 41aca5da-c680-41c1-b070-af291cb0c8e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1315d395e3053d5f6f71fd7f8ff17cb815bea26fc4875878da74dd77113d5e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975751"
---
# <a name="requirements-for-speech-recognition-engines"></a>Requisiti per i motori di riconoscimento vocale

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Un motore di riconoscimento vocale deve anche essere un motore di comando e controllo (C&C) completamente conforme a SAPI 4.0. Deve supportare più grammatiche nel formato binario descritto nella specifica e consentire l'attivazione o la disattivazione di tali grammatiche in tempo reale.

Si noti che SAPI 4.0 richiede che i motori di riconoscimento vocale supportino le interfacce Unicode a caratteri wide. Tuttavia, nel supporto di queste interfacce, il motore non deve dipendere dalla conversione dei dati Unicode in ANSI, perché il motore potrebbe non funzionare correttamente in alcuni sistemi. Ad esempio, un motore giapponese che converte Unicode in ANSI potrebbe non funzionare in un sistema Microsoft Windows 95 in lingua inglese.

Inoltre, per essere considerato conforme a Microsoft Agent, il motore deve restituire oggetti risultati al completamento del riconoscimento di una frase (tramite ISRGramNotifySinkW::P hraseFinish). Questi oggetti risultati devono supportare ISRResBasic, come richiesto dalla specifica. Inoltre, devono supportare ISRResScore. Anche se Microsoft Agent verrà eseguito con un motore che supporta solo ISRResBasic o anche con un motore che non restituisce alcun oggetto risultato, le prestazioni saranno in genere notevolmente più scarse con tali motori. Molte applicazioni usano i valori di attendibilità forniti dal motore per controllare il modo in cui rispondono ai vari comandi.

 

 




