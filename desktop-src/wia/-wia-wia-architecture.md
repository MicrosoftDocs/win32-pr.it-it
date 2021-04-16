---
description: WIA viene implementato come un server out-of-process Component Object Model (COM) per assicurare il funzionamento affidabile delle applicazioni client.
ms.assetid: 9f3d1848-36ab-4e0f-a7f4-312bc85ecc00
title: Architettura WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09652258ee249fb3c68e65472e863ccd35154ee5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104568347"
---
# <a name="wia-architecture"></a>Architettura WIA

WIA viene implementato come un server out-of-process Component Object Model (COM) per assicurare il funzionamento affidabile delle applicazioni client. A differenza della maggior parte delle applicazioni del server di elaborazione, l'acquisizione di immagini Windows (WIA) evita le penalizzazioni delle prestazioni durante il trasferimento dei dati delle immagini fornendo un proprio meccanismo di trasferimento dei dati, [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer). Questa interfaccia a prestazioni elevate usa una finestra di memoria condivisa per trasferire i dati al client.

WIA include tre componenti principali: un Gestione dispositivi, una libreria di servizi minidriver e un dispositivo minidriver.

-   Il Gestione dispositivi enumera i dispositivi di imaging, recupera le proprietà del dispositivo, imposta gli eventi per i dispositivi e crea oggetti dispositivo.
-   La libreria del servizio minidriver implementa tutti i servizi indipendenti dal dispositivo.
-   Il dispositivo minidriver esegue il mapping delle proprietà e dei comandi WIA al dispositivo specifico.

Il diagramma seguente illustra l'architettura WIA:

![architettura WIA](images/wiarch.gif)

 

 



