---
description: Gestione delle ere per il calendario giapponese
ms.assetid: a1dabf7c-6521-492e-bdc0-27cfb07cfc20
title: Gestione delle ere per il calendario giapponese
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6ba9c8957bc37a3e200aad546d04629b049dfb3a7962f73d463358d879fb718
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118949420"
---
# <a name="era-handling-for-the-japanese-calendar"></a>Gestione delle ere per il calendario giapponese

Molti calendari hanno ere, ad esempio AD/BC o CE/BCE. Nel calendario giapponese gli anni sono descritti da nengoso, una combinazione del numero dell'anno e del nome dell'era. Ad esempio, 2009 è Heisei 21. In passato, i nomi dell'era giapponese cambiarono spesso, ma ora le ere giapponesi cambiano solo per la successione imperiale. Windows e Microsoft .NET hanno supportato le quattro ere moderne in base a questo criterio: Meiji, Taishoso, Shosowa ed Heisei.

Con Windows 7, Windows Server 2008 R2 e .NET Framework 4, Microsoft riconosce che potrebbero essere aggiunte ere aggiuntive in futuro. In queste versioni di Windows i dati dell'era vengono archiviati nel Registro di sistema sotto la chiave :<dl> HKEY \_ LOCAL \_ MACHINE \\ SYSTEM \\ CurrentControlSet \\ Control \\ Nls \\ Calendars \\ Japanese \\ Eras  
</dl>

Se necessario, è possibile aggiungere ere aggiuntive a tale chiave tramite il normale Windows di aggiornamento. Questa chiave può essere visualizzata usando l'editor del Registro di sistema (Regedit.exe). Un esempio della chiave e dei valori forniti in Windows 7 è:

``` syntax
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Nls\Calendars\Japanese\Eras]
"1868 01 01"="明治_明_Meiji_M"
"1912 07 30"="大正_大_Taisho_T"
"1926 12 25"="昭和_昭_Showa_S"
"1989 01 08"="平成_平_Heisei_H"
```

Il nome di ogni valore di era è la data di inizio dell'era nel calendario gregoriano. Il valore contiene il nome dell'era in giapponese, il nome abbreviato in giapponese, il nome in inglese e un nome abbreviato in inglese:<dl> "AAAAA MM GG"="JE \_ AJE \_ edizione Enterprise \_ AEE"  
</dl>where

-   "AAAA MM GG" è la data gregoriana dell'inizio dell'era nel formato anno, mese, giorno in cui anno è 4 cifre, giorno è 2 cifre e mese è anche 2 cifre. Uno spazio separa ogni parte della data.
-   "JE" è il nome giapponese dell'era ed è seguito da un carattere di sottolineatura.
-   "AJE" è il nome abbreviato dell'era, in giapponese, seguito da un carattere di sottolineatura.
-   "edizione Enterprise" è il nome inglese dell'era giapponese ed è seguito da un carattere di sottolineatura.
-   "AEE" è il nome inglese abbreviato dell'era giapponese.

Una considerazione per gli sviluppatori di applicazioni è la possibilità che ere aggiuntive verranno aggiunte Windows Update o altri mezzi. In tal caso, l'applicazione potrebbe riscontrare più delle quattro ere previste per il calendario giapponese. A scopo di test, i tester possono aggiungere un'era aggiuntiva al Registro di sistema. Tuttavia, questo dovrebbe essere limitato solo ai computer di test, in quanto influisce sul comportamento dell'intero computer.

Di seguito è riportato un esempio di tale chiave che può essere usata per il test. Questa modifica può essere apportata con l'editor del Registro di sistema. Si tratta di un esempio solo per l'uso di test e non è destinato a prevedere aggiunte future.

``` syntax
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Nls\Calendars\Japanese\Eras]
"2020 09 01"="仮名_仮_Test Era_X"
```

Si noti che ciò influisce solo sui computer che eseguono Windows 7 e versioni successive o .NET Framework 4 e versioni successive. Gli sviluppatori di applicazioni sono invitati a testare le proprie applicazioni con ere di test aggiuntive per garantire che le applicazioni continuino a funzionare se altre ere vengono aggiunte in una data futura.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Recupero di informazioni su ora e data](retrieving-time-and-date-information.md)
</dt> <dt>

[Identificatori di calendario](calendar-identifiers.md)
</dt> </dl>

 

 



