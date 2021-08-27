---
title: Esecuzione di query su dispositivi audio ausiliari
description: Esecuzione di query su dispositivi audio ausiliari
ms.assetid: 9fc0b17f-cc93-4eab-bcb3-09f2332b352f
keywords:
- audio waveform, esecuzione di query su dispositivi audio ausiliari
- audio ausiliario, esecuzione di query sui dispositivi
- interfaccia audio ausiliaria
- dispositivi audio ausiliari, esecuzione di query
- esecuzione di query su dispositivi audio ausiliari
- audio ausiliario, interfaccia
- audio ausiliario, dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49a6d61634475c3b921428529df69113c921b8c5bff8d1a65d5b08931a670fff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037571"
---
# <a name="querying-auxiliary-audio-devices"></a>Esecuzione di query su dispositivi audio ausiliari

Non tutti i sistemi multimediali dispongono del supporto audio ausiliario. È possibile usare [**la funzione auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs) per determinare il numero di dispositivi ausiliari controllabili presenti in un sistema.

Per ottenere informazioni su un particolare dispositivo audio ausiliario, usare la [**funzione auxGetDevCaps.**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps) Questa funzione riempie una [**struttura AUXCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-auxcaps) con informazioni sulle funzionalità di un dispositivo specificato. Queste informazioni includono gli identificatori del produttore e del prodotto, il nome del prodotto per il dispositivo e il numero di versione del driver di dispositivo.

 

 