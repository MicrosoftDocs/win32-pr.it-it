---
description: Le funzioni helper dell'API Version vengono usate per determinare la versione del sistema operativo attualmente in esecuzione. Per ulteriori informazioni, vedere recupero della versione del sistema.
ms.assetid: 1a70b1d9-ed66-4201-9921-4e26e4001020
title: Versione del sistema operativo
ms.topic: article
ms.date: 09/15/2020
ms.openlocfilehash: 73eb9a81880f29f9292713af46c5c79a7e9eb2de
ms.sourcegitcommit: 7ea69db68bca2b1592802e676ada8432a2583410
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/17/2020
ms.locfileid: "104047543"
---
# <a name="operating-system-version"></a>Versione del sistema operativo

Le [funzioni helper dell'API Version](version-helper-apis.md) vengono usate per determinare la versione del sistema operativo attualmente in esecuzione. Per ulteriori informazioni, vedere [recupero della versione del sistema](getting-the-system-version.md).

Nella tabella seguente sono riepilogati i numeri di versione del sistema operativo più recenti.

| Sistema operativo | Numero di versione |
|------------------|----------------|
| Windows 10       | 10,0\*         |
| Windows Server 2019 | 10,0\*      |
| Windows Server 2016 | 10,0\*      |
| Windows 8.1      | 6.3\*          |
| Windows Server 2012 R2 | 6.3\*    |
| Windows 8        | 6.2            |
| Windows Server 2012 | 6.2         |
| Windows 7        | 6.1            |
| Windows Server 2008 R2 | 6.1      |
| Windows Server 2008 | 6.0         |
| Windows Vista    | 6.0            |
| Windows Server 2003 R2 | 5,2      |
| Windows Server 2003 | 5,2         |
| Windows XP 64-bit Edition | 5,2   |
| Windows XP | 5.1                  |
| Windows 2000     | 5.0            |

**\*** Per le applicazioni che sono state manifestate per Windows 8.1 o Windows 10. Le applicazioni non manifestate per Windows 8.1 o Windows 10 restituiranno il valore della versione del sistema operativo Windows 8 (6,2). Per manifestare le applicazioni per Windows 8.1 o Windows 10, fare riferimento all' [applicazione per Windows](targeting-your-application-at-windows-8-1.md).<br/>

L'identificazione del sistema operativo corrente non è in genere il modo migliore per determinare se è presente una particolare funzionalità del sistema operativo. Ciò è dovuto al fatto che è possibile che nel sistema operativo siano state aggiunte nuove funzionalità in una DLL ridistribuibile. Invece di usare le [funzioni Helper API versione](version-helper-apis.md) per determinare la piattaforma del sistema operativo o il numero di versione, verificare la presenza della funzionalità stessa.

Per determinare il modo migliore per verificare la presenza di una funzionalità, vedere la documentazione relativa alla funzionalità di interesse. Nell'elenco seguente vengono illustrate alcune tecniche comuni per il rilevamento delle funzionalità:

- È possibile verificare la presenza delle funzioni associate a una funzionalità. Per verificare la presenza di una funzione in una DLL di sistema, chiamare la funzione [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) per caricare la dll. Chiamare quindi la funzione [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per determinare se la funzione di interesse è presente nella dll. Usare il puntatore restituito da **GetProcAddress** per chiamare la funzione. Si noti che anche se la funzione è presente, può essere uno stub che restituisce solo un codice di errore, ad esempio una chiamata di errore \_ \_ non \_ implementata.
- Per determinare la presenza di alcune funzionalità, è possibile usare la funzione [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) . È ad esempio possibile rilevare più monitor di visualizzazione chiamando **GetSystemMetrics**(SM \_ CMONITORS).
- Sono disponibili diverse versioni delle DLL ridistribuibili che implementano la shell e le funzionalità di controllo comuni. Per informazioni sulla determinazione delle versioni presenti nel sistema in cui è in esecuzione l'applicazione, vedere l'argomento [Shell e le versioni dei controlli comuni](/previous-versions/windows/desktop/legacy/bb776779(v=vs.85)).

Se è necessario richiedere un particolare sistema operativo, assicurarsi di utilizzarlo come versione minima supportata, anziché progettare il test per il sistema operativo. In questo modo, il codice di rilevamento continuerà a funzionare nelle versioni future di Windows.

Si noti che un'applicazione a 32 bit può rilevare se è in esecuzione in WOW64 chiamando la funzione [**IsWow64Process**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process) . Può ottenere informazioni aggiuntive sul processore chiamando la funzione [**GetNativeSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo) .

Per altre informazioni, vedere [informazioni sulla versione di Windows 10](/windows/release-information/) e [foglio dei fatti di Windows Lifecycle](https://support.microsoft.com/help/13853/windows-lifecycle-fact-sheet).

