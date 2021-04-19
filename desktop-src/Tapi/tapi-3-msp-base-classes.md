---
description: Questo documento descrive la progettazione e l'uso delle classi di base MSP. L'uso di queste classi non è obbligatorio, ma la maggior parte degli sviluppatori troverà l'attività di creazione di un MSP basato su DirectShow per TAPI 3 New MSPI.
ms.assetid: 97597dcf-eb18-47aa-b0ed-a43286d5d134
title: Classi base MSP di TAPI 3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb7c7958847ef7bf699cfe4810f7133ef0b4bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317644"
---
# <a name="tapi-3-msp-base-classes"></a>Classi base MSP di TAPI 3

Questo documento descrive la progettazione e l'uso delle classi di base MSP. L'uso di queste classi non è obbligatorio, ma la maggior parte degli sviluppatori troverà l'attività di creazione di un MSP basato su DirectShow per la nuova MSPI di TAPI 3.

Il codice sorgente per le classi base MSP si trova nella directory Samples di Platform Software Development Kit (SDK).

Si presuppone una certa familiarità con COM, ATL, DirectShow e C++. Il lettore deve inoltre conoscere il materiale generale in [informazioni sul provider di servizi multimediali (msp)](about-the-media-service-provider-msp-.md) e in [Media Service Provider Interface (MSPI)](media-service-provider-interface-mspi-.md).

Per Windows 2000 è necessario ATL 2,1. A partire da Windows XP, vengono compilati sia ATL 2,1 che 3,0.

Librerie di classi base MSP (disponibili nell'SDK):

-   Mspbase. lib
-   Mspid. lib
-   Strmbase. lib
-   Tmuid. lib
    > [!Note]  
    > È necessario utilizzare il collegamento dinamico anziché quello statico.

     

File di intestazione della classe di base MSP (disponibili nell'SDK):

-   Mspaddr. h
-   Mspbase. h
-   Mspcall. h
-   Msplog. h
-   Mspstrm. h
-   Mspterm. h
-   Mspthrd. h
-   Msptmac. h
-   Msptmvc. h
-   Msptrmvc. h
-   Msptrmac. h
-   Msptrmar. h
-   Msputils. h

File di origine della classe di base MSP (disponibili negli esempi di SDK):

-   Mspaddr. cpp
-   Mspcall. cpp
-   Msplog. cpp
-   Mspstrm. cpp
-   Mspterm. cpp
-   Mspthrd. cpp
-   Msptrmac. cpp
-   Msptrmar. cpp
-   Msptrmvc. cpp
-   Msputils. cpp

 

 



