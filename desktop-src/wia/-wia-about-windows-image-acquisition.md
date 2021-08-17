---
description: L'Windows di acquisizione di immagini (WIA) è sia un'API che un'interfaccia DDI (Device Driver Interface).
ms.assetid: 725543f8-6e33-4e22-904c-95cbec0388c8
title: Informazioni Windows'acquisizione di immagini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d73662083e568a109760a052994bfcbebdfcbe53f858e50a89728a01bba344d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119451301"
---
# <a name="about-windows-image-acquisition"></a>Informazioni Windows'acquisizione di immagini

L'Windows di acquisizione di immagini (WIA) è sia un'API che un'interfaccia DDI (Device Driver Interface). L'API WIA è progettata per consentire alle applicazioni di:

-   Eseguire in un ambiente solido e stabile.
-   Ridurre al minimo i problemi di interoperabilità.
-   Enumerare i dispositivi di acquisizione delle immagini disponibili.
-   Creare connessioni a più dispositivi contemporaneamente.
-   Eseguire query delle proprietà dei dispositivi in modo standard ed espandibile.
-   Acquisire i dati dei dispositivi usando meccanismi di trasferimento standard e ad alte prestazioni.
-   Mantenere le proprietà dell'immagine tra i trasferimenti di dati.
-   Ricevere una notifica di un'ampia gamma di eventi del dispositivo.

WIADDI è progettato per ridurre al minimo la quantità di codice che un fornitore di hardware deve scrivere, mantenendo la flessibilità necessaria per creare singole soluzioni. Questa operazione viene eseguita da:

-   Fornire una libreria di servizi di dispositivi standard che esegue la maggior parte delle operazioni sui driver.
-   Promuovere gli standard di comunicazione dei dispositivi del settore in modo che un driver WIA supporti la maggior parte dei dispositivi WIA. Ad esempio, Picture Transfer Protocol (PTP).
-   Consentire al driver di dispositivo di supportare interfacce personalizzate, senza richiedere l'uso della libreria del servizio dispositivo standard. Tuttavia, i driver devono comunque implementare le interfacce WIA standard.

Questa sezione presenta una breve panoramica dell'interfaccia WIA nelle aree seguenti:

-   [Architettura WIA](-wia-wia-architecture.md)
-   [Compatibilità sti](-wia-sti-compatibility.md)
-   [Compatibilità con TWAIN](-wia-twain-compatibility.md)
-   [Gestione dispositivi WIA](-wia-wia-device-manager.md)
-   [Libreria del servizio WiA Minidriver](-wia-wia-minidriver-service-library.md)
-   [WIA Minidriver](-wia-wia-minidriver.md)

 

 



