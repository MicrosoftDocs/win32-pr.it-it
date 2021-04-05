---
description: Le lingue occidentali sono definite in inglese (Regno Unito), inglese (Stati Uniti), francese, tedesco e spagnolo.
ms.assetid: d4728506-7484-4c4c-a5ae-e98d699f7e76
title: Factoids per le lingue occidentali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de98cfce0203a2a3a94509d6586c1596390ca16b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049529"
---
# <a name="factoids-for-western-languages"></a>Factoids per le lingue occidentali

Le lingue occidentali sono definite in inglese (Regno Unito), inglese (Stati Uniti), francese, tedesco e spagnolo. I formati all'interno di ogni controllo oggetto specificato nella tabella seguente sono specifici del riconoscimento di ogni linguaggio. Ad esempio, il controllo dell'oggetto **telefonico** è diverso in ogni lingua. Ogni controllo oggetto è inoltre specifico di un determinato riconoscimento. È ad esempio possibile utilizzare il controllo del controllo **telefonico** francese solo con il riconoscimento francese.

> [!Note]  
> Oltre ai seguenti factoids, tutti i linguaggi usano i factoids elencati in [factoids comuni tra più linguaggi](factoids-common-across-languages.md).

 



| Factoid              | Definizione                                                                                                                                                                                                                                                                                                                                                                                                           | Esempio                                                                                                                                                                                                                                                            |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Filename**         | Imposta la distorsione per un percorso di nome file. Il nome non può includere i caratteri<br/> /" < > \|<br/> I caratteri \* e? sono incluse in questo oggetto del controllo per abilitare la ricerca. Inoltre, i caratteri estesi sono supportati nelle lingue europee.<br/>                                                                                                                                                    | c:<br/> \\\\\\nome file DirectoryName<br/> \\\\directory1 \\ directory2 \\ nomefile<br/> \\\\DirectoryName \\ \* .\*<br/> nome file.<br/> myfile.doc<br/>                                                                                |
| **SystemDictionary** | Abilita solo il dizionario di sistema. Questa operazione è utile se un'applicazione esegue una query se una parola si trova nel dizionario di sistema. Impostare il controllo del controllo su **SystemDictionary** e chiamare il metodo [**IsStringSupported**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-isstringsupported) .<br/>                                                                                                                                                 | Il modello di lingua predefinito include la grammatica per il linguaggio e il dizionario di sistema. Questo controllo di stato polarizza il riconoscimento verso solo le parole che si verificano nel dizionario di sistema. Ogni lingua dispone di un proprio dizionario di sistema.<br/>                   |
| **Elenco delle parole**         | Abilita solo l'elenco di parole. Se il controllo del controllo è impostato su **WordList** ma non è assegnato alcun elenco di parole a [**InkRecognizerContext**](inkrecognizercontext-class.md) ([RecognizerContext](/previous-versions/ms552546(v=vs.100)) nel codice gestito), viene usato il dizionario utente. Per altre informazioni sugli elenchi di parole e sui dizionari, vedere [uso dei dizionari delle applicazioni](using-application-dictionaries.md).<br/> | Questo controllo di stato polarizza il riconoscimento verso la restituzione solo delle parole nell'elenco di parole. Ad esempio, per consentire all'utente di immettere un colore in un modulo, è possibile usare questo controllo e un elenco di parole che contiene "verde", "rosso", "blu", "bianco" e altri colori.<br/> |



 

Le seguenti combinazioni di factoids sono supportate solo per le lingue occidentali. Altre combinazioni di factoids non sono supportate in questa versione delle API (Application Programming Interface) della piattaforma Tablet PC. Queste combinazioni di controllo dei dati utilizzano **un operatore OR** logico, pertanto l'input può corrispondere a qualsiasi factoids nell'espressione.



| Combinazione del controllo del controllo     | Definizione                                                                   |
|-------------------------|------------------------------------------------------------------------------|
| **Webwordlist**         | Controllo **Web** o elenco di parole.<br/>                             |
| **EmailWordList**       | Il controllo dell' **indirizzo di posta elettronica** o l'elenco di parole.<br/>                           |
| **FilenameWebWordList** | Controllo del **nome del file** o controllo dell'oggetto **Web** o elenco di parole.<br/> |



 

Negli argomenti seguenti vengono illustrati i formati supportati per ogni lingua occidentale.

-   [Inglese (mondiale) factoids](english--worldwide--factoids.md)
-   [Inglese (Stati Uniti) factoids](english--united-states--factoids.md)
-   [Factoids francese](french-factoids.md)
-   [Factoids tedesco](german-factoids.md)
-   [Factoids spagnolo](spanish-factoids.md)

 

