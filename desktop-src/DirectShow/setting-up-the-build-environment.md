---
description: Compilazione di applicazioni DirectShow
ms.assetid: 2fbdbe49-0d4d-4dce-afc3-7049c793ace0
title: Compilazione di applicazioni DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56c6ab8a0731e93eece734abd4380b092414ff5f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303693"
---
# <a name="building-directshow-applications"></a>Compilazione di applicazioni DirectShow

Questo argomento descrive le intestazioni e le librerie necessarie per compilare applicazioni DirectShow.

Le intestazioni e le librerie DirectShow più recenti sono disponibili nell' [Windows SDK](https://msdn.microsoft.com/windows/aa904949.aspx).

## <a name="header-files"></a>File di intestazione

Tutte le applicazioni DirectShow utilizzano il file di intestazione illustrato nella tabella seguente.



| File di intestazione | Obbligatorio per                 |
|-------------|------------------------------|
| Dshow. h     | Tutte le applicazioni DirectShow. |



 

Per alcune interfacce DirectShow sono necessari file di intestazione aggiuntivi. Questi requisiti sono indicati nella Guida di riferimento all'interfaccia.

## <a name="library-files"></a>File di libreria

DirectShow usa i file di libreria statici indicati nella tabella seguente.



| File di libreria | Descrizione                                                                                                                    |
|--------------|--------------------------------------------------------------------------------------------------------------------------------|
| Strmiids. lib | Esporta gli identificatori di classe (CLSID) e gli identificatori di interfaccia (IID).                                                           |
| Quartz. lib   | Esporta la funzione [**AMGetErrorText**](/windows/win32/api/errors/nf-errors-amgeterrortexta) . Se non si chiama questa funzione, questa libreria non è obbligatoria. |



 

Utilizzare gli stessi file con estensione LIB per le compilazioni di debug e di rilascio.

## <a name="filter-base-classes"></a>Filtrare le classi base

Il Windows SDK fornisce un set di classi C++ consigliate Se si sta scrivendo un filtro DirectShow personalizzato. Queste classi vengono fornite come codice di esempio, che è possibile compilare in una libreria statica. Per altre informazioni, vedere [classi base di DirectShow](directshow-base-classes.md).

## <a name="redistributable-dlls"></a>DLL ridistribuibili

Per le applicazioni DirectShow scritte per Windows XP con Service Pack 2 (SP2) e versioni successive non è necessario ridistribuire le dll DirectShow.

Per Windows XP con Service Pack 1 (SP1) e versioni precedenti, le dll DirectShow ridistribuibili sono disponibili in Microsoft DirectX SDK. La versione più recente di queste dll è la versione 9.0 c. Non è pianificato alcun ulteriore sviluppo di queste DLL ridistribuibili. Windows XP con Service Pack 2 (SP2) contiene le dll della versione 9.0 c.

I pacchetti Redstributable contengono le DLL seguenti:

-   dxnt.cab
    -   amstream.dll
    -   devenum.dll
    -   encapi.dll
    -   ks.sys
    -   ksolay.ax
    -   ksproxy.ax
    -   ksuser.dll
    -   l3codecx.ax
    -   mciqtz32.dll
    -   mpg2splt.ax
    -   msdmo.dll
    -   mskssrv.sys
    -   mspclock.sys
    -   mspqm.sys
    -   mstee.sys
    -   mswebdvd.dll
    -   qasf.dll
    -   qcap.dll
    -   qdv.dll
    -   qdvd.dll
    -   qedit.dll
    -   qedwipes.dll
    -   quartz.dll
    -   stream.sys
    -   swenum.sys
-   bda.cab
    -   bdaplgin.ax
    -   bdasup.sys
    -   ccdecode.sys
    -   ipsink.ax
    -   kstvtune.ax
    -   kswdmcap.ax
    -   ksxbar.ax
    -   mpe.sys
    -   mpeg2data.ax
    -   msdv.sys
    -   msdvbnp.ax
    -   msvidctl.dll
    -   msyuv.dll
    -   nabtsfec.sys
    -   ndisip.sys
    -   psisdecd.dll
    -   psisrndr.ax
    -   slip.sys
    -   streamip.sys
    -   vbisurf.ax
    -   wstcodec.sys
    -   wstdecod.dll

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di filtri DirectShow](building-directshow-filters.md)
</dt> </dl>

 

 
