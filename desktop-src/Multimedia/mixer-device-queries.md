---
title: Query del dispositivo mixer
description: Query del dispositivo mixer
ms.assetid: 3b453802-954b-4356-9ad5-0f8376b6199d
keywords:
- audio multimediale, query del dispositivo mixer
- audio, query del dispositivo mixer
- mixer audio, query sul dispositivo
- mixer, query del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02acc3d5c7e418d14412c60a2e28e32849497c1a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046683"
---
# <a name="mixer-device-queries"></a>Query del dispositivo mixer

I servizi mixer forniscono funzioni per determinare il numero di dispositivi mixer presenti nel sistema e le funzionalità dei dispositivi. È anche possibile usare una funzione di servizi mixer per determinare l'identificatore del dispositivo per un dispositivo mixer.

È possibile usare la funzione [**mixerGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs) per determinare il numero di dispositivi mixer presenti nel sistema. I dispositivi mixer sono identificati da un identificatore di dispositivo. Gli identificatori di dispositivo sono determinati in modo implicito dal numero di dispositivi presenti in un determinato sistema. Sono compresi tra zero e uno inferiore al numero di dispositivi presenti.

Prima di usare un dispositivo mixer, è necessario determinarne le funzionalità. Le funzionalità audio possono variare da un computer multimediale a un altro, quindi le applicazioni devono usare un'ampia gamma di hardware audio.

È possibile usare la funzione [**mixerGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetdevcaps) per determinare le funzionalità dei dispositivi mixer. Questa funzione riempie una struttura [**MIXERCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercaps) con informazioni sulle funzionalità di un dispositivo specificato.

La funzione [**mixerGetID**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetid) recupera l'identificatore del dispositivo mixer audio associato a un handle di dispositivo specificato. Ad esempio, è possibile usare questa funzione per recuperare l'identificatore del dispositivo per un mixer audio e quindi usare l'identificatore del dispositivo per regolare il volume o per visualizzare un altro controllo.

 

 