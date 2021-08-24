---
description: WiA viene implementato come server out-of-process Component Object Model (COM) per garantire il funzionamento affidabile delle applicazioni client.
ms.assetid: 9f3d1848-36ab-4e0f-a7f4-312bc85ecc00
title: Architettura WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 159a6bb88fba5a79f2915500786bbfcf8d531bfe0170ec6c6841f419425ee296
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813266"
---
# <a name="wia-architecture"></a>Architettura WIA

WiA viene implementato come server out-of-process Component Object Model (COM) per garantire il funzionamento affidabile delle applicazioni client. A differenza della maggior parte delle applicazioni server out-of-process, Windows Image Acquisition (WIA) evita le penalità delle prestazioni durante il trasferimento dei dati di immagine fornendo il proprio meccanismo di trasferimento dei dati, [**IWiaDataTransfer.**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) Questa interfaccia a prestazioni elevate usa una finestra di memoria condivisa per trasferire i dati al client.

WIA ha tre componenti principali: Gestione dispositivi, una libreria del servizio Minidriver e un minidriver per dispositivi.

-   Gestione dispositivi enumera i dispositivi di creazione di immagini, recupera le proprietà del dispositivo, configura gli eventi per i dispositivi e crea oggetti dispositivo.
-   La libreria del servizio Minidriver implementa tutti i servizi indipendenti dal dispositivo.
-   Device Minidriver esegue il mapping delle proprietà e dei comandi WIA al dispositivo specifico.

Il diagramma seguente illustra l'architettura WIA:

![Architettura wia](images/wiarch.gif)

 

 



