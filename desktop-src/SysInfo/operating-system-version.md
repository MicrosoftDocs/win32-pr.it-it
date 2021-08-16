---
description: Le funzioni dell'helper API versione vengono usate per determinare la versione del sistema operativo attualmente in esecuzione. Per altre informazioni, vedere Recupero della versione del sistema.
ms.assetid: 1a70b1d9-ed66-4201-9921-4e26e4001020
title: Versione del sistema operativo
ms.topic: article
ms.date: 09/15/2020
ms.openlocfilehash: ae90f4eac5546fccd7513d781234896fbbbda93ff3723a9ac1db438321ecf214
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117763953"
---
# <a name="operating-system-version"></a>Versione del sistema operativo

Le [funzioni dell'helper API](version-helper-apis.md) versione vengono usate per determinare la versione del sistema operativo attualmente in esecuzione. Per altre informazioni, vedere [Recupero della versione del sistema.](getting-the-system-version.md)

Nella tabella seguente sono riepilogati i numeri di versione del sistema operativo più recenti.

| Sistema operativo | Numero di versione |
|------------------|----------------|
| Windows 10       | 10.0\*         |
| Windows Server 2019 | 10.0\*      |
| Windows Server 2016 | 10.0\*      |
| Windows 8.1      | 6.3\*          |
| R2 per Windows Server 2012 | 6.3\*    |
| Windows 8        | 6.2            |
| Windows Server 2012 | 6.2         |
| Windows 7        | 6.1            |
| Windows Server 2008 R2 | 6.1      |
| Windows Server 2008 | 6.0         |
| Windows Vista    | 6.0            |
| Windows Server 2003 R2 | 5,2      |
| Windows Server 2003 | 5,2         |
| Windows XP 64-Bit Edition | 5,2   |
| Windows XP | 5.1                  |
| Windows 2000     | 5.0            |

**\*** Per le applicazioni che sono state manifeste per Windows 8.1 o Windows 10. Le applicazioni non manifeste per Windows 8.1 o Windows 10 restituiranno il valore Windows 8 versione del sistema operativo (6.2). Per manifestare le applicazioni per Windows 8.1 o Windows 10, vedere Definizione della destinazione [dell'applicazione per Windows](targeting-your-application-at-windows-8-1.md).<br/>

L'identificazione del sistema operativo corrente non è in genere il modo migliore per determinare se è presente una particolare funzionalità del sistema operativo. Ciò è dovuto al fatto che nel sistema operativo potrebbero essere state aggiunte nuove funzionalità in una DLL ridistribuibile. Anziché usare le funzioni [dell'helper API versione](version-helper-apis.md) per determinare la piattaforma o il numero di versione del sistema operativo, verificare la presenza della funzionalità stessa.

Per determinare il modo migliore per testare una funzionalità, vedere la documentazione relativa alla funzionalità di interesse. L'elenco seguente illustra alcune tecniche comuni per il rilevamento delle funzionalità:

- È possibile verificare la presenza delle funzioni associate a una funzionalità. Per verificare la presenza di una funzione in una DLL di sistema, chiamare la [**funzione LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) per caricare la DLL. Chiamare quindi la [**funzione GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) per determinare se la funzione di interesse è presente nella DLL. Usare il puntatore restituito **da GetProcAddress** per chiamare la funzione. Si noti che anche se la funzione è presente, potrebbe essere uno stub che restituisce semplicemente un codice di errore, ad esempio ERROR \_ CALL \_ NOT \_ IMPLEMENTED.
- È possibile determinare la presenza di alcune funzionalità usando la [**funzione GetSystemMetrics.**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) Ad esempio, è possibile rilevare più monitor di visualizzazione chiamando **GetSystemMetrics**(SM \_ CMONITORS).
- Esistono diverse versioni delle DLL ridistribuibili che implementano funzionalità comuni di controllo e shell. Per informazioni su come determinare le versioni presenti nel sistema in cui è in esecuzione l'applicazione, vedere l'argomento [Versioni della shell e dei controlli comuni](/previous-versions/windows/desktop/legacy/bb776779(v=vs.85)).

Se è necessario un sistema operativo specifico, assicurarsi di usarlo come versione minima supportata, anziché progettare il test per il sistema operativo. In questo modo, il codice di rilevamento continuerà a funzionare nelle versioni future di Windows.

Si noti che un'applicazione a 32 bit può rilevare se è in esecuzione in WOW64 chiamando la [**funzione IsWow64Process.**](/windows/desktop/api/wow64apiset/nf-wow64apiset-iswow64process) Può ottenere informazioni aggiuntive sul processore chiamando la [**funzione GetNativeSystemInfo.**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getnativesysteminfo)

Per altre informazioni, vedere [l'Windows 10 sulla versione e la](/windows/release-information/) scheda Windows del ciclo di [vita.](https://support.microsoft.com/help/13853/windows-lifecycle-fact-sheet)

