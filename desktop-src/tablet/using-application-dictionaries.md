---
description: Per impostazione predefinita, il sistema di riconoscimento usa un dizionario di sistema che contiene tutte le parole scritte comunemente in una lingua.
ms.assetid: 2ddf04dd-613b-4570-9474-0e33208c4012
title: Uso dei dizionari applicazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c83013f704fe28b5754ab89fd95ed730e16d1cda5ab257d4fb411d0e7293347
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449233"
---
# <a name="using-application-dictionaries"></a>Uso dei dizionari applicazioni

Per impostazione predefinita, il sistema di riconoscimento usa un dizionario di sistema che contiene tutte le parole scritte comunemente in una lingua. Inoltre, il sistema di riconoscimento ha un dizionario utente che contiene le parole che l'utente ha aggiunto al dizionario. Gli utenti aggiungono una parola al dizionario utente tramite il Pannello di input di Tablet PC tramite le selezioni in:

-   Elenco alternativo (durante la scrittura).
-   Menu Strumenti di riconoscimento vocale (quando si parla).

Se si progetta un'applicazione in cui si prevede che l'utente scriverà parole che non si trovano nel dizionario di sistema o nel dizionario utente, creare un dizionario dell'applicazione. Un dizionario applicazioni migliora ulteriormente l'accuratezza del riconoscimento fornendo al riconoscimento un elenco personalizzato aggiuntivo di parole che probabilmente verranno immesse come grafia in un'applicazione.

Per creare un dizionario applicazioni, usare [**l'oggetto WordList.**](inkwordlist-class.md) Il dizionario applicazioni che ne deriva aumenta l'accuratezza del riconoscimento fornendo al riconoscitore un elenco di parole previste. Ad esempio, un dizionario applicazioni che contiene terminologia sanitaria aumenta l'accuratezza del riconoscimento all'interno di un'applicazione sviluppata per il settore sanitario in cui è probabile che i termini siano scritti.

Come altro esempio, quando si progetta un modulo per ordinare gli strumenti di strumentazione, creare un oggetto [**WordList**](inkwordlist-class.md) contenente i nomi dei produttori di strumenti più comuni. Impostare la [**proprietà WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) [**dell'oggetto RecognizerContext**](inkrecognizercontext-class.md) **sull'oggetto WordList** creato. Questo elenco di parole viene quindi passato al riconoscimento **dall'oggetto RecognizerContext.** Il dizionario applicazioni aumenta l'accuratezza del riconoscimento quando tali nomi vengono scritti in un campo dell'applicazione.

Gli argomenti seguenti descrivono come usare i dizionari delle applicazioni.

-   [Informazioni su elenchi di parole, contesto di riconoscimento e factoid](understanding-wordlists--the-recognizercontext--and-factoids.md)
-   [Uso dei dizionari applicazioni con le API della piattaforma Tablet PC](using-application-dictionaries-with-the-tablet-pc-platform-apis.md)
-   [Creazione di dizionari personalizzati per il riconoscimento della grafia](creating-custom-dictionaries-for-handwriting-recognition-in-windows-7-and-windows-server-2008-r2.md)

 

 



