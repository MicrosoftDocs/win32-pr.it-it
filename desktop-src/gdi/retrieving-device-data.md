---
description: 'Le applicazioni possono usare le funzioni seguenti per recuperare i dati del dispositivo usando un contesto di dispositivo: GetDeviceCaps e DeviceCapabilities.'
ms.assetid: eed6a323-b7eb-41a2-adb9-592f3f912884
title: Recupero dei dati del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adf956a04c733883cb5fb374e4e75dc4e93e8029f9968deb90cc113cef460864
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119717991"
---
# <a name="retrieving-device-data"></a>Recupero dei dati del dispositivo

Le applicazioni possono usare le funzioni seguenti per recuperare i dati del dispositivo usando un contesto di dispositivo: [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) e [**DeviceCapabilities**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa).

[**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) recupera i dati generali del dispositivo per i dispositivi seguenti:

-   Visualizzazione raster
-   Stampanti a matrice a punti
-   Stampanti ink-jet
-   Stampanti laser
-   Plotter vettoriali
-   Fotocamere raster

I dati includono le funzionalità supportate del dispositivo, tra cui risoluzione del dispositivo (per schermi video), formato a colori (per schermi video e stampanti a colori), numero di oggetti grafici, funzionalità raster, disegno di curve, disegno a linee, disegno poligono e disegno di testo. Un'applicazione recupera questi dati fornendo un handle che identifica il contesto di dispositivo appropriato, nonché un indice che specifica il tipo di dati che la funzione deve recuperare.

La funzione [**DeviceCapabilities**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa) recupera i dati specifici delle stampanti, tra cui il numero di contenitori di carta disponibili, le funzionalità duplex della stampante, le risoluzioni supportate dalla stampante, le dimensioni massime e minime supportate della carta e così via. Un'applicazione recupera questi dati fornendo stringhe che specificano un dispositivo e una porta della stampante, nonché un indice che specifica il tipo di dati che la funzione deve recuperare.

 

 
