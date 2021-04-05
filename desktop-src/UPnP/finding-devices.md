---
title: Ricerca di dispositivi
description: L'architettura UPnP è un'architettura di rete dinamica che consente ai dispositivi di aggiungersi e lasciare la rete in qualsiasi momento.
ms.assetid: b89d9ec3-ce1a-4162-bf82-b08a49207d7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5b8feebd430252b118353681a90ce4cd683ee7b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045179"
---
# <a name="finding-devices"></a>Ricerca di dispositivi

L'architettura UPnP è un'architettura di rete dinamica che consente ai dispositivi di aggiungersi e lasciare la rete in qualsiasi momento. Grazie a questa architettura dinamica, le applicazioni non possono basarsi su dispositivi specifici basati su UPnP per essere disponibili in un determinato momento. Per questo motivo, le applicazioni (o i punti di controllo) cercano la rete per individuare i dispositivi che soddisfano i criteri specificati. Le applicazioni attendono anche che i messaggi di annuncio del dispositivo che indicano la presenza di nuovi dispositivi siano stati aggiunti alla rete.

Di seguito sono riportati i criteri di ricerca validi per i dispositivi basati su UPnP:

-   Tipo di dispositivo
-   Tipo di servizio
-   Nome univoco del dispositivo (UDN)
-   Tutti i dispositivi radice

Il tipo di dispositivo e le ricerche del tipo di servizio vengono in genere usate per trovare una classe di dispositivi con caratteristiche comuni. La ricerca UDN viene usata per trovare un dispositivo specifico.

Per cercare i dispositivi, un'applicazione deve prima creare un'istanza dell'oggetto di ricerca del dispositivo. Questo oggetto espone l'interfaccia [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) ; i metodi eseguono le ricerche descritte in precedenza.

Le sezioni seguenti descrivono il processo di ricerca dei dispositivi:

-   [Creazione del dispositivo di ricerca](creating-the-device-finder.md)
-   [Ricerca asincrona](asynchronous-searching.md)
-   [Ricerca sincrona](synchronous-searching.md)
-   [Raccolte di dispositivi restituite da ricerche sincrone](device-collections-returned-by-synchronous-searches.md)

 

 




