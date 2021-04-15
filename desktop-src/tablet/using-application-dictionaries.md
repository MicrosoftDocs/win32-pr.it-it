---
description: Per impostazione predefinita, il riconoscimento utilizza un dizionario di sistema che contiene tutte le parole scritte comunemente in un linguaggio.
ms.assetid: 2ddf04dd-613b-4570-9474-0e33208c4012
title: Uso di dizionari applicazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74dfda443a688af9dfcec44a81f0e5ed2d50846c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484788"
---
# <a name="using-application-dictionaries"></a>Uso di dizionari applicazioni

Per impostazione predefinita, il riconoscimento utilizza un dizionario di sistema che contiene tutte le parole scritte comunemente in un linguaggio. Il riconoscimento dispone inoltre di un dizionario utente che contiene parole che l'utente ha aggiunto al dizionario. Gli utenti aggiungono una parola al dizionario utente tramite il pannello input penna di Tablet PC attraverso le selezioni in:

-   Elenco alternativo (durante la scrittura).
-   Menu strumenti vocali (in lingua inglese).

Se si sta progettando un'applicazione in cui si prevede che l'utente scriva parole che non sono presenti nel dizionario di sistema o nel dizionario utente, creare un dizionario dell'applicazione. Un dizionario applicazioni migliora ulteriormente l'accuratezza del riconoscimento fornendo al sistema di riconoscimento un elenco personalizzato aggiuntivo di parole che è probabile immettere come grafia in un'applicazione.

Per creare un dizionario applicazioni, usare l'oggetto [**WordList**](inkwordlist-class.md) . Il dizionario applicazioni risultante aumenta l'accuratezza del riconoscimento fornendo al riconoscimento un elenco di parole previste. Ad esempio, un dizionario di applicazioni che contiene la terminologia medica aumenta l'accuratezza del riconoscimento all'interno di un'applicazione sviluppata per il settore medico in cui è probabile che i termini vengano scritti.

Come altro esempio, quando si progetta un modulo per un utente per ordinare gli strumenti musicali, creare un oggetto [**WordList**](inkwordlist-class.md) contenente i nomi dei produttori di strumenti più comuni. Impostare la proprietà [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) dell'oggetto [**RecognizerContext**](inkrecognizercontext-class.md) sull'oggetto **WordList** creato. Questo elenco di parole viene quindi passato al riconoscimento dall'oggetto **RecognizerContext** . Il dizionario applicazioni aumenta l'accuratezza del riconoscimento quando tali nomi vengono scritti in un campo nell'applicazione.

Negli argomenti seguenti viene descritto come utilizzare i dizionari applicazione.

-   [Informazioni sugli elenchi di parole, contesto di riconoscimento e factoids](understanding-wordlists--the-recognizercontext--and-factoids.md)
-   [Uso dei dizionari applicazioni con le API della piattaforma Tablet PC](using-application-dictionaries-with-the-tablet-pc-platform-apis.md)
-   [Creazione di dizionari personalizzati per il riconoscimento della grafia](creating-custom-dictionaries-for-handwriting-recognition-in-windows-7-and-windows-server-2008-r2.md)

 

 



