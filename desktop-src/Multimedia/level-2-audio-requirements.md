---
title: Requisiti audio di livello 2
description: Requisiti audio di livello 2
ms.assetid: 203648f2-9d20-438d-975b-b80e50b0fb9b
keywords:
- PC multimediali (MPC), livello 2
- MPC (PC multimediale), livello 2
- Consiglio marketing per PC multimediali, livello 2
- Livello 2 di MPC, requisiti audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e20458f8dcb26149c9fa697587faf93cf10c0f27
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709364"
---
# <a name="level-2-audio-requirements"></a>Requisiti audio di livello 2

Il sottosistema audio di un PC che soddisfa la specifica di livello 2 include gli elementi seguenti:

-   Un driver CD-ROM con output di CD-DA (Red Book Audio) e controllo del volume
-   Un'applicazione livello dati a 16 bit con le caratteristiche seguenti:
    -   Campionamento lineare PCM (Pulse Code Modulation)
    -   Funzionalità di trasferimento con memorizzazione nel buffer di DMA o FIFO con interrupt sul buffer vuoto
    -   Frequenza di campionamento obbligatorie di 44,1, 22,05 e 11,025 kHz
    -   Canali stereo
    -   Utilizzo della larghezza di banda della CPU pari al 10% o inferiore quando si esegue l'output dell'audio della frequenza di campionamento 22,05 o 11,025 kHz oppure una larghezza di banda della CPU del 15% o meno quando si esegue l'output della frequenza di campionamento 44,1 di

<!-- -->

-   ADC a 16 bit con le caratteristiche seguenti:
    -   Campionamento PCM lineare
    -   Funzionalità di trasferimento con memorizzazione nel buffer di DMA o FIFO con interrupt sul buffer vuoto
    -   Frequenza di campionamento obbligatorie di 44,1, 22,05 e 11,025 kHz
    -   Input microfono

<!-- -->

-   Funzionalità del sintetizzatore interno con multivoice, multitimbrico, sei note di melodia simultanee più due note di percussione simultanee
-   Combinazione interna con le funzionalità seguenti:
    -   Può combinare tre origini audio e presentare l'output come segnale audio stereo a livello di riga nel pannello indietro
    -   Le origini di mixaggio sono il CD rosso del libro, il sintetizzatore e l'applicazione livello dati
    -   Ogni origine di combinazione dispone di un controllo del volume a 3 bit con una conicità logaritmica

 

 




