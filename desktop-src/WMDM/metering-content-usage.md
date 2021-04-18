---
title: Misurazione dell'utilizzo del contenuto
description: Misurazione dell'utilizzo del contenuto
ms.assetid: f87b5d95-a497-4356-817f-49ac3819df08
keywords:
- Windows Media Gestione dispositivi, utilizzo del contenuto di misurazione
- Gestione dispositivi, utilizzo del contenuto di misurazione
- Guida per programmatori, utilizzo del contenuto di misurazione
- applicazioni desktop, utilizzo del contenuto di misurazione
- creazione di applicazioni Windows Media Gestione dispositivi, utilizzo del contenuto di misurazione
- misurazione dell'utilizzo del contenuto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 649eee810e7bbdbc2ea93a32c6368ec345fa7364
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "106300621"
---
# <a name="metering-content-usage"></a>Misurazione dell'utilizzo del contenuto

Con la tecnologia Windows Media 10, è ora possibile misurare l'utilizzo del contenuto su un dispositivo portatile. Se una licenza Windows Media 10 consente la misurazione, il dispositivo può archiviare il numero di giochi per i brani e caricare di nuovo l'uso nell'autorità emittente della licenza tramite Internet. Questo sistema consente ai provider di contenuti di modificare i canoni di royalty, misurando accuratamente l'utilizzo del contenuto.

Per misurare il contenuto, l'applicazione deve disporre di un certificato di misurazione fornito da un servizio di gestione delle licenze basato su Windows Media Rights Manager 10 SDK. È possibile misurare solo i contenuti concessi in licenza da questo stesso servizio. Per ulteriori informazioni sul funzionamento del controllo e su come creare un servizio di controllo delle licenze, vedere la [documentazione di Windows Media Rights Manager SDK](/previous-versions/ms986509(v=msdn.10)) su MSDN. L'SDK può essere acquisito compilando le informazioni necessarie nella [pagina Windows Media Licensing](https://www.microsoft.com/licensing/default).

Un'applicazione può disporre di un controllo incorporato oppure è possibile creare un plug-in COM per un'applicazione esistente, ad esempio Windows Media Player, se l'applicazione accetta plug-in di misurazione.

Un'applicazione deve avvertire gli utenti se l'utilizzo del contenuto verrà misurato. Per ulteriori informazioni, vedere le pagine Web Microsoft elencate nell' [informativa sulla privacy](privacy-statement.md).

L'acquisizione di dati di misurazione da un dispositivo può essere lenta. Di conseguenza, se l'uso di un contatore di applicazioni, questa operazione deve essere eseguita spesso per impedire l'accumulo di grandi quantità di dati nel dispositivo e il rallentamento del trasferimento dei dati. Per evitare trasferimenti di dati troppo lenti, i produttori di dispositivi possono inviare subset di dati di misurazione disponibili. L'applicazione deve monitorare i flag recuperati da [**IWMDRMDeviceApp::P rocessmeterresponse**](iwmdrmdeviceapp-processmeterresponse.md) per verificare se sono presenti altri dati di misurazione nel dispositivo.

Nei passaggi seguenti viene illustrato come un'applicazione può misurare l'utilizzo del contenuto.

1.  Poiché la misurazione è disponibile solo nei dispositivi che supportano Windows Media DRM 10 per i dispositivi portatili, l'applicazione dovrebbe a un certo punto chiamare **QueryDeviceStatus**, come descritto in [gestione del contenuto protetto nell'applicazione](handling-protected-content-in-the-application.md), per assicurarsi che il dispositivo sia valido e aggiornato.
2.  Richiedere informazioni di misurazione dal dispositivo chiamando [**IWMDRMDeviceApp:: GenerateMeterChallenge**](iwmdrmdeviceapp-generatemeterchallenge.md).
3.  Inviare i dati di controllo recuperati al servizio di misurazione nell'URL recuperato da **GenerateMeterChallenge**. Il formato dei dati inviati al servizio dipende dallo scripting in quel particolare servizio. Ad esempio, alcuni servizi potrebbero richiedere che i dati vengano inviati come un comando POST come una coppia nome/valore. Il provider di servizi deve consentire di conoscerne i requisiti di formattazione specifici.
4.  Ottenere una risposta dal servizio di misurazione e inviarla al dispositivo chiamando [**IWMDRMDeviceApp::P rocessmeterresponse**](iwmdrmdeviceapp-processmeterresponse.md). In questo modo, il dispositivo Reimposta i conteggi di riproduzione e restituisce anche un valore che indica se nel dispositivo sono presenti più dati di controllo che devono essere recuperati chiamando di nuovo **GenerateMeterChallenge** .

Per informazioni complete e codice di esempio per la misurazione, vedere il [sito Web Windows Media](/previous-versions//bb614723(v=vs.85)).

 

 