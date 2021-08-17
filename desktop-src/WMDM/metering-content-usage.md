---
title: Misurazione dell'utilizzo del contenuto
description: Misurazione dell'utilizzo del contenuto
ms.assetid: f87b5d95-a497-4356-817f-49ac3819df08
keywords:
- Windows Gestione dispositivi multimediali, misurazione dell'utilizzo del contenuto
- Gestione dispositivi, misurazione dell'utilizzo del contenuto
- guida alla programmazione, misurazione dell'utilizzo del contenuto
- applicazioni desktop, misurazione dell'utilizzo del contenuto
- creazione Windows applicazioni di Gestione dispositivi multimediali, misurazione dell'utilizzo del contenuto
- misurazione dell'utilizzo del contenuto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029bae2bcdd69f9dc58c4a64317f974538c672b1d27597fbdc1915074aff0278
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957201"
---
# <a name="metering-content-usage"></a>Misurazione dell'utilizzo del contenuto

Con Windows tecnologia Media 10, è ora possibile controllare l'utilizzo del contenuto in un dispositivo portatile. Se una licenza Windows Media 10 consente la misurazione, il dispositivo può archiviare il numero di riproduci per i brani e caricare nuovamente l'utilizzo nell'emittente della licenza tramite Internet. Questo sistema consente ai provider di contenuti di modificare i costi di licenza misurando accuratamente l'utilizzo del contenuto.

Per controllare il contenuto, l'applicazione deve avere un certificato di controllo fornito da un servizio di gestione delle licenze basato su Windows Media Rights Manager 10 SDK. Solo il contenuto concesso in licenza dallo stesso servizio può essere misurato. Per altre informazioni sul funzionamento della misurazione e su come creare un servizio di controllo delle licenze, vedere la documentazione di [Windows Media Rights Manager SDK](/previous-versions/ms986509(v=msdn.10)) su MSDN. L'SDK può essere acquisito compilando le informazioni necessarie nella pagina [Windows media licensing.](https://www.microsoft.com/licensing/default)

A un'applicazione può essere incorporato il controllo oppure è possibile compilare un plug-in COM per un'applicazione esistente, ad esempio il Windows Media Player, se l'applicazione accetta plug-in di misurazione.

Un'applicazione deve avvisare gli utenti se l'utilizzo del contenuto verrà misurato. Per altre informazioni, vedere le pagine Web Microsoft elencate nell'Informativa [sulla privacy.](privacy-statement.md)

L'acquisizione dei dati di misurazione da un dispositivo può essere lenta. Pertanto, se un'applicazione misura l'utilizzo, è consigliabile farlo con una frequenza tale da impedire l'accumulo di grandi quantità di dati nel dispositivo e il rallentamento del trasferimento dei dati. Per evitare trasferimenti di dati troppo lenti, i produttori di dispositivi possono inviare subset di dati di misurazione disponibili. L'applicazione deve monitorare i flag recuperati da [**IWMDRMDeviceApp::P rocessMeterResponse**](iwmdrmdeviceapp-processmeterresponse.md) per verificare se nel dispositivo rimangono altri dati di misurazione.

La procedura seguente illustra come un'applicazione può controllare l'utilizzo del contenuto.

1.  Poiché la misurazione è disponibile solo nei dispositivi che supportano Windows Media DRM 10 per dispositivi portatili, a un certo punto l'applicazione deve chiamare **QueryDeviceStatus**, come descritto in [Gestione](handling-protected-content-in-the-application.md)del contenuto protetto nell'applicazione , per garantire che il dispositivo sia valido e aggiornato.
2.  Richiedere informazioni di misurazione dal dispositivo chiamando [**IWMDRMDeviceApp::GenerateMeterChallenge**](iwmdrmdeviceapp-generatemeterchallenge.md).
3.  Inviare i dati di misurazione recuperati al servizio di misurazione all'URL recuperato **da GenerateMeterChallenge.** Il formato dei dati inviati al servizio dipende dallo scripting su quel particolare servizio. Ad esempio, alcuni servizi potrebbero richiedere i dati inviati come comando POST come coppia nome/valore. Il provider di servizi deve inserirne i requisiti di formattazione specifici.
4.  Ottenere una risposta dal servizio di misurazione e inviarla al dispositivo chiamando [**IWMDRMDeviceApp::P rocessMeterResponse**](iwmdrmdeviceapp-processmeterresponse.md). In questo modo il dispositivo reimposta i conteggi di riproduzione e restituisce anche un valore che indica se nel dispositivo sono presenti più dati di misurazione che devono essere recuperati chiamando di nuovo **GenerateMeterChallenge.**

Per informazioni dettagliate e codice di esempio per la misurazione, [vedere il sito Web Windows Media](/previous-versions//bb614723(v=vs.85)).

 

 