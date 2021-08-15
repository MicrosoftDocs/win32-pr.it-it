---
description: I set di API sono gruppi funzionali di API Win32 nel sistema operativo principale. Forniscono una separazione dell'architettura dalla DLL host in cui viene definita una determinata API Win32 e dal gruppo funzionale a cui appartiene l'API.
title: Windows Set di API
ms.topic: article
ms.date: 10/14/2020
ms.openlocfilehash: 34724f255b963c23406ed5bdc59de0278e68a6f75de0d00b4d45aa449575af89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117737608"
---
# <a name="windows-api-sets"></a>Windows Set di API

Tutte le versioni di Windows 10 condividono una base comune di componenti del sistema operativo denominata sistema operativo di base *(in* alcuni contesti questa base comune è detta *anche OneCore*). Nei componenti principali del sistema operativo le API Win32 sono organizzate in gruppi funzionali denominati *set di API.*

Lo scopo di un set di API è fornire una separazione dell'architettura dalla DLL host in cui viene implementata una determinata API Win32 e dal contratto funzionale a cui appartiene l'API. La separazione offerta da set di API tra implementazione e contratti offre molti vantaggi di progettazione per gli sviluppatori. In particolare, l'uso di set di API nel codice può migliorare la compatibilità con tutti Windows 10 dispositivi.

I set di API riguardano in modo specifico gli scenari seguenti:

- Anche se l'intera gamma dell'API Win32 è supportata nei PC, solo un subset dell'API Win32 è disponibile in altri dispositivi Windows 10 come HoloLens, Xbox e altri dispositivi che eseguono Windows 10x. Il nome del set di API fornisce un meccanismo di query per rilevare in modo pulito se un'API è disponibile in un determinato dispositivo.

- Alcune implementazioni dell'API Win32 esistono in DLL con nomi diversi in Windows 10 dispositivi. L'uso di nomi di set di API anziché di nomi di DLL durante il rilevamento della disponibilità dell'API e il caricamento ritardato delle API forniscono una route corretta all'implementazione, indipendentemente dalla posizione in cui l'API viene effettivamente implementata.

Per altri dettagli, vedere [Api set loader operation (Operazione del caricatore del set di API)](api-set-loader-operation.md) e [Detect API set availability (Rilevare la disponibilità del set di API).](detect-api-set-availability.md)

## <a name="linking-to-umbrella-libraries"></a>Collegamento a librerie generico

Per semplificare la limitazione del codice alle API Win32 supportate nel sistema operativo di base, sono disponibili una serie di librerie *generico.* Ad esempio, una libreria generico denominata OneCore.lib fornisce le esportazioni per il subset di API Win32 comuni a tutti Windows 10 dispositivi.

Le API in una libreria generico possono essere implementate in una gamma di moduli. La libreria generico estrae questi dettagli dall'utente, rendendo il codice più portabile Windows 10 versioni e dispositivi. Invece di collegarsi a librerie come kernel32.lib e advapi32.lib, è sufficiente collegare l'app desktop o il driver alla libreria generico che contiene il set di API principali del sistema operativo a cui si è interessati.

Per altri dettagli, vedere l'Windows [librerie generico.](windows-umbrella-libraries.md)

## <a name="api-set-contract-names"></a>Nomi dei contratti del set di API

I set di API sono identificati da un nome di contratto sicuro che segue queste convenzioni standard riconosciute dal caricatore di libreria. 

- Il nome deve iniziare con la stringa **api-** o **ext-**. 
    - I nomi che **iniziano con api** rappresentano API che sono garantite in tutte Windows 10 versioni.
    - I nomi che **iniziano con ext-** rappresentano API che potrebbero non esistere in tutte Windows 10 versioni.
- Il nome deve terminare con la sequenza **\<n\> - \<n\> - \<n\> l**, dove **n è** costituito da cifre decimali.
- Il corpo del nome può essere di caratteri alfanumerici o trattini ( **-** ).
- Per il nome non viene fatta distinzione tra maiuscole e minuscole.

Ecco alcuni esempi di nomi di contratto del set di API:

- **api-ms-win-core-ums-l1-1-0**
- **ext-ms-win-com-ole32-l1-1-5**
- **ext-ms-win-ntuser-window-l1-1-0**
- **ext-ms-win-ntuser-window-l1-1-1**

È possibile usare un nome di set di API nel contesto di un'operazione del caricatore, ad esempio [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) o [P/Invoke,](/dotnet/standard/native-interop/pinvoke) anziché un nome di modulo DLL per garantire una route corretta all'implementazione, indipendentemente dalla posizione in cui l'API viene effettivamente implementata nel dispositivo corrente. Tuttavia, in questo caso è necessario aggiungere la **stringa.dll** alla fine del nome del contratto. Si tratta di un requisito per il corretto funzionamento del caricatore e non è considerato effettivamente una parte del nome del contratto. Anche se in questo contesto i nomi dei contratti sono simili ai nomi delle DLL, sono fondamentalmente diversi dai nomi dei moduli DLL e non fanno riferimento direttamente a un file su disco.

Fatta eccezione per l'aggiunta della **stringa.dll** nelle operazioni del caricatore, i nomi dei contratti del set di API devono essere considerati un identificatore non modificabile che corrisponde a una versione del contratto specifica.

## <a name="identifying-api-sets-for-win32-apis"></a>Identificazione dei set di API per le API Win32

Per determinare se una particolare API Win32 appartiene a un set di API, esaminare la tabella dei requisiti nella documentazione di riferimento per l'API. Se l'API appartiene a un set di API, la tabella dei requisiti nell'articolo elenca il nome del set di API e la versione di Windows in cui l'API è stata introdotta per la prima volta nel set di API. Per esempi di API che appartengono a un set di API, vedere questi articoli:

- [AllowSetForegroundWindow](/windows/win32/api/winuser/nf-winuser-allowsetforegroundwindow)
- [FindWindowsEx](/windows/win32/api/winuser/nf-winuser-findwindowexa)
- [GetClassFile](/windows/win32/api/objbase/nf-objbase-getclassfile)

## <a name="in-this-section"></a>Contenuto della sezione

* [Funzionamento del caricatore dei set di API](api-set-loader-operation.md)
* [Rilevare la disponibilità di un set di API](detect-api-set-availability.md)
* [Librerie generiche di Windows](windows-umbrella-libraries.md)