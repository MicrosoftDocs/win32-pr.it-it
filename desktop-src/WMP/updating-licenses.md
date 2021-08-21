---
title: Aggiornamento delle licenze
description: Aggiornamento delle licenze
ms.assetid: b298badf-efcf-423c-8cc7-c3f50ab288a0
keywords:
- Windows Media Player online, aggiornamento delle licenze
- negozi online, aggiornamento delle licenze
- store online di tipo 1, aggiornamento delle licenze
- Windows Media Player online, aggiornamento delle licenze
- negozi online, aggiornamento delle licenze
- store online di tipo 1, aggiornamento delle licenze
- aggiornamento delle licenze
- licenze, aggiornamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 182af125021af43b1a08695d00c194ec90c38a543d95123b093d30375e45e0c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118117326"
---
# <a name="updating-licenses"></a>Aggiornamento delle licenze

Gli store online possono distribuire contenuti concessi in licenza per un periodo di tempo specifico o fino a una determinata data. Questo è normale per il contenuto musicale fornito come parte di un contratto di servizio di sottoscrizione. In questo caso, lo store online deve avere la possibilità di aggiornare queste licenze prima della scadenza, presupponendo, naturalmente, che l'utente abbia pagato per rinnovare la propria sottoscrizione. Se l'utente non ha rinnovato la sottoscrizione, le licenze possono semplicemente scadere.

Windows Media Player esegue una query sul plug-in partner di contenuti sulla quantità di avvisi in anticipo che il lettore deve fornire per una licenza che sta per scadere. A tale scopo, chiama [IWMPContentPartner::GetContentPartnerInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcontentpartnerinfo), passando la costante g \_ szContentPartnerInfo \_ LicenseRefreshAdvanceWarning tramite il *parametro bstrInfoName.* Per avvisare il plug-in delle licenze che stanno per scadere, Windows Media Player [chiama IWMPContentPartner::RefreshLicense](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-refreshlicense). Questa chiamata accetta parametri che forniscono dettagli sul file da aggiornare, ad esempio se il file si trova nel computer dell'utente e il percorso del file. Se la licenza viene aggiornata come parte di un'operazione di sincronizzazione del dispositivo, il *parametro pReasonContext* fornisce il nome descrittivo del dispositivo

Quando Windows Media Player chiama **RefreshLicence,** passa un cookie che identifica la richiesta di aggiornamento. Al termine dell'elaborazione della richiesta di aggiornamento, il plug-in invia una notifica Windows Media Player chiamando [IWMPContentPartnerCallback::RefreshLicenseComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-refreshlicensecomplete), passando il cookie, l'ID dell'elemento multimediale e un **HRESULT** che indica se l'aggiornamento è stato completato correttamente.

I plug-in dei negozi online possono anche eseguire l'ispezione delle licenze e gli aggiornamenti come processo in background. Windows Media Player notifica al plug-in gli orari in cui è consentito eseguire attività di elaborazione in background chiamando [IWMPContentPartner::Notify.](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-notify) Per segnalare al plug-in di avviare l'elaborazione in background, il lettore passa il valore di enumerazione [WMPPartnerNotification](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmppartnernotification) wmpsnBackgroundProcessingBegin; per segnalare al plug-in di arrestare l'elaborazione in background, il lettore passa il valore wmpsnBackgroundProcessingEnd.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida di programmazione per gli store online di tipo 1**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




