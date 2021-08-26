---
title: Informazioni sullo scheggiamento cd
description: Informazioni sullo scheggiamento cd
ms.assetid: 1a179284-2909-4fc0-82be-996794ee4f31
keywords:
- Windows Media Player,ripping CD
- Windows Media Player a oggetti, ripping CD
- modello a oggetti, ripping CD
- Windows Media Player ActiveX controllo, ripping CD
- ActiveX, ripping CD
- Windows Media Player Controllo ActiveX per dispositivi mobili, ripping CD
- Windows Media Player Mobile, ripping CD
- ripping cd, informazioni
- ripping di CD, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0efab14a97f9cc24c4137e5d939bc9562b1fc073cd551bd83388de4ba1de0b65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903601"
---
# <a name="about-cd-ripping"></a>Informazioni sullo scheggiamento cd

L Windows Media Player 11 SDK introduce nuove funzionalità per la copia di tracce audio dai CD al computer dell'utente. Questo processo è denominato *ripping* di .

Quando si copiano tracce audio usando le interfacce di Windows Media Player SDK, le tracce musicali risultanti vengono create  usando le impostazioni definite dall'utente nella finestra di dialogo Windows Media Player Opzioni.

Per enumerare le unità CD nel computer dell'utente, usare **l'interfaccia IWMPCdromCollection.** Per recuperare un puntatore a questa interfaccia, chiamare [IWMPCore::get \_ cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection). Usando i **metodi count** e **item,** è possibile scorrere la raccolta per recuperare un puntatore a interfaccia **IWMPCdrom** per ogni unità CD nel computer dell'utente. **L'interfaccia IWMPCdrom** rappresenta una singola unità CD. Prima di iniziare a copiare un CD, è necessario chiamare **QueryInterface** tramite un puntatore **IWMPCdrom** per recuperare un puntatore all'interfaccia **IWMPCdromRip.**

Per avviare l'operazione di ripping, è sufficiente chiamare [IWMPCdromRip::startRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-startrip). È possibile monitorare lo stato dell'operazione di ripping chiamando periodicamente [IWMPCdromRip::get \_ ripProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripprogress). Questo metodo recupera un valore di stato per l'intera operazione di ripping. Il valore recuperato è un numero che rappresenta la percentuale di ripping completato. È possibile monitorare lo stato dell'operazione di ripping chiamando periodicamente [IWMPCdromRip::get \_ ripState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripstate). Questo metodo recupera un [valore di enumerazione WMPRipState](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate) che indica se l'operazione è in corso o arrestata. È anche possibile monitorare lo stato dell'operazione di ripping gestendo l'evento [IWMPEvents3::CdromRipStateChange.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripstatechange) È necessario fare attenzione a confrontare il puntatore **IWMPCdromRip** (fornito dall'evento) con il puntatore che rappresenta l'operazione di depping per assicurarsi che l'evento sia stato generato dall'operazione. È possibile arrestare l'operazione di ripping chiamando [IWMPCdromRip::stopRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-stoprip).

Per ricevere notifiche di errore relative a un'operazione di depping, è possibile gestire l'evento [IWMPEvents3::CdromRipMediaError.](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripmediaerror) Come **CdromRipStateChange,** questo evento fornisce un puntatore a interfaccia **IWMPCdromRip** che rappresenta l'operazione di ripping che ha generato l'evento. L'evento fornisce anche un **puntatore IDispatch** che rappresenta l'elemento multimediale che ha generato l'evento. È possibile chiamare **QueryInterface tramite** questo puntatore per recuperare un **puntatore IWMPMedia.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sul modello a oggetti del lettore**](about-the-player-object-model.md)
</dt> </dl>

 

 




