---
title: Gestione del contenuto protetto
description: Gestione del contenuto protetto
ms.assetid: f218d69e-ac80-43ba-be31-af3abf2b8de9
keywords:
- Windows Media Gestione dispositivi, certificati
- Gestione dispositivi, certificati
- applicazioni desktop, certificati
- provider di servizi, certificati
- Guida per programmatori, certificati
- certificates
- Windows Media Gestione dispositivi, Secure Content Provider (SCP)
- Gestione dispositivi, Secure Content Provider (SCP)
- applicazioni desktop, Secure Content Provider (SCP)
- provider di servizi, Secure Content Provider (SCP)
- Guida per programmatori, Secure Content Provider (SCP)
- provider di contenuti protetti (SCP)
- SCP (provider di contenuti protetto)
- Windows Media Gestione dispositivi, contenuto protetto da DRM
- Gestione dispositivi, contenuto protetto da DRM
- Guida per programmatori, contenuto protetto da DRM
- applicazioni desktop, contenuto protetto da DRM
- provider di servizi, contenuto protetto da DRM
- Contenuto protetto da DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd0fb6ab155d08ed19eb84988709695f9ed63fd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395702"
---
# <a name="handling-protected-content"></a>Gestione del contenuto protetto

Se si compila un'applicazione o un provider di servizi che utilizzerà il contenuto protetto da Windows Media Digital Rights Management (DRM), è necessario disporre di una coppia chiave/certificato rilasciata da Microsoft. Per informazioni su dove ottenere questo certificato, vedere [strumenti per lo sviluppo](tools-for-development.md). Se non si prevede di gestire il contenuto protetto, è possibile usare la chiave fittizia e il certificato fornito con questo SDK in un file denominato Key. c.

Per tutti i file protetti dalla tecnologia DRM, Windows Media Gestione dispositivi richiede la presenza di un provider di contenuti protetto (SCP) per il formato di file. Microsoft fornisce un modulo SCP per i file WMA e WMV. Se l'applicazione o il provider di servizi gestisce contenuti protetti con DRM di un altro formato, è necessario fornire il proprio modulo SCP. Un modulo SCP è un oggetto COM che implementa tutte le [interfacce per i provider di contenuti protetti](interfaces-for-secure-content-providers.md).

Un'applicazione può inviare contenuto protetto da DRM ai dispositivi compilati in Windows Media DRM 10 per i dispositivi portatili o DRM (PDDRM). Tuttavia, è possibile creare solo un provider di servizi per i dispositivi basati su PDDRM; non è possibile creare un provider di servizi per i dispositivi basati su Windows Media DRM 10 per i dispositivi portatili. Questi ultimi dispositivi possono usare solo il provider di servizi MTP fornito da Microsoft.

I dispositivi basati su PDDRM possono supportare solo le licenze per il contenuto acquistato. Le licenze con condizioni di scadenza del tempo sono supportate solo dai dispositivi basati su Windows Media DRM 10 per i dispositivi portatili, che hanno requisiti speciali, ad esempio un orologio sicuro e una individualizzazione. Windows Media DRM 10 per i dispositivi portatili SDK fornisce informazioni dettagliate sui requisiti dei dispositivi per supportare la tecnologia versione 10.

Prima di inviare contenuto DRM al dispositivo, un'applicazione deve verificare diverse operazioni:

-   Il dispositivo supporta la tecnologia DRM.
-   Versione della tecnologia DRM supportata (versione 10 o precedente).
-   Se il dispositivo è basato sulla versione 10, tutti i relativi componenti sono aggiornati, ad esempio il clock sicuro e i requisiti di individualizzazione.

Tutte le chiamate ai metodi per rispondere a queste domande vengono effettuate dal client e gestite da Windows Media Gestione dispositivi e dal componente del provider di contenuti protetto. il provider di servizi non gestisce nessuna di queste chiamate.

Se il dispositivo non supporta Windows Media DRM 10 per i dispositivi portatili, potrebbe comunque essere in grado di utilizzare contenuto protetto (a seconda della licenza del contenuto e della progettazione del dispositivo), ma qualsiasi contenuto inviato avrà una licenza d'uso semplificata con diritti limitati (ad esempio, nessuna scadenza dell'ora).

-   Per esempi che illustrano il modo in cui un'applicazione verifica se un dispositivo è in grado di gestire il contenuto protetto e se deve aggiornare i componenti DRM, vedere [gestione del contenuto protetto nell'applicazione](handling-protected-content-in-the-application.md).
-   Per ulteriori informazioni sulla compilazione di un provider di servizi in grado di gestire il contenuto protetto, vedere [gestione del contenuto protetto nel provider di servizi](handling-protected-content-in-the-service-provider.md).

> [!Note]  
> Molti Windows Media Gestione dispositivi il trasferimento di file o i diritti che richiedono metodi non riusciranno (spesso con un valore **HRESULT** misterioso) quando si gestiscono file protetti con DRM con un debugger collegato. Pertanto, è necessario utilizzare modi alternativi per eseguire il debug del codice, ad esempio la registrazione degli output in un Windows Form o in un file di log. Per ulteriori informazioni sulle opzioni di registrazione, vedere [Abilitazione della registrazione](enabling-logging.md). Se si esegue un debugger sul contenuto protetto, un metodo restituirà uno dei codici di errore elencati nella sezione DRM codici di [errore](error-codes.md)o un codice di errore sconosciuto. Se si ottengono valori **HRESULT** misteriosi quando si esegue un debugger su contenuto o metodi protetti, la protezione DRM potrebbe essere la stessa.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida per programmatori**](programming-guide.md)
</dt> </dl>

 

 




