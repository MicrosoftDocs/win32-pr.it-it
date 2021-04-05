---
title: Esecuzione di query su dispositivi audio ausiliari
description: Esecuzione di query su dispositivi audio ausiliari
ms.assetid: 9fc0b17f-cc93-4eab-bcb3-09f2332b352f
keywords:
- audio Waveform, esecuzione di query sui dispositivi audio ausiliari
- audio ausiliario, esecuzione di query sui dispositivi
- interfaccia audio ausiliaria
- dispositivi audio ausiliari, esecuzione di query
- esecuzione di query su dispositivi audio ausiliari
- audio ausiliario, interfaccia
- audio ausiliario, dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d7de949c304cdd6941be87277f2eef1711ada24
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046625"
---
# <a name="querying-auxiliary-audio-devices"></a>Esecuzione di query su dispositivi audio ausiliari

Non tutti i sistemi multimediali hanno supporto audio ausiliario. È possibile utilizzare la funzione [**auxGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetnumdevs) per determinare il numero di dispositivi ausiliari controllabili presenti in un sistema.

Per ottenere informazioni su un particolare dispositivo audio ausiliario, usare la funzione [**auxGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-auxgetdevcaps) . Questa funzione riempie una struttura [**AUXCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-auxcaps) con informazioni sulle funzionalità di un dispositivo specificato. Queste informazioni includono gli identificatori del produttore e del prodotto, il nome del prodotto per il dispositivo e il numero di versione del driver del dispositivo.

 

 