---
title: Aggiornamento delle licenze
description: Aggiornamento delle licenze
ms.assetid: b298badf-efcf-423c-8cc7-c3f50ab288a0
keywords:
- Windows Media Player Online Stores, aggiornamento delle licenze
- archivi online, aggiornamento delle licenze
- digitare 1 negozi online, aggiornamento delle licenze
- Windows Media Player Online Stores, aggiornamento delle licenze
- negozi online, aggiornamento delle licenze
- digitare 1 negozi online, aggiornamento delle licenze
- aggiornamento delle licenze
- licenze, aggiornamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 154959b01c93719184e310b60dffaa91fe2dcfa0
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336329"
---
# <a name="updating-licenses"></a>Aggiornamento delle licenze

Gli archivi online possono fornire contenuti con licenza per un periodo di tempo specifico o fino a una determinata data. Si tratta di una situazione normale per il contenuto musicale fornito come parte di un contratto di servizio di sottoscrizione. In questo caso, lo Store online deve avere la possibilità di aggiornare le licenze prima della scadenza, presumendo, ovviamente, che l'utente abbia pagato per rinnovare la propria sottoscrizione. Se l'utente non ha rinnovato la sottoscrizione, le licenze possono semplicemente essere lasciate scadere.

Windows Media Player esegue una query sul plug-in del partner di contenuti circa la quantità di avvisi di anticipo che il lettore deve fornire per una licenza che sta per scadere. Questa operazione viene eseguita chiamando [IWMPContentPartner:: GetContentPartnerInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcontentpartnerinfo), passando la costante g \_ szContentPartnerInfo \_ LicenseRefreshAdvanceWarning tramite il parametro *bstrInfoName* . Per avvisare il plug-in sulle licenze che stanno per scadere, Windows Media Player chiama [IWMPContentPartner:: RefreshLicense](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-refreshlicense). Questa chiamata accetta parametri che forniscono dettagli sul file da aggiornare, ad esempio se il file si trova nel computer dell'utente e il percorso del file. Se la licenza viene aggiornata nell'ambito di un'operazione di sincronizzazione del dispositivo, il parametro *pReasonContext* fornisce il nome cannonical del dispositivo

Quando Windows Media Player chiama **RefreshLicence**, passa un cookie che identifica la richiesta di aggiornamento. Al termine dell'elaborazione della richiesta di aggiornamento, il plug-in Invia una notifica a Windows Media Player chiamando [IWMPContentPartnerCallback:: RefreshLicenseComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-refreshlicensecomplete), passando il cookie, l'ID dell'elemento multimediale e un valore **HRESULT** che indica se l'aggiornamento è stato eseguito correttamente.

I plug-in di Store online possono anche eseguire l'ispezione e gli aggiornamenti delle licenze come processo in background. Windows Media Player notifica al plug-in informazioni sugli orari in cui è consentito eseguire attività di elaborazione in background chiamando [IWMPContentPartner:: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-notify). Per segnalare al plug-in di avviare l'elaborazione in background, il giocatore passa il valore di enumerazione [WMPPartnerNotification](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmppartnernotification) wmpsnBackgroundProcessingBegin; per segnalare al plug-in di arrestare l'elaborazione in background, il giocatore passa il valore wmpsnBackgroundProcessingEnd.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida per programmatori per i negozi di tipo 1 online**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




