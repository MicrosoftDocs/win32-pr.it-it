---
title: Informazioni sul ripping del CD
description: Informazioni sul ripping del CD
ms.assetid: 1a179284-2909-4fc0-82be-996794ee4f31
keywords:
- Windows Media Player, copia di CD
- Modello a oggetti di Windows Media Player, copia di CD
- modello a oggetti, copia di CD
- Controllo ActiveX di Windows Media Player, copia di CD
- Controllo ActiveX, copia di CD
- Controllo ActiveX Windows Media Player Mobile, copia di CD
- Windows Media Player Mobile, copia di CD
- Ripping di CD, informazioni
- ripping di CDs, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e28769c6af666e510fb97ebc98e44fadc7c3e472
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299417"
---
# <a name="about-cd-ripping"></a>Informazioni sul ripping del CD

Windows Media Player 11 SDK introduce nuove funzionalità per la copia di tracce audio da CDs al computer dell'utente. Questo processo è denominato *estrazione*.

Quando si esegue il RIP delle tracce audio utilizzando le interfacce di Windows Media Player SDK, le tracce musicali risultanti vengono create utilizzando le impostazioni definite dall'utente nella finestra di dialogo **Opzioni** di Windows Media Player.

Per enumerare le unità CD nel computer dell'utente, usare l'interfaccia **IWMPCdromCollection** . Per recuperare un puntatore a questa interfaccia, chiamare [IWMPCore:: Get \_ cdromcollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection). Utilizzando i metodi **count** e **Item** , è possibile eseguire l'iterazione della raccolta per recuperare un puntatore di interfaccia **IWMPCdrom** per ogni unità CD nel computer dell'utente. L'interfaccia **IWMPCdrom** rappresenta una singola unità CD. Prima di iniziare a rippare un CD, è prima necessario chiamare **QueryInterface** tramite un puntatore **IWMPCdrom** per recuperare un puntatore all'interfaccia **IWMPCdromRip** .

Per avviare l'operazione di estrazione, è sufficiente chiamare [IWMPCdromRip:: startRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-startrip). È possibile monitorare lo stato di avanzamento dell'operazione di strappo chiamando periodicamente [IWMPCdromRip:: Get \_ ripProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripprogress). Questo metodo recupera un valore di avanzamento per l'intera operazione di estrazione. Il valore recuperato è un numero che rappresenta la percentuale di ripping completata. È possibile monitorare lo stato dell'operazione di strappo chiamando periodicamente [IWMPCdromRip:: Get \_ ripState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripstate). Questo metodo recupera un valore di enumerazione [WMPRipState](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate) che indica se l'operazione è in corso o è stata arrestata. È anche possibile monitorare lo stato dell'operazione di strappo gestendo l'evento [IWMPEvents3:: CdromRipStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripstatechange) . È necessario prestare attenzione a confrontare il puntatore **IWMPCdromRip** (fornito dall'evento) al puntatore che rappresenta l'operazione di estrazione per assicurarsi che l'evento sia stato generato dall'operazione. È possibile arrestare l'operazione di strappo chiamando [IWMPCdromRip:: stopRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-stoprip).

Per ricevere le notifiche di errore relative a un'operazione di ripping, è possibile gestire l'evento [IWMPEvents3:: CdromRipMediaError](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripmediaerror) . Analogamente a **CdromRipStateChange**, questo evento fornisce un puntatore all'interfaccia **IWMPCdromRip** che rappresenta l'operazione di strappo che ha generato l'evento. L'evento fornisce inoltre un puntatore **IDispatch** che rappresenta l'elemento multimediale che ha generato l'evento. È possibile chiamare **QueryInterface** tramite questo puntatore per recuperare un puntatore **IWMPMedia** .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sul modello a oggetti del lettore**](about-the-player-object-model.md)
</dt> </dl>

 

 




