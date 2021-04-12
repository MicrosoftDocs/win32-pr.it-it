---
title: Riferimento al plug-in
description: Funzioni di adapter, funzioni wrapper e strutture per la creazione di adattatori plug-in personalizzati di tre tipi di motore, sensore e archiviazione.
ms.assetid: 1886c389-b914-4b2d-ab7e-3e163782673d
keywords:
- API Windows Biometric Framework API di Windows Biometric Framework, informazioni di riferimento sul plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc764be98f6417d211effe1c182279d54c95d234
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471702"
---
# <a name="plug-in-reference"></a>Riferimento al plug-in

I dispositivi biometrici sono prodotti in un'ampia gamma di tipi e configurazioni. Nel Windows Biometric Framework è incorporata un'architettura estendibile che consente di gestire questa varietà creando plug-in personalizzati. Al centro di questa architettura è presente un oggetto software denominato unità biometrica. È possibile considerare un'unità biometrica come un'astrazione che rappresenta un dispositivo biometrico per il Framework. I componenti del software plug-in denominati adapter consentono di connettere l'unità biometrica all'hardware associato. Sono disponibili tre tipi di adapter che è possibile creare. Un adattatore del motore genera modelli biometrici dagli esempi acquisiti, associa gli esempi ai modelli esistenti e indicizza i modelli. Un adattatore del sensore esegue il wrapping di un dispositivo biometrico e fornisce un'interfaccia standard per la configurazione del sensore, l'acquisizione di esempi e il controllo del flusso di dati biometrici nel motore di elaborazione. Un adattatore di archiviazione gestisce i database modello.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                 | Descrizione                                                                                                                                                        |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Funzioni plug-in](plug-in-functions.md)<br/>                 | Funzioni che è possibile utilizzare per creare i plug-in di adapter che costituiscono un'unità biometrica.<br/>                                                                     |
| [Strutture di plug-in](plug-in-structures.md)<br/>               | Strutture per lo sviluppo di applicazioni client da parte dell'API Windows Biometric Framework.<br/>                                                                   |
| [Funzioni wrapper plug-in](plug-in-wrapper-functions.md)<br/> | Funzioni wrapper che consentono di chiamare una funzione pubblica su qualsiasi Adapter collegato alla pipeline senza acquisire manualmente un puntatore all'adapter.<br/> |



 

 

 





