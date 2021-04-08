---
description: Gestione delle ere per il calendario giapponese
ms.assetid: a1dabf7c-6521-492e-bdc0-27cfb07cfc20
title: Gestione delle ere per il calendario giapponese
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eba757745bf0d90d119c821772c7fc23f3f8694b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884570"
---
# <a name="era-handling-for-the-japanese-calendar"></a>Gestione delle ere per il calendario giapponese

Molti calendari hanno ere, ad esempio AD/BC o CE/BCE. Nel calendario giapponese gli anni sono descritti da nengō, una combinazione di numero di anno e nome dell'era. Ad esempio, 2009 è Heisei 21. In passato, i nomi delle epoche giapponesi venivano modificati di frequente, ma ora le modifiche giapponesi cambiano solo in seguito alla successione Imperial. Windows e Microsoft .NET hanno supportato in passato le quattro epoche moderne in questo criterio: Meiji, Taishō, Shōwa e Heisei.

Con Windows 7, Windows Server 2008 R2 e il .NET Framework 4, Microsoft riconosce che è possibile aggiungere altre ere in futuro. In queste versioni di Windows i dati dell'era vengono archiviati nel registro di sistema sotto la chiave:<dl> HKEY \_ Local \_ Machine \\ System \\ CurrentControlSet \\ controllo \\ NLS \\ calendari \\ giapponese \\  
</dl>

Se necessario, è possibile aggiungere altre ere a tale chiave tramite il normale processo di Windows Update. Questa chiave può essere visualizzata tramite l'editor del registro di sistema (Regedit.exe). Di seguito è riportato un esempio della chiave e dei valori forniti in Windows 7:

``` syntax
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Nls\Calendars\Japanese\Eras]
"1868 01 01"="明治_明_Meiji_M"
"1912 07 30"="大正_大_Taisho_T"
"1926 12 25"="昭和_昭_Showa_S"
"1989 01 08"="平成_平_Heisei_H"
```

Il nome di ogni valore era la data in cui l'era inizia nel calendario gregoriano. Il valore contiene il nome dell'era in giapponese, il nome abbreviato in giapponese, il nome in inglese e un nome abbreviato in inglese:<dl> "AAAA MM GG" = "JE \_ AJE \_ EE \_ AEE"  
</dl>where

-   "AAAA MM GG" è la data gregoriano dell'inizio dell'era nel formato anno, mese, giorno in cui anno è 4 cifre, il giorno è 2 cifre e il mese è anche 2 cifre. Uno spazio separa ogni parte della data.
-   "JE" è il nome giapponese dell'era ed è seguito da un carattere di sottolineatura.
-   "AJE" è il nome abbreviato dell'era, in giapponese, ed è seguito da un carattere di sottolineatura.
-   "EE" è il nome inglese dell'era giapponese ed è seguito da un carattere di sottolineatura.
-   "AEE" è il nome in inglese abbreviato dell'era giapponese.

Una considerazione per gli sviluppatori di applicazioni è la possibilità che altre ere vengano aggiunte da Windows Update o altri mezzi. In tal caso, è possibile che l'applicazione riscontri più di quattro ere previste per il calendario giapponese. A scopo di test, i tester possono aggiungere un'altra era al registro di sistema; Tuttavia, deve essere limitato solo ai computer di test, in quanto influisca sul comportamento dell'intero computer.

Di seguito è riportato un esempio di chiave che può essere usata per il test. Questa modifica può essere apportata con l'editor del registro di sistema. (Questo è un esempio solo per l'utilizzo dei test e non è progettato per prevedere eventuali aggiunte future).

``` syntax
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Nls\Calendars\Japanese\Eras]
"2020 09 01"="仮名_仮_Test Era_X"
```

Si noti che questo influisca solo sui computer che eseguono Windows 7 e versioni successive o .NET Framework 4 e versioni successive. Gli sviluppatori di applicazioni sono invitati a testare le proprie applicazioni con altre ere di test aggiuntive per garantire che le applicazioni continuino a funzionare se in una data futura verranno aggiunte altre ere.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Recupero di informazioni su data e ora](retrieving-time-and-date-information.md)
</dt> <dt>

[Identificatori del calendario](calendar-identifiers.md)
</dt> </dl>

 

 



