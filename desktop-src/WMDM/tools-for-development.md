---
title: Strumenti per lo sviluppo
description: Strumenti per lo sviluppo
ms.assetid: 7932f599-a073-4fc8-82da-c0e7001c1809
keywords:
- Windows Media Gestione dispositivi, strumenti di sviluppo
- Gestione dispositivi, strumenti di sviluppo
- Windows Media Gestione dispositivi, certificati
- Gestione dispositivi, certificati
- Windows Media Gestione dispositivi, chiavi
- Gestione dispositivi, chiavi
- Windows Media Gestione dispositivi, librerie
- Gestione dispositivi, librerie
- Windows Media Gestione dispositivi, Software Development Kit (SDK)
- Gestione dispositivi, Software Development Kit (SDK)
- Windows Media Gestione dispositivi SDK
- SDK di Gestione dispositivi
- Windows Media Player SDK
- Windows Media Format SDK
- Windows Media Rights Manager SDK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45a3e419b87c56a447ad2412234a80432b1598e
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "106300620"
---
# <a name="tools-for-development"></a>Strumenti per lo sviluppo

In questa sezione vengono descritti i vari certificati e chiavi, le librerie e gli SDK necessari per programmare mediante Windows Media Gestione dispositivi SDK.

Certificati e chiavi

Windows Media Gestione dispositivi SDK viene fornito con una coppia chiave/certificato di test (nel file Key. c) che può essere usata da un'applicazione o da un provider di servizi per usare i metodi di Windows Media Gestione dispositivi su contenuto non protetto. Questa coppia chiave/certificato consente all'applicazione o al provider di servizi di utilizzare la maggior parte delle funzionalità Windows Media Gestione dispositivi.

Tuttavia, per sviluppare un'applicazione o un provider di servizi in grado di gestire contenuti protetti da DRM, è necessario richiedere uno o più certificati (ognuno con una chiave) dalla [pagina Windows Media Licensing](https://www.microsoft.com/licensing/default). I certificati sono necessari per le applicazioni o gli oggetti seguenti:

-   I provider di servizi che gestiscono il contenuto protetto con DRM richiedono un certificato del provider di servizi Windows Media Gestione dispositivi (e una chiave)
-   Le applicazioni che trasferiscono contenuti protetti con DRM richiedono un certificato di trasferimento Gestione dispositivi Windows Media (e una chiave)
-   Le applicazioni che svolgono contenuti protetti con DRM richiedono un certificato DRM (e una chiave).
-   I componenti di misurazione delle licenze richiedono un certificato di misurazione. Questa operazione viene fornita da un servizio di controllo delle licenze creato in Windows Media Rights Manager SDK, che può essere richiesto nella pagina Windows Media Licensing.

Librerie e intestazioni

Oltre alle librerie e alle intestazioni indicate nei [file di intestazione e di libreria necessari per un'applicazione](required-library-and-header-files-for-an-application.md) o le [librerie e le intestazioni obbligatorie per un provider di servizi](required-libraries-and-headers-for-a-service-provider.md), qualsiasi applicazione o plug-in precedentemente collegato a WMDRMSDK. lib per chiamare le funzioni di Windows Media Format SDK dovrebbe ora eseguire il collegamento a WMDRMSDKStub. lib. Questo file di libreria viene utilizzato per accedere ai file protetti da DRM. È possibile richiedere questa libreria anche dalla pagina Windows Media Licensing.

SDK correlati

Gli SDK Microsoft seguenti forniscono elementi che potrebbero essere necessari per la progettazione di soluzioni per i dispositivi multimediali portatili.



| SDK obbligatorio                     | Obbligatorio per...                                                                                                                                                                                                                       |
|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Media Gestione dispositivi SDK | Applicazioni desktop media player che comunicano con dispositivi portatili<br/> Applicazioni desktop che possono scambiare file o informazioni con i dispositivi portatili<br/> Oggetti COM di controllo Media Player di Windows<br/> |
| Windows Media Player SDK         | Plug-in di Windows Media Player<br/> Oggetti COM di controllo Media Player di Windows<br/> Interfacce di Media Player Windows<br/>                                                                                                   |
| Windows Media Format SDK         | Lettori audio o video in grado di creare o riprodurre file (in particolare file ASF)<br/> Applicazioni di modifica audio o video<br/>                                                                                               |
| Windows Media Rights Manager SDK | Applicazioni o plug-in che controllano la riproduzione del contatore sul desktop o sul dispositivo.                                                                                                                                                             |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Introduzione**](getting-started.md)
</dt> </dl>

 

 





