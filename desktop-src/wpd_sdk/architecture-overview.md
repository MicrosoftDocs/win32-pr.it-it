---
description: Panoramica dell'architettura
ms.assetid: ff20d83a-e9cd-46e9-95f7-3ebdf791e667
title: Panoramica dell'architettura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15f911a14e60465efc8f8f8d798b7ddf527bf4e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884914"
---
# <a name="architecture-overview"></a>Panoramica dell'architettura

L'architettura WPD può essere divisa in tre processi. All'interno di questi processi si trovano i tre componenti principali di WPD: l'API, il serializzatore e il driver. Nella figura seguente vengono illustrati i processi e i componenti che costituiscono l'architettura WPD.

![illustrazione che mostra i componenti API, serializer e driver di WPD](images/wpd-overview-figure1.gif)

## <a name="the-wpd-application-programming-interface"></a>Interfaccia di programmazione dell'applicazione WPD

L'API WPD viene implementata come un server COM in-process. L'API usa le API Microsoft Win32 standard per comunicare con il driver WPD appropriato. Un componente denominato serializzatore WPD viene usato sia dagli oggetti API che dal driver per comprimere o decomprimere i parametri da e verso i buffer di Windows Driver Foundation (CDR)-modalità utente (UMDF).

## <a name="the-wpd-serializer"></a>Serializzatore WPD

Il serializzatore WPD viene implementato come un server COM in-process. L'API WPD usa il serializzatore per comprimere i comandi e i parametri in buffer di messaggi inviati al driver. Il driver utilizza il serializzatore per decomprimere i buffer dei messaggi per l'elaborazione. Il driver usa anche il serializzatore per comprimere i dati e i parametri nei buffer di risposta restituiti all'API WPD e l'API WPD usa il serializzatore per decomprimere i buffer di risposta per tornare ai chiamanti.

## <a name="wpd-driver"></a>Driver WPD

Il driver WPD viene implementato come driver standard di Windows Driver Foundation (CDR)-User-Mode Driver Framework (UMDF). I driver WPD sono ospitati da UMDF in un processo separato denominato host driver.

Il driver riceve i messaggi dal riflettore UMDF (questa operazione non viene mostrata nel diagramma, poiché il modo in cui vengono ricevuti i buffer non è importante per il driver. Per ulteriori informazioni, vedere la documentazione di UMDF. Il driver implementa un gestore IOCL (WPD) specifico per elaborare i messaggi WPD ricevuti dall'API WPD. Il driver usa il serializzatore WPD per decomprimere i comandi e i parametri da questi buffer dei messaggi e per comprimere la risposta nel buffer restituito.

I driver WPD possono comunicare con i dispositivi tramite un driver in modalità kernel, in genere accessibili tramite operazioni su file Win32, ovvero CreateFile, ReadFile, WriteFile e così via. Per gli autobus comuni, Microsoft fornirà i driver del kernel standard che i fornitori utilizzeranno per consentire ai fornitori di fornire una soluzione driver solo in modalità utente. Inoltre, per i dispositivi MTP (Media Transfer Protocol) e di classe di archiviazione di massa (MSC), Microsoft fornirà i driver della classe WPD.

Per ulteriori informazioni sui driver WPD, vedere la documentazione del driver dei dispositivi portatili Windows in Windows Driver Kit.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Panoramica dell'applicazione**](application-overview.md)
</dt> </dl>

 

 



