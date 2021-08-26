---
title: Informazioni sulla masterizzazione di CD
description: Informazioni sulla masterizzazione di CD
ms.assetid: 1ecc73ed-c49d-4190-baa9-93162f075a4c
keywords:
- Windows Media Player,masterizzazione CD
- Windows Media Player a oggetti, masterizzazione CD
- modello a oggetti, masterizzazione CD
- Windows Media Player ActiveX controllo, masterizzazione CD
- ActiveX controllo, masterizzazione CD
- Windows Media Player Controllo ActiveX per dispositivi mobili, masterizzazione CD
- Windows Media Player Mobile, masterizzazione CD
- masterizzazione cd, informazioni su
- masterizzazione di CD, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c784765a09b601da2f0ec75434a37f55a75ff7e6ab6d737f7912daab8f197c07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957141"
---
# <a name="about-cd-burning"></a>Informazioni sulla masterizzazione di CD

L Windows Media Player 11 SDK introduce nuove funzionalità per la creazione di CD. Questo processo è denominato *masterizzazione* di .

Per enumerare le unità CD nel computer dell'utente, usare **l'interfaccia IWMPCdromCollection.** Per recuperare un puntatore a questa interfaccia, chiamare [IWMPCore::get \_ cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection). Usando i **metodi count** e **item,** è possibile scorrere la raccolta per recuperare un puntatore a interfaccia **IWMPCdrom** per ogni unità CD nel computer dell'utente. **L'interfaccia IWMPCdrom** rappresenta una singola unità CD.

Prima di iniziare a masterizzare un CD, è necessario chiamare **QueryInterface** tramite un puntatore **IWMPCdrom** per recuperare un puntatore all'interfaccia **IWMPCdromBurn.** Usando il metodo **isAvailable** è possibile determinare se una determinata unità CD può masterizzare CD, se è presente un CD nell'unità e come può essere usato il CD.

Per specificare gli elementi da masterizzare su CD, è necessario creare una playlist. Windows Media Player le playlist usando **l'interfaccia IWMPPlaylist.** È possibile creare questa playlist nel modo che si desidera. Ad esempio, è possibile recuperare semplicemente una playlist dalla libreria chiamando [IWMPMediaCollection::getByAlbum](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getbyalbum). Dopo aver creato la playlist da masterizzare su CD, è necessario chiamare il metodo [IWMPCdromBurn::p ut \_ burnPlaylist](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnplaylist) e passare il puntatore della playlist come argomento. In questo modo la playlist viene impostata come Windows Media Player copiata nel CD.

Se si recupera una playlist dalla libreria, tutte le modifiche apportate alla playlist verranno riflesse nella libreria dell'utente. Per evitare questo problema, chiamare [IWMPPlaylist::setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-setiteminfo), passando il nome dell'attributo "Temporary" e il valore "true". In questo modo l'istanza di playlist viene convertita in una playlist temporanea, che può essere modificata senza modificare la playlist originale.

Ogni volta che si imposta una nuova playlist per la masterizzazione o si apportano modifiche a una playlist di masterizzazione esistente, è necessario chiamare [IWMPCdromBurn::refreshStatus](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-refreshstatus) per aggiornare le informazioni sullo stato. Ciò garantisce che Windows Media Player l'elaborazione necessaria per fornire informazioni di stato accurate per l'operazione di masterizzazione cd.

Per specificare il tipo di CD da masterizzare, chiamare [IWMPCdromBurn::p ut \_ burnFormat](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnformat). Windows Media Player consente di masterizzare due tipi di CD: CD audio e CD dati. [L'enumerazione WMPKindFormat](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnformat) definisce i tipi di CD.

È possibile specificare un'etichetta di volume per il CD chiamando [IWMPCdromBurn::p ut \_ label](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_label).

Quando si è pronti per iniziare a masterizzare il CD, chiamare [IWMPCdromBurn::startBurn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-startburn). È possibile monitorare lo stato dell'operazione di masterizzazione chiamando periodicamente [IWMPCdromBurn::get \_ burnProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnprogress). Questo metodo recupera un valore di stato per l'intera operazione di masterizzazione. Il valore recuperato è un numero che rappresenta la percentuale di masterizzazione completata. È possibile monitorare lo stato dell'operazione di masterizzazione gestendo l'evento [IWMPEvents3::CdromKindStateChange,](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromburnstatechange) che usa l'enumerazione [WMPKindState](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate) per indicare lo stato corrente. È necessario fare attenzione a confrontare il puntatore **IWMPCdromBurn** (fornito dall'evento) con il puntatore che rappresenta l'operazione di masterizzazione per assicurarsi che l'evento sia stato generato dall'operazione. È possibile arrestare l'operazione di masterizzazione chiamando [IWMPCdromBurn::stopBurn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-stopburn).

Esistono due eventi che è possibile gestire per ricevere notifiche di errore relative all'operazione di masterizzazione. [L'evento IWMPEvents3::CdromBurnError](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromburnerror) viene generato quando si verifica un errore generico. [IWMPEvents3::CdromBurnMediaError](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromburnmediaerror) viene generato quando un particolare elemento multimediale causa un errore durante la masterizzazione. Analogamente **all'evento CdromBurnStateChange,** ognuno di questi eventi fornisce un **puntatore IWMPCdromBurn** che rappresenta l'operazione di masterizzazione che ha generato l'evento. **L'evento CdromBurnMediaError** fornisce un **puntatore IDispatch** che rappresenta l'elemento multimediale che ha generato l'evento. È possibile chiamare **QueryInterface tramite** questo puntatore per recuperare un **puntatore IWMPMedia.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sul modello a oggetti del lettore**](about-the-player-object-model.md)
</dt> <dt>

[**Interfaccia IWMPCdrom**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom)
</dt> <dt>

[**Interfaccia IWMPCdromBurn**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)
</dt> <dt>

[**Interfaccia IWMPCdromCollection**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> <dt>

[**Interfaccia IWMPEvents3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)
</dt> <dt>

[**Interfaccia IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[**Interfaccia IWMPPlaylist**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)
</dt> <dt>

[**Attributo temporaneo**](temporary-attribute.md)
</dt> </dl>

 

 




