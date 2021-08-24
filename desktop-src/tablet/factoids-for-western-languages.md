---
description: Le lingue occidentali sono definite come inglese (Regno Unito), inglese (Stati Uniti), francese, tedesco e spagnolo.
ms.assetid: d4728506-7484-4c4c-a5ae-e98d699f7e76
title: Factoid per le lingue occidentali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e417c9662252213d761760a1486f9808a2d18bc3236073fe8c8d7746c396beb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119936541"
---
# <a name="factoids-for-western-languages"></a>Factoid per le lingue occidentali

Le lingue occidentali sono definite come inglese (Regno Unito), inglese (Stati Uniti), francese, tedesco e spagnolo. I formati all'interno di ogni factoid illustrato nella tabella seguente sono specifici del riconoscimento di ogni lingua. Ad esempio, **il** factoid Telefono è diverso in ogni lingua. Inoltre, ogni factoid è specifico di un particolare sistema di riconoscimento. Ad esempio, il factoid **Telefono** francese può essere usato solo con il riconoscimento francese.

> [!Note]  
> Oltre ai factoid seguenti, tutti i linguaggi usano i factoid elencati in [Factoids Common Across Languages](factoids-common-across-languages.md).

 



| Factoid              | Definizione                                                                                                                                                                                                                                                                                                                                                                                                           | Esempio                                                                                                                                                                                                                                                            |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Filename**         | Imposta la distorsione per un percorso del nome file. Il nome non può includere i caratteri<br/> / " < > \|<br/> I caratteri \* e ? sono inclusi in questo factoid per abilitare la ricerca. Inoltre, i caratteri estesi sono supportati nelle lingue europae.<br/>                                                                                                                                                    | c:<br/> \\\\nome directory \\ nomefile<br/> \\\\directory1 \\ directory2 \\ filename<br/> \\\\directoryname \\ \* .\*<br/> Filename.?<br/> myfile.doc<br/>                                                                                |
| **SystemDictionary** | Abilita solo il dizionario di sistema. Ciò è utile se un'applicazione esegue una query se una parola si trova nel dizionario di sistema. Impostare factoid su **SystemDictionary e** chiamare il [**metodo IsStringSupported.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-isstringsupported)<br/>                                                                                                                                                 | Il modello linguistico predefinito include la grammatica per la lingua e il dizionario di sistema. Questo factoid biases recognition verso solo le parole che si verificano nel dizionario di sistema. Ogni lingua ha un proprio dizionario di sistema.<br/>                   |
| **Wordlist**         | Abilita solo l'elenco di parole. Se il factoid è impostato su **WordList** ma non viene assegnato alcun elenco di parole [**a InkRecognizerContext**](inkrecognizercontext-class.md) [(RecognizerContext](/previous-versions/ms552546(v=vs.100)) nel codice gestito), viene usato il dizionario utente. Per altre informazioni sugli elenchi di parole e i dizionari, vedere [Uso dei dizionari applicazioni.](using-application-dictionaries.md)<br/> | Questa distorsione factoide prescindo dal riconoscimento per restituire solo le parole nell'elenco di parole. Ad esempio, per consentire all'utente di immettere un colore in un modulo, è possibile usare questo factoid e un elenco di parole che contiene "Verde", "Rosso", "Blu", "Bianco" e altri colori.<br/> |



 

Le combinazioni di factoid seguenti sono supportate solo per le lingue occidentali. Altre combinazioni di factoid non sono supportate in questa versione delle API (Application Programming Interface) della piattaforma Tablet PC. Queste combinazioni di factoid utilizzano un operatore **OR** logico, pertanto l'input può corrispondere a qualsiasi factoid nell'espressione.



| Combinazione factoide     | Definizione                                                                   |
|-------------------------|------------------------------------------------------------------------------|
| **WebWordList**         | Factoid **Web** o elenco di parole.<br/>                             |
| **EmailWordList**       | Factoid **email** o elenco di parole.<br/>                           |
| **FilenameWebWordList** | **Factoid** nome file, **factoid Web** o elenco di parole.<br/> |



 

Gli argomenti seguenti illustrano i formati supportati per ogni lingua occidentale.

-   [Inglese (a livello mondiale) Factoid](english--worldwide--factoids.md)
-   [Factoid in inglese (Stati Uniti)](english--united-states--factoids.md)
-   [Factoid francese](french-factoids.md)
-   [Factoid tedesco](german-factoids.md)
-   [Factoid spagnoli](spanish-factoids.md)

 

