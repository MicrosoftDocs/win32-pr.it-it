---
title: ITTSBufNotifySinkW
description: ITTSBufNotifySinkW
ms.assetid: 00f4a529-2db1-4cad-9340-ed95999448f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de27451826a232092bc74e630a54621a004cc15e44ad4a9a7d3377509ff00ca5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118476718"
---
# <a name="ittsbufnotifysinkw"></a>ITTSBufNotifySinkW

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Il motore deve chiamare tramite **BookMark**. Durante la pre-elaborazione dell'output vocale, il codice di Microsoft Agent inserisce segnalibri tra "parole" e usa l'arrivo di tali segnalibri per guidare il ritmo del testo nel fumetto delle parole. Anche se SAPI non richiede altro che l'arrivo di tali segnalibri in un certo momento prima della fine dell'espressione, i segnalibri devono essere restituiti in modo relativamente temporale per supportare Microsoft Agent.

Si noti che non esiste un concetto rigoroso di "parola" in alcune lingue, ad esempio il giapponese. Il metodo [**Speak di**](speak-method.md) Microsoft Agent definisce una "parola" come stringa connessa di simboli con significato e pronuncia in isolamento. Microsoft Agent usa codice di analisi piuttosto semplice per determinare che cos'è una "parola": cerca simboli separati da spazi vuoti. Nella stringa inglese "The 101 Dalmatians", quindi, sono presenti tre "parole": "the", "one hundred and one" e "Dalmati". Il testo incluso nel tag mappa di Microsoft Agent viene considerato come una singola "parola" a scopo di visualizzazione.

 

 




