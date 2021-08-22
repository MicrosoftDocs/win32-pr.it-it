---
description: Panoramica dell'architettura
ms.assetid: ff20d83a-e9cd-46e9-95f7-3ebdf791e667
title: Panoramica dell'architettura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76eafce326655a4d9386d37c02df9ef0ab2b9772b5e87eedaff40a19383b2cec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590467"
---
# <a name="architecture-overview"></a>Panoramica dell'architettura

L'architettura WPD può essere suddivisa in tre processi. All'interno di questi processi sono presenti i tre componenti principali di WPD: l'API, il serializzatore e il driver. La figura seguente illustra i processi e i componenti che costituiscono l'architettura WPD.

![illustrazione che mostra i componenti api, serializzatore e driver di wpd](images/wpd-overview-figure1.gif)

## <a name="the-wpd-application-programming-interface"></a>The WPD Application Programming Interface

L'API WPD viene implementata come server COM in-process. L'API usa le API Microsoft Win32 standard per comunicare con il driver WPD appropriato. Un componente denominato serializzatore WPD viene usato sia dagli oggetti API che dal driver per il pacchetto o la decompressione dei parametri da o verso i buffer di Windows Driver Foundation (WDF) -User-Mode Driver Framework (UMDF).

## <a name="the-wpd-serializer"></a>Serializzatore WPD

Il serializzatore WPD viene implementato come server COM in-process. L'API WPD usa il serializzatore per creare pacchetti di comandi e parametri in buffer di messaggi inviati al driver. Il driver utilizza il serializzatore per decomprimere questi buffer dei messaggi per l'elaborazione. Il driver usa anche il serializzatore per il pacchetto di dati e parametri nei buffer di risposta restituiti all'API WPD e l'API WPD usa il serializzatore per decomprimere questi buffer di risposta da restituire ai chiamanti.

## <a name="wpd-driver"></a>WPD Driver

Il driver WPD viene implementato come driver Windows Driver Foundation (WDF)-User-Mode Driver Framework (UMDF) standard. I driver WPD sono ospitati da UMDF in un processo separato denominato Host driver.

Il driver riceve i messaggi dal riflettore UMDF(questo non è illustrato nel diagramma, perché la modalità di ricezione dei buffer non è importante per il driver. Per altre informazioni, vedere la documentazione di UMDF. Il driver implementa un gestore ioCL (I/O Control Code) specifico della WPD per elaborare i messaggi WPD ricevuti dall'API WPD. Il driver usa il serializzatore WPD per decomprimere i comandi e i parametri da questi buffer dei messaggi e per creare il pacchetto della risposta nel buffer restituito.

I driver WPD possono comunicare con i propri dispositivi passando attraverso un driver in modalità kernel, a cui si accede in genere tramite operazioni su file Win32,ovvero CreateFile, ReadFile, WriteFile e così via. Per i bus comuni, Microsoft fornirà driver kernel standard per i fornitori da usare, che consentiranno ai fornitori di spedire una soluzione di driver solo in modalità utente. Inoltre, per i dispositivi Media Transfer Protocol (MTP) e Mass Archiviazione Class (MSC), Microsoft fornirà driver di classe WPD.

Per altre informazioni sui driver WPD, vedere la Windows portable devices driver (Driver di dispositivi portatili) in Windows Driver Kit.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Panoramica dell'applicazione**](application-overview.md)
</dt> </dl>

 

 



