---
title: Strumenti per lo sviluppo
description: Strumenti per lo sviluppo
ms.assetid: 7932f599-a073-4fc8-82da-c0e7001c1809
keywords:
- Windows Gestione dispositivi multimediali, strumenti di sviluppo
- Gestione dispositivi, strumenti di sviluppo
- Windows Gestione dispositivi multimediali, certificati
- Gestione dispositivi, certificati
- Windows Gestione dispositivi multimediali, chiavi
- Gestione dispositivi, chiavi
- Windows Gestione dispositivi multimediali, librerie
- Gestione dispositivi, librerie
- Windows Gestione dispositivi multimediali, Software Development Kit (SDK)
- Gestione dispositivi, Software Development Kit (SDK)
- Windows Media Device Manager SDK
- SDK di Gestione dispositivi
- Windows Media Player Sdk
- Windows Media Format SDK
- Windows Media Rights Manager SDK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e517a97246c2bf9b2ac5670a7cf696e714777a2f5926a37e1b2d37ecbe45c9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031611"
---
# <a name="tools-for-development"></a>Strumenti per lo sviluppo

Questa sezione descrive i vari certificati e chiavi, librerie e SDK che è necessario programmare usando l'SDK Windows Media Device Manager.

Certificati e chiavi

L'SDK di Windows Media Device Manager viene fornito con una coppia chiave/certificato di test (nel file key.c) che può essere usata da un'applicazione o da un provider di servizi per usare i metodi di Gestione dispositivi multimediali di Windows su contenuto non protetto. Questa coppia chiave/certificato consente all'applicazione o al provider di servizi di usare la maggior parte Windows funzionalità Gestione dispositivi multimediali.

Tuttavia, per sviluppare un'applicazione o un provider di servizi in grado di gestire contenuto protetto da DRM, è necessario richiedere uno o più certificati (ognuno con una chiave) dalla pagina delle licenze multimediali di [Windows](https://www.microsoft.com/licensing/default). I certificati sono necessari per le applicazioni o gli oggetti seguenti:

-   I provider di servizi che gestiscono contenuti protetti da DRM richiedono un certificato e una chiave Windows provider di servizi di Gestione dispositivi multimediali
-   Le applicazioni che trasferiscono contenuto protetto da DRM richiedono Windows certificato di trasferimento (e chiave) di Gestione dispositivi multimediali
-   Le applicazioni che riproducino contenuto protetto da DRM richiedono un certificato (e una chiave) DRM.
-   I componenti di misurazione delle licenze richiedono un certificato di controllo. Viene fornito da un servizio di controllo delle licenze basato su Windows Media Rights Manager SDK, che può essere richiesto nella pagina Windows Media Licensing.

Librerie e intestazioni

Oltre alle librerie e alle intestazioni indicate [in](required-library-and-header-files-for-an-application.md) Libreria richiesta e file di intestazione per un'applicazione o Librerie e intestazioni necessarie per un [provider](required-libraries-and-headers-for-a-service-provider.md)di servizi, qualsiasi applicazione o plug-in precedentemente collegato a WMDRMSDK.lib per chiamare le funzioni di Windows Media Format SDK dovrebbe ora collegarsi a WMDRMSDKStub.Lib. Questo file di libreria viene usato per accedere ai file protetti da DRM. È possibile richiedere questa libreria anche dalla pagina Windows licenze multimediali.

SDK correlati

I Microsoft SDK seguenti forniscono gli elementi che potrebbero essere necessari per la progettazione di soluzioni per dispositivi multimediali portatili.



| SDK obbligatorio                     | Obbligatorio per...                                                                                                                                                                                                                       |
|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Media Device Manager SDK | Applicazioni lettore multimediale desktop che comunicano con dispositivi portatili<br/> Applicazioni desktop in grado di scambiare file o informazioni con dispositivi portatili<br/> Windows Media Player oggetti COM di misurazione<br/> |
| Windows Media Player Sdk         | Windows Media Player plug-in<br/> Windows Media Player oggetti COM di misurazione<br/> Windows Media Player interfaccia utente<br/>                                                                                                   |
| Windows Media Format SDK         | Lettori audio o video in grado di creare o riprodurre file (in particolare file ASF)<br/> Applicazioni di modifica audio o video<br/>                                                                                               |
| Windows Media Rights Manager SDK | Le applicazioni o i plug-in che misurano la riproduzione vengono conteggiati sul desktop o sul dispositivo.                                                                                                                                                             |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Attività iniziali**](getting-started.md)
</dt> </dl>

 

 





