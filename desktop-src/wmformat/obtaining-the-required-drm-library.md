---
title: Ottenere la libreria DRM necessaria
description: Ottenere la libreria DRM necessaria
ms.assetid: 7bd13b77-439e-40cf-99e8-b359247da74d
keywords:
- Windows Media Format SDK, acquisizione delle librerie DRM richieste
- ASF (Advanced Systems Format), acquisizione delle librerie DRM richieste
- ASF (Advanced Systems Format), acquisizione delle librerie DRM richieste
- Digital Rights Management (DRM), ottenere le librerie necessarie
- DRM (Digital Rights Management), recupero delle librerie richieste
- Digital Rights Management (DRM), informazioni sulla compilazione
- DRM (Digital Rights Management), informazioni sulla compilazione
- Digital Rights Management (DRM), informazioni di debug
- DRM (Digital Rights Management), informazioni di debug
- debug di DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f5c124c1e7edf0bba736b9dd392e852aac97e96
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "104399858"
---
# <a name="obtaining-the-required-drm-library"></a>Ottenere la libreria DRM necessaria

Per creare o riprodurre file multimediali digitali protetti da DRM, l'applicazione deve collegarsi a una libreria statica fornita in formato binario da Microsoft. Questa libreria è talvolta denominata libreria stub o "stublib" e identifica in modo univoco l'applicazione.

In questa documentazione la libreria DRM è denominata "WMStubDRM. lib". Il nome della libreria ricevuta includerà un numero di identificazione. Per ottenere questa libreria, è necessario firmare un contratto di licenza con Microsoft. Le condizioni del contratto possono variare a seconda che si richieda una licenza di valutazione o una licenza di produzione. Per ulteriori informazioni sul processo di gestione delle licenze DRM, vedere il modulo Windows Media Licensing sul [sito Web Microsoft](https://www.microsoft.com/licensing/default).

La libreria ricevuta ha un livello di protezione DRM che dipende dal tipo di contratto di licenza immesso. Una licenza DRM può limitare l'accesso al contenuto del file alle applicazioni con componenti DRM al di sotto di un livello di sicurezza specificato. Questo livello di sicurezza non corrisponde al livello di individualizzazione DRM e non è correlato a uno dei valori numerici dei livelli di protezione dell'output (OPLs). La tabella seguente illustra esempi di livelli di sicurezza DRM per diversi lettori e dispositivi portatili.



| Livello di sicurezza | Lettori e dispositivi portatili                                                                                                                                                                                                                                                                                                   | Esempio                                                                                                                                                                                          |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 150            | Dispositivi che non supportano Windows Media DRM. La protezione DRM viene rimossa quando il contenuto viene trasferito a tale dispositivo.                                                                                                                                                                                                         | Dispositivi che supportano contenuto basato su Windows Media ma non protetto                                                                                                                       |
| 1\.000          | Applicazioni Player basate su Windows Media Format 9,5 SDK o versioni precedenti che non soddisfano requisiti aggiuntivi per il livello 2000. dispositivi basati su Windows Media Portable Device DRM V1.<br/> Dispositivi basati su Windows CE 4,2 e versioni successive.<br/>                                                                       | Windows Media Player 6,4, Windows Media Player 7Portable i dispositivi multimediali che supportano Windows Media Portable Device DRM V1.<br/>                                                             |
| 2\.000          | Applicazioni Player basate su Windows Media Format 9 Series SDK o versione successiva e che seguono un set più restrittivo di linee guida per la protezione dei contenuti rispetto alle applicazioni a livello 1000. dispositivi basati su Windows Media DRM 10 per dispositivi portatili.<br/> Dispositivi basati su Windows Media DRM 10 per i dispositivi di rete.<br/> | Windows Media Player 9 e dispositivi multimediali laterPortable che supportano Windows Media DRM 10 per dispositivi portatili<br/> Dispositivi Portable Media Center basati su Windows Mobile<br/> |



 

## <a name="build-and-debugging-information"></a>Informazioni di compilazione e debug

Quando si collega a WMStubDRM. lib, non eseguire il collegamento a wmvcore. lib. Se l'applicazione è collegata a entrambe le librerie, il componente DRM non funzionerà correttamente.

Un punto di interruzione utente nel componente DRM impedisce l'accesso al contenuto protetto da parte di versioni di debug e di rilascio delle applicazioni quando viene eseguito all'interno del debugger. Per risolvere i problemi relativi alle funzioni correlate a DRM nell'applicazione, è necessario scrivere routine di traccia personalizzate che salvano le informazioni, ad esempio i valori **HRESULT** , in alcune posizioni, ad esempio un file di log.

Se si tenta di eseguire una versione di rilascio di un'applicazione in un sistema con una versione di debug dei bit SDK installata (o viceversa), durante la riproduzione del contenuto DRM versione 7 si verificheranno errori di heap. Assicurarsi di eseguire le applicazioni di debug sui bit SDK di debug e rilasciare le applicazioni oltre i bit della versione. Lo stesso problema si verificherà se si esegue una versione di debug dell'SDK con un componente DRM individualizzato, che è sempre una build di rilascio.

**Note** Il DRM non è supportato dalla versione basata su x64 di questo SDK.

I file WMStubDRM. lib associati al formato Windows Media 9,5 SDK possono essere utilizzati solo con i componenti di Microsoft Visual Studio .NET 2003. Se si utilizza una versione precedente della libreria stub, non sono previste nuove restrizioni per l'utilizzo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Abilitazione del supporto DRM**](enabling-drm-support.md)
</dt> </dl>

 

 





