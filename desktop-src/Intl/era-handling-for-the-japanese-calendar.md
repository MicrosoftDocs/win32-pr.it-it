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
# <a name="era-handling-for-the-japanese-calendar"></a><span data-ttu-id="e4ce5-103">Gestione delle ere per il calendario giapponese</span><span class="sxs-lookup"><span data-stu-id="e4ce5-103">Era Handling for the Japanese Calendar</span></span>

<span data-ttu-id="e4ce5-104">Molti calendari hanno ere, ad esempio AD/BC o CE/BCE.</span><span class="sxs-lookup"><span data-stu-id="e4ce5-104">Many calendars have eras, such as AD/BC or CE/BCE.</span></span> <span data-ttu-id="e4ce5-105">Nel calendario giapponese gli anni sono descritti da nengō, una combinazione di numero di anno e nome dell'era.</span><span class="sxs-lookup"><span data-stu-id="e4ce5-105">In the Japanese Calendar, years are described by nengō, a combination of the year number and era name.</span></span> <span data-ttu-id="e4ce5-106">Ad esempio, 2009 è Heisei 21.</span><span class="sxs-lookup"><span data-stu-id="e4ce5-106">For example, 2009 is Heisei 21.</span></span> <span data-ttu-id="e4ce5-107">In passato, i nomi delle epoche giapponesi venivano modificati di frequente, ma ora le modifiche giapponesi cambiano solo in seguito alla successione Imperial.</span><span class="sxs-lookup"><span data-stu-id="e4ce5-107">In the past, Japanese era names changed frequently, but now the Japanese eras change only on imperial succession.</span></span> <span data-ttu-id="e4ce5-108">Windows e Microsoft .NET hanno supportato in passato le quattro epoche moderne in questo criterio: Meiji, Taishō, Shōwa e Heisei.</span><span class="sxs-lookup"><span data-stu-id="e4ce5-108">Windows and Microsoft .NET have historically supported the four modern eras under this policy: Meiji, Taishō, Shōwa and Heisei.</span></span>

<span data-ttu-id="e4ce5-109">Con Windows 7, Windows Server 2008 R2 e il .NET Framework 4, Microsoft riconosce che è possibile aggiungere altre ere in futuro.</span><span class="sxs-lookup"><span data-stu-id="e4ce5-109">With Windows 7, Windows Server 2008 R2, and the .NET Framework 4, Microsoft recognizes that additional eras may be added in the future.</span></span> <span data-ttu-id="e4ce5-110">In queste versioni di Windows i dati dell'era vengono archiviati nel registro di sistema sotto la chiave:</span><span class="sxs-lookup"><span data-stu-id="e4ce5-110">On these versions of Windows the era data is stored in the registry under the key:</span></span><dl> <span data-ttu-id="e4ce5-111">HKEY \_ Local \_ Machine \\ System \\ CurrentControlSet \\ controllo \\ NLS \\ calendari \\ giapponese \\</span><span class="sxs-lookup"><span data-stu-id="e4ce5-111">HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentControlSet\\Control\\Nls\\Calendars\\Japanese\\Eras</span></span>  
</dl>

<span data-ttu-id="e4ce5-112">Se necessario, è possibile aggiungere altre ere a tale chiave tramite il normale processo di Windows Update.</span><span class="sxs-lookup"><span data-stu-id="e4ce5-112">If necessary, additional eras can be added to that key through the normal Windows Update process.</span></span> <span data-ttu-id="e4ce5-113">Questa chiave può essere visualizzata tramite l'editor del registro di sistema (Regedit.exe).</span><span class="sxs-lookup"><span data-stu-id="e4ce5-113">This key can be viewed using the registry editor (Regedit.exe).</span></span> <span data-ttu-id="e4ce5-114">Di seguito è riportato un esempio della chiave e dei valori forniti in Windows 7:</span><span class="sxs-lookup"><span data-stu-id="e4ce5-114">An example of the key and values shipped in Windows 7 is:</span></span>

``` syntax
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Nls\Calendars\Japanese\Eras]
"1868 01 01"="明治_明_Meiji_M"
"1912 07 30"="大正_大_Taisho_T"
"1926 12 25"="昭和_昭_Showa_S"
"1989 01 08"="平成_平_Heisei_H"
```

<span data-ttu-id="e4ce5-115">Il nome di ogni valore era la data in cui l'era inizia nel calendario gregoriano.</span><span class="sxs-lookup"><span data-stu-id="e4ce5-115">The name of each era value is the date the era begins in the Gregorian calendar.</span></span> <span data-ttu-id="e4ce5-116">Il valore contiene il nome dell'era in giapponese, il nome abbreviato in giapponese, il nome in inglese e un nome abbreviato in inglese:</span><span class="sxs-lookup"><span data-stu-id="e4ce5-116">The value contains the era name in Japanese, the abbreviated name in Japanese, the name in English, and an abbreviated name in English:</span></span><dl> <span data-ttu-id="e4ce5-117">"AAAA MM GG" = "JE \_ AJE \_ EE \_ AEE"</span><span class="sxs-lookup"><span data-stu-id="e4ce5-117">"YYYY MM DD"="JE\_AJE\_EE\_AEE"</span></span>  
</dl>where

