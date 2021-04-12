---
title: Esecuzione dell'individualizzazione DRM
description: Esecuzione dell'individualizzazione DRM
ms.assetid: daad1a31-f0a7-43ab-b920-94b9f050a44e
keywords:
- Windows Media Format SDK, API client DRM estese
- Windows Media Format SDK, API client estese
- Windows Media Format SDK, API estese
- Windows Media Format SDK, API
- Windows Media Format SDK, Digital Rights Management (DRM)
- Windows Media Format SDK, individualizzazione DRM
- Windows Media Format SDK, individualizzazione
- Digital Rights Management (DRM), API estese del client
- DRM (Digital Rights Management), API estese client
- Digital Rights Management (DRM), API estese
- DRM (Digital Rights Management), API estese
- Digital Rights Management (DRM), API
- DRM (Digital Rights Management), API
- Digital Rights Management (DRM), individualizzazione
- DRM (Digital Rights Management), individualizzazione
- Digital Rights Management (DRM), individualizzazione DRM
- DRM (Digital Rights Management), individualizzazione DRM
- API estese del client DRM, individualizzazione
- API estese client, individualizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d8f7f04add4ed626985651d5220e69ea713e4d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331711"
---
# <a name="performing-drm-individualization"></a>Esecuzione dell'individualizzazione DRM

L'individualizzazione è il processo di aggiornamento del componente DRM nel computer client, della crittografia e della sua univocità. Quando un computer è individualizzato, il componente DRM è collegato al computer e non sarà in grado di decodificare il contenuto in un altro computer. Le API estese del client Windows Media DRM forniscono supporto per individualizzazione il componente DRM nei computer client.

L'individualizzazione viene eseguita chiamando il metodo [**IWMDRMSecurity::P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) . È possibile chiamare **PerformSecurityUpdate** in modo che venga individuato solo se la versione sul server è più recente di quella installata nel computer client o se è possibile forzare l'individualizzazione senza considerare le versioni di sicurezza relative. Il flag per l'individualizzazione necessaria è WMDRM \_ Security \_ \_ indiv. Il flag per l'individualizzazione forzata è WMDRM \_ Security \_ eseguire \_ Force \_ indiv.

**PerformSecurityUpdate** è una chiamata asincrona. Viene restituito rapidamente e quindi genera eventi per fornire informazioni sullo stato del processo di individualizzazione. La maggior parte degli eventi generati sarà costituita da eventi **MEWMDRMIndividualizationProgress** , ognuno dei quali ha un'interfaccia [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md) associata. Per ottenere l'interfaccia di stato, è necessario chiamare **IMFMediaEvent:: GetValue** per recuperare un puntatore **IUnknown** che si trova nello stesso oggetto, quindi eseguire una query per **IWMDRMIndividualizationStatus**.

È possibile ottenere dati per una struttura di [**\_ \_ stato di personalizzazione WM**](drmwm-individualize-status.md) chiamando [**IWMDRMIndividualizeStatus:: GetStatus**](iwmdrmindividualizationstatus-getstatus.md). Ogni evento generato ha un proprio oggetto con lo stato, quindi è necessario eseguire ogni volta il processo di recupero del valore dell'evento ed esecuzione di query per l'interfaccia di stato.

A seconda delle dimensioni del download, potrebbero essere presenti dozzine o centinaia di eventi **MEWMDRMIndividualizationProgress** . Al termine del processo di individualizzazione, viene generato un evento **MEWMDRMIndividualizationCompleted** .

Una volta completata l'individualizzazione, gli unici oggetti esistenti che riflettono il nuovo stato individualizzato saranno quelli che ereditano da [**IWMDRMSecurity**](iwmdrmsecurity.md). Tutti gli altri oggetti esistenti non verranno aggiornati. È necessario rilasciare e ricreare altri oggetti in modo che riflettano il nuovo stato individualizzato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Esempio di individualizzazione DRM**](drm-individualization-example.md)
</dt> <dt>

[**Guida per programmatori**](drm-programming-guide.md)
</dt> <dt>

[**Uso del modello di eventi Media Foundation**](using-the-media-foundation-model.md)
</dt> <dt>

[Procedure consigliate per l'individualizzazione DRM di Windows Media](/previous-versions/ms867216(v=msdn.10))
</dt> </dl>

 

 




