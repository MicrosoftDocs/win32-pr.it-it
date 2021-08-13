---
title: Informazioni di riferimento sul plug-in
description: Funzioni dell'adapter, funzioni wrapper e strutture per la creazione di adattatori plug-in personalizzati di tre tipi di motore, sensore e archiviazione.
ms.assetid: 1886c389-b914-4b2d-ab7e-3e163782673d
keywords:
- Windows Informazioni di riferimento sul plug-in dell'API Biometric Framework Windows'API Biometric Framework
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2223f398579663d94c0cc40daef1fcf37e4239d8d0dc8246fedd15b454b3354
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119410961"
---
# <a name="plug-in-reference"></a>Informazioni di riferimento sul plug-in

I dispositivi biometrici vengono prodotti in un'ampia gamma di tipi e configurazioni. Il Windows Biometric Framework incorpora un'architettura estendibile che consente di gestire questa varietà creando plug-in personalizzati. Al centro di questa architettura è presente un oggetto software denominato unità biometrica. Un'unità biometrica può essere pensata come un'astrazione che rappresenta un dispositivo biometrico per framework. I componenti software plug-in denominati adattatori connettono l'unità biometrica all'hardware associato. È possibile creare tre tipi di adattatori. Un adattatore del motore genera modelli biometrici dagli esempi acquisiti, corrisponde agli esempi ai modelli esistenti e indicizza i modelli. Un adattatore sensore esegue il wrapping di un dispositivo biometrico e fornisce un'interfaccia standard per la configurazione del sensore, l'acquisizione di campioni e il controllo del flusso dei dati biometrici al motore di elaborazione. Un adattatore di archiviazione gestisce i database modello.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                 | Descrizione                                                                                                                                                        |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Funzioni plug-in](plug-in-functions.md)<br/>                 | Funzioni che è possibile usare per creare i plug-in dell'adapter che costituiscono un'unità biometrica.<br/>                                                                     |
| [Strutture dei plug-in](plug-in-structures.md)<br/>               | Strutture per lo sviluppo di applicazioni client da parte dell Windows API Biometric Framework.<br/>                                                                   |
| [Funzioni wrapper plug-in](plug-in-wrapper-functions.md)<br/> | Funzioni wrapper che consentono di chiamare una funzione pubblica su qualsiasi adattatore collegato alla pipeline senza acquisire manualmente un puntatore all'adapter.<br/> |



 

 

 





