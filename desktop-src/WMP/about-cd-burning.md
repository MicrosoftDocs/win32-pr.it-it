---
title: Informazioni sulla masterizzazione di CD
description: Informazioni sulla masterizzazione di CD
ms.assetid: 1ecc73ed-c49d-4190-baa9-93162f075a4c
keywords:
- Windows Media Player, masterizzazione CD
- Modello a oggetti di Windows Media Player, masterizzazione CD
- modello a oggetti, masterizzazione CD
- Controllo ActiveX Windows Media Player, masterizzazione CD
- Controllo ActiveX, masterizzazione CD
- Controllo ActiveX Windows Media Player Mobile, masterizzazione CD
- Windows Media Player Mobile, masterizzazione CD
- Masterizzazione CD, informazioni
- masterizzazione di CDs, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc921080d02bef6ffbf916fe4d7d1df09f1e8bbc
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/21/2020
ms.locfileid: "103724053"
---
# <a name="about-cd-burning"></a>Informazioni sulla masterizzazione di CD

Windows Media Player 11 SDK introduce nuove funzionalità per la creazione di CDs. Questo processo è denominato *Burning*.

Per enumerare le unità CD nel computer dell'utente, usare l'interfaccia **IWMPCdromCollection** . Per recuperare un puntatore a questa interfaccia, chiamare [IWMPCore:: Get \_ cdromcollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection). Utilizzando i metodi **count** e **Item** , è possibile eseguire l'iterazione della raccolta per recuperare un puntatore di interfaccia **IWMPCdrom** per ogni unità CD nel computer dell'utente. L'interfaccia **IWMPCdrom** rappresenta una singola unità CD.

Prima di iniziare a masterizzare un CD, è prima necessario chiamare **QueryInterface** tramite un puntatore **IWMPCdrom** per recuperare un puntatore all'interfaccia **IWMPCdromBurn** . Utilizzando **il metodo IsValid** , è possibile determinare se un'unità CD specifica può masterizzare CDS, se è presente un CD nell'unità e come è possibile utilizzare il CD.

Per specificare gli elementi da masterizzare su CD, è necessario creare una playlist. Windows Media Player rappresenta le playlist usando l'interfaccia **IWMPPlaylist** . È possibile creare questa playlist in qualsiasi modo. Ad esempio, è possibile recuperare semplicemente una playlist dalla libreria chiamando [IWMPMediaCollection:: getByAlbum](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getbyalbum). Dopo aver creato la playlist che si vuole masterizzare su CD, è necessario chiamare il metodo [IWMPCdromBurn::p UT \_ burnPlaylist](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnplaylist) e passare il puntatore della playlist come argomento. Questa operazione consente di impostare la playlist come quella che verrà copiata da Windows Media Player nel CD.

Se si recupera una playlist dalla libreria, tutte le modifiche apportate alla playlist verranno riflesse nella libreria dell'utente. Per evitare questo problema, chiamare [IWMPPlaylist:: setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-setiteminfo), passando il nome di attributo "Temporary" e il valore "true". Questa operazione converte l'istanza della playlist in una playlist temporanea, che può essere modificata senza modificare la playlist originale.

Ogni volta che si imposta una nuova playlist per la masterizzazione o si apportano modifiche a una playlist Burn esistente, è necessario chiamare [IWMPCdromBurn:: refreshStatus](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-refreshstatus) per aggiornare le informazioni sullo stato. Ciò garantisce che Windows Media Player esegue l'elaborazione necessaria per fornire informazioni accurate sullo stato per l'operazione di masterizzazione del CD.

Per specificare il tipo di CD da masterizzare, chiamare [IWMPCdromBurn::p UT \_ burnFormat](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnformat). Windows Media Player consente di masterizzare due tipi di CDs, ovvero CD audio e CD di dati. L'enumerazione [WMPBurnFormat](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnformat) definisce i tipi di CD.

È possibile specificare un'etichetta di volume per il CD chiamando [IWMPCdromBurn::p UT \_ Label](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_label).

Quando si è pronti per iniziare la masterizzazione del CD, chiamare [IWMPCdromBurn:: startBurn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-startburn). È possibile monitorare lo stato di avanzamento dell'operazione di masterizzazione chiamando periodicamente [IWMPCdromBurn:: Get \_ burnProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnprogress). Questo metodo recupera un valore di avanzamento per l'intera operazione di masterizzazione. Il valore recuperato è un numero che rappresenta la percentuale di masterizzazione completata. È possibile monitorare lo stato dell'operazione di masterizzazione gestendo l'evento [IWMPEvents3:: CdromBurnStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromburnstatechange) , che usa l'enumerazione [WMPBurnState](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate) per indicare lo stato corrente. È necessario prestare attenzione a confrontare il puntatore **IWMPCdromBurn** (fornito dall'evento) al puntatore che rappresenta l'operazione di masterizzazione per garantire che l'evento sia stato generato dall'operazione. È possibile arrestare l'operazione di masterizzazione chiamando [IWMPCdromBurn:: stopBurn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-stopburn).

Sono disponibili due eventi che è possibile gestire per ricevere le notifiche di errore relative all'operazione di masterizzazione. Quando si verifica un errore generico, viene generato l'evento [IWMPEvents3:: CdromBurnError](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromburnerror) . [IWMPEvents3:: CdromBurnMediaError](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromburnmediaerror) viene generato quando un particolare elemento multimediale genera un errore durante la combustione. Analogamente all'evento **CdromBurnStateChange** , ognuno di questi eventi fornisce un puntatore **IWMPCdromBurn** che rappresenta l'operazione di masterizzazione che ha generato l'evento. L'evento **CdromBurnMediaError** fornisce un puntatore **IDispatch** che rappresenta l'elemento multimediale che ha generato l'evento. È possibile chiamare **QueryInterface** tramite questo puntatore per recuperare un puntatore **IWMPMedia** .

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

 

 




