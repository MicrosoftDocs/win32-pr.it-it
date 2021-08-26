---
description: Questo documento descrive la progettazione e l'uso delle classi di base MSP. L'uso di queste classi non è obbligatorio, ma la maggior parte degli sviluppatori scoprirà che semplificano l'attività di creazione di un msp basato su DirectShow per TAPI 3s nuovo MSPI.
ms.assetid: 97597dcf-eb18-47aa-b0ed-a43286d5d134
title: Classi di base TAPI 3 MSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee34d4f9f67618c3637bfaff149773ab7b0de4b93f33c8bca8e5eb892527735e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012341"
---
# <a name="tapi-3-msp-base-classes"></a>Classi di base TAPI 3 MSP

Questo documento descrive la progettazione e l'uso delle classi di base MSP. L'uso di queste classi non è obbligatorio, ma la maggior parte degli sviluppatori scoprirà che semplificano l'attività di creazione di un msp basato su DirectShow per il nuovo MSPI di TAPI 3.

Il codice sorgente per le classi di base MSP è disponibile nella directory Samples di Platform Software Development Kit (SDK).

Si presuppone una certa familiarità con COM, ATL, DirectShow e C++. Il lettore deve anche conoscere il materiale generale in About [the Media Service Provider (MSP) e](about-the-media-service-provider-msp-.md) in Media Service Provider Interface [(MSPI).](media-service-provider-interface-mspi-.md)

ATL 2.1 è necessario per Windows 2000. A partire Windows XP, atl 2.1 e 3.0 verranno compilati.

Librerie di classi di base MSP (disponibili nell'SDK):

-   Mspbase.lib
-   Mspid.lib
-   Strmbase.lib
-   Tmuid.lib
    > [!Note]  
    > È consigliabile usare il collegamento dinamico anziché statico.

     

File di intestazione della classe di base MSP (disponibili nell'SDK):

-   Mspaddr.h
-   Mspbase.h
-   Mspcall.h
-   Msplog.h
-   Mspstrm.h
-   Mspterm.h
-   Mspthrd.h
-   Msptmac.h
-   Msptmvc.h
-   Msptrmvc.h
-   Msptrmac.h
-   Msptrmar.h
-   Msputils.h

File di origine della classe di base MSP (disponibili negli esempi sdk):

-   Mspaddr.cpp
-   Mspcall.cpp
-   Msplog.cpp
-   Mspstrm.cpp
-   Mspterm.cpp
-   Mspthrd.cpp
-   Msptrmac.cpp
-   Msptrmar.cpp
-   Msptrmvc.cpp
-   Msputils.cpp

 

 



