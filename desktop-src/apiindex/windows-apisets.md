---
description: I set di API sono gruppi funzionali di API Win32 nel sistema operativo di base. Forniscono una separazione architettonica dalla DLL host in cui è definita una determinata API Win32 e dal gruppo funzionale a cui appartiene l'API.
title: Set di API Windows
ms.topic: article
ms.date: 10/14/2020
ms.openlocfilehash: 15c8e6ad8124abf06e6ab3c2a8ca2bcd83772855
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/18/2020
ms.locfileid: "104474723"
---
# <a name="windows-api-sets"></a>Set di API Windows

Tutte le versioni di Windows 10 condividono una base comune di componenti del sistema operativo denominati *sistema operativo* di base (in alcuni contesti questa base comune è chiamata anche *OneCore*). Nei componenti del sistema operativo di base, le API Win32 sono organizzate in gruppi funzionali denominati *set di API*.

Lo scopo di un set di API è fornire una separazione architettonica dalla DLL host in cui è implementata un'API Win32 specifica e dal contratto funzionale a cui appartiene l'API. Il disaccoppiamento che i set di API forniscono tra implementazione e contratti offre molti vantaggi tecnici per gli sviluppatori. In particolare, l'uso di set di API nel codice può migliorare la compatibilità con tutti i dispositivi Windows 10.

I set di API risolvono specificamente gli scenari seguenti:

- Sebbene la vasta gamma di API Win32 sia supportata nei PC, solo un subset dell'API Win32 è disponibile in altri dispositivi Windows 10, ad esempio HoloLens, Xbox e altri dispositivi che eseguono Windows 10. Il nome del set di API fornisce un meccanismo di query per rilevare in modo corretto se un'API è disponibile in un determinato dispositivo.

- Alcune implementazioni di API Win32 sono presenti in dll con nomi diversi in diversi dispositivi Windows 10. L'uso di nomi di set di API invece dei nomi di DLL quando si rileva la disponibilità delle API e le API per il caricamento ritardato forniscono una route corretta all'implementazione indipendentemente da dove è effettivamente implementata l'API.

Per altri dettagli, vedere [operazione del caricatore del set di API](api-set-loader-operation.md) e [rilevare la disponibilità dei set di API](detect-api-set-availability.md).

## <a name="linking-to-umbrella-libraries"></a>Collegamento a librerie Umbrella

Per semplificare la limitazione del codice alle API Win32 supportate nel sistema operativo di base, viene fornita una serie di *librerie Umbrella*. Ad esempio, una libreria Umbrella denominata OneCore. lib fornisce le esportazioni per il subset di API Win32 comuni a tutti i dispositivi Windows 10.

Le API in una libreria Umbrella possono essere implementate in un'ampia gamma di moduli. La libreria Umbrella estrae questi dettagli, rendendo il codice più portabile tra le versioni e i dispositivi di Windows 10. Anziché collegarsi a librerie come Kernel32. lib e Advapi32. lib, è sufficiente collegare l'app desktop o il driver alla libreria Umbrella che contiene il set di API del sistema operativo di base a cui si è interessati.

Per ulteriori informazioni, vedere [Windows Umbrella Libraries](windows-umbrella-libraries.md).

## <a name="api-set-contract-names"></a>Nomi di contratto di set di API

I set di API sono identificati da un nome di contratto sicuro che segue le convenzioni standard riconosciute dal caricatore della libreria. 

- Il nome deve iniziare con l' **API** stringa o **ext-**. 
    - I nomi che iniziano con **API** rappresentano le API che possono esistere in tutte le versioni di Windows 10.
    - I nomi che iniziano con **ext** rappresentano le API che potrebbero non esistere in tutte le versioni di Windows 10.
- Il nome deve terminare con la sequenza **l \<n\> - \<n\> - \<n\>**, dove **n** è costituito da cifre decimali.
- Il corpo del nome può essere costituito da caratteri alfanumerici o trattini ( **-** ).
- Per il nome non viene fatta distinzione tra maiuscole e minuscole.

Di seguito sono riportati alcuni esempi di nomi di contratto di set di API:

- **API-MS-Win-Core-UMS-L1-1-0**
- **EXT-MS-Win-com-Ole32-L1-1-5**
- **EXT-MS-Win-Ntuser-Window-L1-1-0**
- **EXT-MS-Win-Ntuser-Window-L1-1-1**

È possibile usare un nome di set di API nel contesto di un'operazione del caricatore, ad esempio [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [P/Invoke](/dotnet/standard/native-interop/pinvoke) anziché un nome di modulo dll, per garantire una route corretta all'implementazione indipendentemente dal punto in cui l'API è effettivamente implementata nel dispositivo corrente. Tuttavia, quando si esegue questa operazione, è necessario aggiungere la stringa **. dll** alla fine del nome del contratto. Si tratta di un requisito per il corretto funzionamento del caricatore, che non viene considerato effettivamente una parte del nome del contratto. Sebbene i nomi di contratto risultino simili ai nomi di DLL in questo contesto, sono fondamentalmente diversi dai nomi dei moduli DLL e non fanno direttamente riferimento a un file su disco.

Ad eccezione dell'accodamento di String **. dll** nelle operazioni del caricatore, i nomi dei contratti di set di API devono essere considerati un identificatore non modificabile corrispondente a una versione del contratto specifica.

## <a name="identifying-api-sets-for-win32-apis"></a>Identificazione dei set di API per le API Win32

Per determinare se una particolare API Win32 appartiene a un set di API, esaminare la tabella dei requisiti nella documentazione di riferimento per l'API. Se l'API appartiene a un set di API, nella tabella dei requisiti dell'articolo sono elencati il nome del set di API e la versione di Windows in cui l'API è stata introdotta per la prima volta nel set di API. Per esempi di API che appartengono a un set di API, vedere questi articoli:

- [AllowSetForegroundWindow](/windows/win32/api/winuser/nf-winuser-allowsetforegroundwindow)
- [FindWindowsEx](/windows/win32/api/winuser/nf-winuser-findwindowexa)
- [GetClassFile](/windows/win32/api/objbase/nf-objbase-getclassfile)

## <a name="in-this-section"></a>Contenuto della sezione

* [Funzionamento del caricatore dei set di API](api-set-loader-operation.md)
* [Rilevare la disponibilità di un set di API](detect-api-set-availability.md)
* [Librerie generiche di Windows](windows-umbrella-libraries.md)