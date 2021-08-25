---
title: Ricerca di dispositivi
description: L'architettura UPnP è un'architettura di rete dinamica che consente ai dispositivi di aggiungersi e uscire dalla rete in qualsiasi momento.
ms.assetid: b89d9ec3-ce1a-4162-bf82-b08a49207d7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccf5626f7d941d9e3fa73b6d3d46ef9f51ef256ee8371e7594c312d225bba865
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867591"
---
# <a name="finding-devices"></a>Ricerca di dispositivi

L'architettura UPnP è un'architettura di rete dinamica che consente ai dispositivi di aggiungersi e uscire dalla rete in qualsiasi momento. A causa di questa architettura dinamica, le applicazioni non possono basarsi su dispositivi specifici basati su UPnP per essere disponibili in qualsiasi momento. Per questo motivo, le applicazioni (o i punti di controllo) e ricercano nella rete i dispositivi che corrispondono maggiormente ai criteri specificati. Le applicazioni attendono anche messaggi di annuncio del dispositivo che indicano che sono stati aggiunti nuovi dispositivi alla rete.

Di seguito sono riportati i criteri di ricerca validi per i dispositivi basati su UPnP:

-   Tipo di dispositivo
-   Tipo di servizio
-   Nome univoco del dispositivo (UDN)
-   Tutti i dispositivi radice

Le ricerche del tipo di dispositivo e del tipo di servizio vengono in genere usate per trovare una classe di dispositivi con caratteristiche comuni. La ricerca UDN viene usata per trovare un dispositivo specifico.

Per cercare i dispositivi, un'applicazione deve prima creare un'istanza dell'oggetto Device Finder. Questo oggetto espone [**l'interfaccia IUPnPDeviceFinder.**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) I relativi metodi eseguono le ricerche descritte in precedenza.

Le sezioni seguenti descrivono il processo di ricerca dei dispositivi:

-   [Creazione di Device Finder](creating-the-device-finder.md)
-   [Ricerca asincrona](asynchronous-searching.md)
-   [Ricerca sincrona](synchronous-searching.md)
-   [Raccolte di dispositivi restituite da ricerche sincrone](device-collections-returned-by-synchronous-searches.md)

 

 




