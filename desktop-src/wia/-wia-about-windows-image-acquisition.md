---
description: L'interfaccia Windows Image Acquisition (WIA) è un'API e un'interfaccia DDI (Device Driver Interface).
ms.assetid: 725543f8-6e33-4e22-904c-95cbec0388c8
title: Informazioni sull'acquisizione di immagini Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80eed6289f7a30476ea6889c947577ad003b656e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312460"
---
# <a name="about-windows-image-acquisition"></a>Informazioni sull'acquisizione di immagini Windows

L'interfaccia Windows Image Acquisition (WIA) è un'API e un'interfaccia DDI (Device Driver Interface). L'API WIA è progettata per consentire alle applicazioni di:

-   Eseguire in un ambiente solido e stabile.
-   Ridurre al minimo i problemi di interoperabilità.
-   Enumera i dispositivi di acquisizione immagini disponibili.
-   Consente di creare connessioni a più dispositivi contemporaneamente.
-   Eseguire query sulle proprietà dei dispositivi in modo standard ed espandibile.
-   Acquisisci i dati del dispositivo usando meccanismi di trasferimento standard e ad alte prestazioni.
-   Gestire le proprietà delle immagini nei trasferimenti di dati.
-   Ricevere una notifica relativa a un'ampia gamma di eventi del dispositivo.

Il WIADDI è progettato per ridurre al minimo la quantità di codice che un fornitore di hardware deve scrivere, mantenendo al tempo stesso la flessibilità necessaria per creare singole soluzioni. Questa operazione viene eseguita da:

-   Fornire una libreria di servizi per dispositivi standard che esegue la maggior parte delle operazioni del driver.
-   Promozione degli standard di comunicazione dei dispositivi del settore in modo che un driver WIA supporti la maggior parte dei dispositivi WIA. Ad esempio, il protocollo PTP (Picture Transfer Protocol).
-   Consentire al driver di dispositivo di supportare interfacce personalizzate, senza richiedere l'uso della libreria del servizio del dispositivo standard. Tuttavia, i driver devono comunque implementare le interfacce standard WIA.

In questa sezione viene presentata una breve panoramica dell'interfaccia WIA nelle seguenti aree:

-   [Architettura WIA](-wia-wia-architecture.md)
-   [Compatibilità STI](-wia-sti-compatibility.md)
-   [Compatibilità con TWAIN](-wia-twain-compatibility.md)
-   [Gestione dispositivi WIA](-wia-wia-device-manager.md)
-   [Libreria di servizi WIA minidriver](-wia-wia-minidriver-service-library.md)
-   [Minidriver WIA](-wia-wia-minidriver.md)

 

 



