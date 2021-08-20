---
title: Requisiti audio di livello 2
description: Requisiti audio di livello 2
ms.assetid: 203648f2-9d20-438d-975b-b80e50b0fb9b
keywords:
- PC multimediale (MPC), livello 2
- MPC (Multimedia PC),Livello 2
- Multimedia PC Marketing Council,Level 2
- MPC Livello 2, requisiti audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a2bc9398a25ac916352f41ad2ddc2325820354d1c7beb511b03b27004fadd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118139832"
---
# <a name="level-2-audio-requirements"></a>Requisiti audio di livello 2

Il sottosistema audio di un PC che soddisfa la specifica di livello 2 include gli elementi seguenti:

-   Driver CD-ROM con output CD-DA (audio Red Book) e controllo del volume
-   Applicazione livello dati a 16 bit con le caratteristiche seguenti:
    -   Campionamento PCM lineare (pulse code modulation)
    -   Funzionalità di trasferimento con buffer DMA o FIFO con interrupt nel buffer vuoto
    -   Frequenze di campionamento obbligatorie di 44,1, 22,05 e 11,025 kHz
    -   Canali stereo
    -   Utilizzo della larghezza di banda della CPU del 10% o inferiore durante l'output audio di una frequenza di campionamento di 22,05 o 11,025 kHz o una larghezza di banda della CPU del 15% o inferiore durante l'output audio di una frequenza di campionamento di 44,1 kHz

<!-- -->

-   ADC a 16 bit con le caratteristiche seguenti:
    -   Campionamento PCM lineare
    -   Funzionalità di trasferimento con buffer DMA o FIFO con interrupt nel buffer vuoto
    -   Frequenze di campionamento obbligatorie di 44,1, 22,05 e 11,025 kHz
    -   Input del microfono

<!-- -->

-   Funzionalità di sintetizzatore interno con multivoice, multitimbral, sei note simultanee più due note percussive simultanee
-   Combinazione interna con le funzionalità seguenti:
    -   Può combinare tre origini audio e presentare l'output come segnale audio stereo a livello di linea nel pannello indietro
    -   Le origini di combinazione sono audio CD Red Book, sintetizzatore e applicazione livello dati
    -   Ogni origine di combinazione ha un controllo del volume a 3 bit con un taper logaritmico

 

 




