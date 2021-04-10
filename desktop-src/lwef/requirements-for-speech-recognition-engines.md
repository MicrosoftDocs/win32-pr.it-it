---
title: Requisiti per i motori di riconoscimento vocale
description: Requisiti per i motori di riconoscimento vocale
ms.assetid: 41aca5da-c680-41c1-b070-af291cb0c8e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9214f13b11a071ec8d8599f0b6dd542884ae05f8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955721"
---
# <a name="requirements-for-speech-recognition-engines"></a>Requisiti per i motori di riconoscimento vocale

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Un motore di riconoscimento vocale deve anche essere un motore di comando e controllo completamente compatibile (C&C) in base a SAPI 4,0. Deve supportare più grammatiche nel formato binario descritto nella specifica e consentire l'attivazione o la disattivazione di tali grammatiche in tempo reale.

Si noti che SAPI 4,0 richiede che i motori di riconoscimento vocale supportino le interfacce Unicode a caratteri wide. Tuttavia, nel supportare queste interfacce, il motore non deve dipendere dalla conversione dei dati Unicode in ANSI, perché il motore potrebbe non funzionare correttamente in alcuni sistemi. Ad esempio, un motore giapponese che converte Unicode in ANSI potrebbe non funzionare in un sistema Microsoft Windows 95 in lingua inglese.

Inoltre, per essere considerato conforme a Microsoft Agent, il motore deve restituire oggetti results dopo il riconoscimento corretto di una frase (tramite ISRGramNotifySinkW::P hraseFinish). Questi oggetti risultati devono supportare ISRResBasic, come richiesto dalla specifica. Inoltre, devono supportare ISRResScore. Anche se Microsoft Agent verrà eseguito con un motore che supporta solo ISRResBasic o anche con un motore che non restituisce alcun oggetto di risultati, le prestazioni sono in genere significativamente più scarse con tali motori. Molte applicazioni usano i valori di confidenza forniti dal motore per controllare la modalità di risposta ai vari comandi.

 

 




