---
description: Gli sviluppatori che creano applicazioni per Tablet PC sono in grado di sfruttare l'ambito di input e le informazioni di contesto.
ms.assetid: 74e4e4b2-6ceb-4044-84df-2fff0788267a
title: Modalità d'uso del contesto da parte della piattaforma Tablet PC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c586bf3ffcff8fc92b02bc0b4f5aff79c6bd0bbd66e6f048eab35a78d3be9676
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709281"
---
# <a name="how-the-tablet-pc-platform-uses-context"></a>Modalità d'uso del contesto da parte della piattaforma Tablet PC

Gli sviluppatori che creano applicazioni per Tablet PC sono in grado di sfruttare l'ambito di input e le informazioni di contesto. Le migliori soluzioni possibili per l'impostazione delle informazioni di contesto sui controlli nelle applicazioni variano a seconda che il controllo sia abilitato per l'input penna e che l'applicazione sia stata rilasciata sul mercato. Un controllo abilitato per l'input penna è un controllo progettato specificamente per l'input penna e in cui i dati dell'input penna vengono principalmente raccolti e resi persistenti come input penna. Esempi di applicazioni abilitate per l'input penna sono Microsoft Windows Journal o un programma di sketching. In un controllo che non è abilitato per l'input penna, i dati di input vengono raccolti e resi persistenti come testo, in genere usando il Pannello di input di Tablet PC quando l'applicazione viene eseguita in un Tablet PC. Le soluzioni per abilitare le informazioni di contesto all'interno dei controlli sono:

-   API [SetInputScope:](/windows/win32/api/inputscope/nf-inputscope-setinputscope) soluzione a livello di codice di basso livello per applicazioni e controlli non abilitati per l'input penna. I file binari per l'applicazione sono influenzati e devono essere ridistribuiti.
-   Proprietà [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) e [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) dell'oggetto [**RecognizerContext:**](inkrecognizercontext-class.md) soluzione programmatica per le applicazioni con controlli abilitati per l'input penna. I file binari per l'applicazione sono influenzati e devono essere ridistribuiti.

Il pannello di input di Tablet PC è stato aggiornato a partire da Windows Vista per sfruttare le informazioni di contesto fornite quando si usano le API [SetInputScope.](/windows/win32/api/inputscope/nf-inputscope-setinputscope) La tabella seguente fornisce informazioni dettagliate sui motori di riconoscimento Microsoft che supportano gli ambiti di input. Una "X" nella riga per un ambito di input indica che il riconoscitore in tale colonna supporta l'ambito di input.



| Nome della proprietà                                     | Inglese (Stati Uniti) | Inglese (Regno Unito) | Tedesco       | Francese       | Giapponese     | Coreano       | Cinese (semplificato) | Cinese (tradizionale) |
|---------------------------------------------------|-------------------------|--------------------------|--------------|--------------|--------------|--------------|----------------------|-----------------------|
| **INDIRIZZO \_ \_ FULLPOSTALADDRESS**<br/>     | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **CODICE \_ \_ POSTALE DELL'INDIRIZZO**<br/>            | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ ADDRESS \_ STREET**<br/>                | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ ADDRESS \_ STATEORPROVINCE**<br/>       | X<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ ADDRESS \_ CITY**<br/>                  | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ ADDRESS \_ COUNTRYNAME**<br/>           | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ ADDRESS \_ COUNTRYSHORTNAME**<br/>      | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ CURRENCY \_ AMOUNTANDSYMBOL**<br/>      | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ CURRENCY \_ AMOUNT**<br/>               | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ DATE \_ FULLDATE**<br/>                 | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ DATE \_ MONTH**<br/>                    | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ DATE \_ DAY**<br/>                      | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ DATE \_ YEAR**<br/>                     | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ DATE \_ MONTHNAME**<br/>                | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ DATE \_ DAYNAME**<br/>                  | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **È \_ L'IMPOSTAZIONE PREDEFINITA**<br/>                        | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **NOME UTENTE \_ DI \_ POSTA ELETTRONICA**<br/>                | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ EMAIL \_ SMTPEMAILADDRESS**<br/>        | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **È \_ IL FILE \_ FULLFILEPATH**<br/>             | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **È IL \_ NOME FILE \_**<br/>                 | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ LOGINNAME**<br/>                      | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **CIFRE \_ IS**<br/>                         | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ NUMBER**<br/>                         | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **È \_ ONECHAR**<br/>                        | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **È \_ LA PASSWORD**<br/>                       | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **È \_ PERSONALNAME \_ FULLNAME**<br/>         | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **PREFISSO \_ \_ PERSONALNAME**<br/>           | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **È \_ PERSONALNAME \_ GIVENNAME**<br/>        | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **È \_ PERSONALNAME \_ MIDDLENAME**<br/>       | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **È \_ PERSONALNAME \_ SURNAME**<br/>          | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **\_SUFFISSO \_ PERSONALNAME**<br/>           | X<br/>            | -<br/>             | X<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **È \_ PHONE \_ FULLTELEPHONENUMBER**<br/> | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **È \_ IL CODICE PAESE DEL \_ TELEFONO**<br/>         | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **È \_ \_ L'AREACODE DEL TELEFONO**<br/>            | X<br/>            | X<br/>             | X<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **È \_ TELEPHONE \_ LOCALNUMBER**<br/>         | X<br/>            | X<br/>             | X<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **TEMPO \_ PIENO \_ TEMPO**<br/>                 | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ TIME \_ HOUR**<br/>                     | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **È \_ TEMPO \_ MINORSEC**<br/>                 | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ URL**<br/>                            | X<br/>            | X<br/>             | X<br/> | X<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ NUMBER \_ FULLWIDTH**<br/>              | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ ALPHANUMERIC \_ HALFWIDTH**<br/>        | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **È \_ \_ FULLWIDTH ALFANUMERICO**<br/>        | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ CURRENCY \_ CHINESE**<br/>              | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ BOPOMOFO**<br/>                       | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ HIRAGANA**<br/>                       | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **È \_ KATAKANA \_ HALFWIDTH**<br/>            | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **È \_ KATAKANA \_ FULLWIDTH**<br/>            | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |
| **IS \_ HANJA**<br/>                          | -<br/>            | -<br/>             | -<br/> | -<br/> | -<br/> | -<br/> | -<br/>         | -<br/>          |



 

Quando si usano le API [SetInputScope](/windows/win32/api/inputscope/nf-inputscope-setinputscope) o la proprietà [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) dell'oggetto [**RecognizerContext**](inkrecognizercontext-class.md) per impostare il contesto, il tentativo di impostare un ambito di input per una lingua non supportata dal riconoscimento di tale lingua fa sì che il pannello di input di Tablet PC usi il modello linguistico predefinito come contesto per il controllo. Ad esempio, **l'ambito di input IS ADDRESS \_ \_ STATEORPROVINCE** non è supportato dal riconoscimento francese. Se si imposta il contesto in un campo come

`(!IS_ADDRESS_STATEORPROVINCE)|(!IS_ADDRESS_POSTALCODE)`

Quando si usa il riconoscimento francese, il contesto risultante è il modello linguistico predefinito. Per evitare questo problema, rilevare la lingua del sistema di riconoscimento in uso e impostare gli ambiti di input di conseguenza.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Enumerazione InputScope](/windows/win32/api/inputscope/ne-inputscope-inputscope)
</dt> </dl>

 

