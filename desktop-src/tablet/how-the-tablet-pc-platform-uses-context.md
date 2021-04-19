---
description: Gli sviluppatori che creano applicazioni per Tablet PC sono in grado di sfruttare i vantaggi dell'ambito di input e delle informazioni sul contesto.
ms.assetid: 74e4e4b2-6ceb-4044-84df-2fff0788267a
title: Modalità di utilizzo del contesto da parte della piattaforma Tablet PC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcd991a2ad8e76bb0a96ea5e41977b158cc30f5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307483"
---
# <a name="how-the-tablet-pc-platform-uses-context"></a>Modalità di utilizzo del contesto da parte della piattaforma Tablet PC

Gli sviluppatori che creano applicazioni per Tablet PC sono in grado di sfruttare i vantaggi dell'ambito di input e delle informazioni sul contesto. Le migliori soluzioni possibili per l'impostazione delle informazioni di contesto sui controlli nelle applicazioni variano a seconda che il controllo sia abilitato per l'input penna e che l'applicazione sia stata rilasciata sul mercato. Un controllo abilitato per l'input penna è uno appositamente progettato per l'input penna e in cui i dati di input penna vengono raccolti e salvati in modo permanente come input penna. Esempi di applicazioni abilitate per l'input penna sono Microsoft Windows Journal o un programma di sketch. In un controllo non abilitato per l'input penna, i dati di input vengono raccolti e salvati in modo permanente come testo, in genere tramite il pannello input penna di Tablet PC quando l'applicazione viene eseguita in un Tablet PC. Le soluzioni per l'abilitazione delle informazioni di contesto nei controlli sono:

-   API [SetInputScope](/windows/win32/api/inputscope/nf-inputscope-setinputscope) : soluzione a livello di codice di basso livello per le applicazioni e i controlli non abilitati per input penna. I file binari per l'applicazione sono interessati e devono essere ridistribuiti.
-   Proprietà del [**controllo dell'oggetto**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) [**RecognizerContext**](inkrecognizercontext-class.md) e dell'oggetto [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) : una soluzione a livello di codice per le applicazioni con controlli con input penna abilitati. I file binari per l'applicazione sono interessati e devono essere ridistribuiti.

Il pannello input penna di Tablet PC è stato aggiornato a partire da Windows Vista per sfruttare le informazioni di contesto fornite quando si utilizzano le API [SetInputScope](/windows/win32/api/inputscope/nf-inputscope-setinputscope) . La tabella seguente fornisce informazioni dettagliate sui motori di riconoscimento Microsoft che supportano gli ambiti di input. Una "X" nella riga per un ambito di input indica che il riconoscimento in tale colonna supporta l'ambito di input.



| Nome della proprietà                                     | Inglese (Stati Uniti) | Inglese (Regno Unito) | Tedesco       | Francese       | Giapponese     | Coreano       | Cinese (semplificato) | Cinese (tradizionale) |
|---------------------------------------------------|-------------------------|--------------------------|--------------|--------------|--------------|--------------|----------------------|-----------------------|
| **\_indirizzo \_ FULLPOSTALADDRESS**<br/>     | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_indirizzo ( \_ Cap)**<br/>            | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_indirizzo della \_ strada**<br/>                | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_indirizzo \_ STATEORPROVINCE**<br/>       | X<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_città indirizzo \_**<br/>                  | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_indirizzo \_ CountryName**<br/>           | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_indirizzo \_ COUNTRYSHORTNAME**<br/>      | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_valuta \_ AMOUNTANDSYMBOL**<br/>      | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_importo valuta \_**<br/>               | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_data \_ FULLDATE**<br/>                 | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_mese data di inizio \_**<br/>                    | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_data \_ giorno**<br/>                      | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_data \_ anno**<br/>                     | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_data \_ mesename**<br/>                | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_data \_ NomeGiorno**<br/>                  | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **è il \_ valore predefinito**<br/>                        | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_ \_ nome utente posta elettronica**<br/>                | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_SMTPEMAILADDRESS posta elettronica \_**<br/>        | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_file \_ FULLFILEPATH**<br/>             | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_nome file file \_**<br/>                 | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_LoginName**<br/>                      | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_cifre**<br/>                         | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_numero**<br/>                         | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **è \_ ONechar**<br/>                        | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_password**<br/>                       | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **è \_ personalname \_ FullName**<br/>         | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **il \_ prefisso è personalname \_**<br/>           | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **è \_ personalname \_ datoname**<br/>        | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **è \_ personalname \_ MiddleName**<br/>       | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_ \_ cognome personale**<br/>          | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_suffisso è personalname \_**<br/>           | X<br/>            | -<br/>             | X<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_FULLTELEPHONENUMBER telefono \_**<br/> | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_COUNTRYCODE telefono \_**<br/>         | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_AREACODE telefono \_**<br/>            | X<br/>            | X<br/>             | X<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_LOCALNUMBER telefono \_**<br/>         | X<br/>            | X<br/>             | X<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_tempo \_ pieno**<br/>                 | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **ora di ora \_ \_**<br/>                     | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_ora \_ MINORSEC**<br/>                 | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_URL**<br/>                            | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_numero \_ fullwidth**<br/>              | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_carattere alfanumerico \_**<br/>        | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_fullwidth alfanumerico \_**<br/>        | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_valuta \_ cinese**<br/>              | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_BOPOMOFO**<br/>                       | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_Hiragana**<br/>                       | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_carattere katakana \_**<br/>            | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_fullwidth katakana \_**<br/>            | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_Hanja**<br/>                          | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |



 

Quando si usano le API [SetInputScope](/windows/win32/api/inputscope/nf-inputscope-setinputscope) o [**la proprietà del controllo dell'oggetto**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) [**RecognizerContext**](inkrecognizercontext-class.md) per impostare il contesto, il tentativo di impostare un ambito di input per una lingua non supportata dal riconoscimento di tale lingua causa il pannello di input di Tablet PC per l'uso del modello di lingua predefinito come contesto per il controllo. Ad esempio, l'ambito di input **\_ \_ STATEORPROVINCE è Address** non è supportato dal riconoscimento francese. Se si imposta Context su un campo come

`(!IS_ADDRESS_STATEORPROVINCE)|(!IS_ADDRESS_POSTALCODE)`

Quando si usa il riconoscimento francese, il contesto risultante è il modello di lingua predefinito. Per evitare questo problema, rilevare la lingua del riconoscimento in uso e impostare gli ambiti di input di conseguenza.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Enumerazione InputScope](/windows/win32/api/inputscope/ne-inputscope-inputscope)
</dt> </dl>

 