-   <span data-ttu-id="e4ce5-118">"AAAA MM GG" è la data gregoriano dell'inizio dell'era nel formato anno, mese, giorno in cui anno è 4 cifre, il giorno è 2 cifre e il mese è anche 2 cifre.</span><span class="sxs-lookup"><span data-stu-id="e4ce5-118">"YYYY MM DD" is the Gregorian date of the start of the era in year, month, day form where year is 4 digits, day is 2 digits and month is also 2 digits.</span></span> <span data-ttu-id="e4ce5-119">Uno spazio separa ogni parte della data.</span><span class="sxs-lookup"><span data-stu-id="e4ce5-119">A space separates each part of the date.</span></span>
-   <span data-ttu-id="e4ce5-120">"JE" è il nome giapponese dell'era ed è seguito da un carattere di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="e4ce5-120">"JE" is the Japanese name of the era, and is followed by an underscore.</span></span>
-   <span data-ttu-id="e4ce5-121">"AJE" è il nome abbreviato dell'era, in giapponese, ed è seguito da un carattere di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="e4ce5-121">"AJE" is the abbreviated name of the era, in Japanese, and is followed by an underscore.</span></span>
-   <span data-ttu-id="e4ce5-122">"EE" è il nome inglese dell'era giapponese ed è seguito da un carattere di sottolineatura.</span><span class="sxs-lookup"><span data-stu-id="e4ce5-122">"EE" is the English name of the Japanese era, and is followed by an underscore.</span></span>
-   <span data-ttu-id="e4ce5-123">"AEE" è il nome in inglese abbreviato dell'era giapponese.</span><span class="sxs-lookup"><span data-stu-id="e4ce5-123">"AEE" is the abbreviated English name of the Japanese era.</span></span>

<span data-ttu-id="e4ce5-124">Una considerazione per gli sviluppatori di applicazioni è la possibilità che altre ere vengano aggiunte da Windows Update o altri mezzi.</span><span class="sxs-lookup"><span data-stu-id="e4ce5-124">One consideration for application developers is the possibility that additional eras will be added by Windows Update or other means.</span></span> <span data-ttu-id="e4ce5-125">In tal caso, è possibile che l'applicazione riscontri più di quattro ere previste per il calendario giapponese.</span><span class="sxs-lookup"><span data-stu-id="e4ce5-125">In that case the application may encounter more than the expected four eras for the Japanese calendar.</span></span> <span data-ttu-id="e4ce5-126">A scopo di test, i tester possono aggiungere un'altra era al registro di sistema; Tuttavia, deve essere limitato solo ai computer di test, in quanto influisca sul comportamento dell'intero computer.</span><span class="sxs-lookup"><span data-stu-id="e4ce5-126">For testing purposes testers may add an additional era to the registry; however, that should be restricted to test machines only, as it impacts the behavior of the entire machine.</span></span>

<span data-ttu-id="e4ce5-127">Di seguito è riportato un esempio di chiave che può essere usata per il test.</span><span class="sxs-lookup"><span data-stu-id="e4ce5-127">An example of such a key that could be used for test follows.</span></span> <span data-ttu-id="e4ce5-128">Questa modifica può essere apportata con l'editor del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="e4ce5-128">This change can be made with the registry editor.</span></span> <span data-ttu-id="e4ce5-129">(Questo è un esempio solo per l'utilizzo dei test e non è progettato per prevedere eventuali aggiunte future).</span><span class="sxs-lookup"><span data-stu-id="e4ce5-129">(This is an example for test use only, and is not intended to predict any future additions.)</span></span>

``` syntax
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Nls\Calendars\Japanese\Eras]
"2020 09 01"="仮名_仮_Test Era_X"
```

<span data-ttu-id="e4ce5-130">Si noti che questo influisca solo sui computer che eseguono Windows 7 e versioni successive o .NET Framework 4 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="e4ce5-130">Note that this only impacts machines running Windows 7 and later or .NET Framework 4 and later.</span></span> <span data-ttu-id="e4ce5-131">Gli sviluppatori di applicazioni sono invitati a testare le proprie applicazioni con altre ere di test aggiuntive per garantire che le applicazioni continuino a funzionare se in una data futura verranno aggiunte altre ere.</span><span class="sxs-lookup"><span data-stu-id="e4ce5-131">Application developers are encouraged to test their applications with such additional test eras to ensure that their applications will continue to work if additional eras are added at some future date.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e4ce5-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e4ce5-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4ce5-133">Recupero di informazioni su data e ora</span><span class="sxs-lookup"><span data-stu-id="e4ce5-133">Retrieving Time and Date Information</span></span>](retrieving-time-and-date-information.md)
</dt> <dt>

[<span data-ttu-id="e4ce5-134">Identificatori del calendario</span><span class="sxs-lookup"><span data-stu-id="e4ce5-134">Calendar Identifiers</span></span>](calendar-identifiers.md)
</dt> </dl>

 

 



