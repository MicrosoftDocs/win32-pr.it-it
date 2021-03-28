---
description: 'Le applicazioni possono usare le funzioni seguenti per recuperare i dati del dispositivo usando un contesto di dispositivo: GetDeviceCaps e DeviceCapabilities.'
ms.assetid: eed6a323-b7eb-41a2-adb9-592f3f912884
title: Recupero dei dati del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28fa4054170f9b66d73e3494928db312eb8aa9d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978306"
---
# <a name="retrieving-device-data"></a>Recupero dei dati del dispositivo

Le applicazioni possono usare le funzioni seguenti per recuperare i dati del dispositivo usando un contesto di dispositivo: [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) e [**DeviceCapabilities**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa).

[**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) recupera i dati generali del dispositivo per i dispositivi seguenti:

-   Visualizzazioni raster
-   Stampanti a matrice di punti
-   Stampanti Ink-Jet
-   Stampanti laser
-   Plotter vettoriali
-   Fotocamere raster

I dati includono le funzionalità supportate del dispositivo, inclusa la risoluzione del dispositivo (per le visualizzazioni video), il formato colori (per le visualizzazioni video e le stampanti colori), il numero di oggetti grafici, le funzionalità raster, il disegno a curva, il disegno a linee, il disegno del poligono e il disegno del testo. Un'applicazione recupera questi dati fornendo un handle che identifica il contesto di dispositivo appropriato, oltre a un indice che specifica il tipo di dati che la funzione deve recuperare.

La funzione [**DeviceCapabilities**](/windows/win32/api/wingdi/nf-wingdi-devicecapabilitiesa) recupera i dati specifici delle stampanti, incluso il numero di contenitori di carta disponibili, le funzionalità duplex della stampante, le risoluzioni supportate dalla stampante, le dimensioni massime e minime supportate della carta e così via. Un'applicazione recupera questi dati fornendo stringhe che specificano un dispositivo e una porta della stampante, oltre a un indice che specifica il tipo di dati che la funzione deve recuperare.

 

 
