---
title: Esecuzione della individualizzazione DRM
description: Esecuzione della individualizzazione DRM
ms.assetid: daad1a31-f0a7-43ab-b920-94b9f050a44e
keywords:
- Windows MEDIA Format SDK, API estese del client DRM
- Windows MEDIA Format SDK, API estese client
- Windows Media Format SDK, API estese
- Windows MEDIA Format SDK, API
- Windows Media Format SDK, Digital Rights Management (DRM)
- Windows Media Format SDK, individualizzazione DRM
- Windows Media Format SDK, individualizzazione
- DRM (Digital Rights Management), API estese client
- DRM (Digital Rights Management),API estese client
- DRM (Digital Rights Management), API estese
- DRM (Digital Rights Management),API estese
- DRM (Digital Rights Management), API
- DRM (Digital Rights Management),API
- digital rights management (DRM), individualizzazione
- DRM (Digital Rights Management),individualizzazione
- digital rights management (DRM),individualizzazione DRM
- DRM (digital rights management),individualizzazione DRM
- API estese del client DRM, individualizzazione
- API estese client, individualizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72c46d2cd6fccd2c6c1a8898a2d0215b6bc62a3655b12412192d1809021747ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027389"
---
# <a name="performing-drm-individualization"></a>Esecuzione della individualizzazione DRM

La individualizzazione è il processo di aggiornamento del componente DRM nel computer client, crittografia e univocità. Quando un computer viene individualizzato, il componente DRM è associato al computer e non sarà in grado di decodificare il contenuto in nessun altro computer. Le WINDOWS Client Extended di Media DRM forniscono il supporto per l'individualizzazione del componente DRM nei computer client.

La individualizzazione viene eseguita chiamando il [**metodo IWMDRMSecurity::P erformSecurityUpdate.**](iwmdrmsecurity-performsecurityupdate.md) È possibile chiamare **PerformSecurityUpdate** in modo che si individualizzi solo se la versione nel server è più recente di quella installata nel computer client oppure è possibile forzare l'individualizzazione indipendentemente dalle versioni di sicurezza relative. Il flag per l'individualizzazione in base alle esigenze è WMDRM \_ SECURITY \_ PERFORM \_ INDIV. Il flag per l'individualizzazione forzata è WMDRM \_ SECURITY \_ PERFORM FORCE \_ \_ INDIV.

**PerformSecurityUpdate è** una chiamata asincrona. Verrà restituito rapidamente e quindi verranno generati eventi per fornire informazioni sullo stato del processo di individualizzazione. La maggior parte degli eventi generati sarà eventi **MEWMDRMIndividualizationProgress** e a ognuno è associata [**un'interfaccia IWMDRMIndividualizationStatus.**](iwmdrmindividualizationstatus.md) Per ottenere l'interfaccia di stato, è necessario chiamare **IMFMediaEvent::GetValue** per recuperare un puntatore **IUnknown** che si trova nello stesso oggetto e quindi eseguire una query per **IWMDRMIndividualizationStatus.**

È possibile ottenere i dati per una struttura [**WM \_ INDIVIDUALIZE \_ STATUS**](drmwm-individualize-status.md) chiamando [**IWMDRMIndividualizeStatus::GetStatus**](iwmdrmindividualizationstatus-getstatus.md). Ogni evento generato ha un proprio oggetto con stato, quindi è necessario eseguire ogni volta il processo di recupero del valore dell'evento ed eseguire query sull'interfaccia di stato.

A seconda delle dimensioni del download, possono essere presenti decine o centinaia di eventi **MEWMDRMIndividualizationProgress.** Al termine del processo di individualizzazione, viene generato un evento **MEWMDRMIndividualizationCompleted.**

Al termine della individualizzazione, gli unici oggetti esistenti che rifletteranno il nuovo stato individualizzato sono quelli che ereditano da [**IWMDRMSecurity.**](iwmdrmsecurity.md) Tutti gli altri oggetti esistenti non verranno aggiornati. È necessario rilasciare e creare nuovamente qualsiasi altro oggetto in modo che riflettano il nuovo stato individualizzato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Esempio di individualizzazione DRM**](drm-individualization-example.md)
</dt> <dt>

[**Guida per programmatori**](drm-programming-guide.md)
</dt> <dt>

[**Uso del modello Media Foundation eventi**](using-the-media-foundation-model.md)
</dt> <dt>

[Windows Procedure consigliate per l'individualizzazione di Media DRM](/previous-versions/ms867216(v=msdn.10))
</dt> </dl>

 

 




