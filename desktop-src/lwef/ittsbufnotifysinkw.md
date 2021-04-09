---
title: ITTSBufNotifySinkW
description: ITTSBufNotifySinkW
ms.assetid: 00f4a529-2db1-4cad-9340-ed95999448f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678a1ce3013ba1d8acf01f79b4f71d2d5088f4d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955772"
---
# <a name="ittsbufnotifysinkw"></a>ITTSBufNotifySinkW

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Il motore deve chiamare tramite **segnalibro**. Durante la pre-elaborazione dell'output vocale, il codice dell'agente Microsoft inserisce segnalibri tra "parole" e usa l'arrivo di tali segnalibri per guidare la velocità del testo nel fumetto di Word. Sebbene SAPI non richieda più dell'arrivo di questi segnalibri in un determinato momento prima della fine dell'espressione, i segnalibri devono essere restituiti in modo relativamente tempestivo per supportare Microsoft Agent.

Si noti che non esiste un concetto rigoroso di "parola" in alcune lingue, ad esempio il giapponese. Il metodo [**Speak**](speak-method.md) di Microsoft Agent definisce una "parola" come una stringa connessa di simboli con un significato e una pronuncia in isolamento. Microsoft Agent usa un codice di analisi piuttosto semplice per determinare la "parola": Cerca i simboli separati da spazi vuoti. Ci sono quindi tre "parole" nella stringa inglese "The 101 Dalmati": "The", "101" e "Dalmati". Il testo incluso nel tag della mappa di Microsoft Agent viene considerato come una singola parola a scopo di visualizzazione.

 

 




