---
title: Spazi colori Device-Dependent
description: La maggior parte degli spazi dei colori dipende dal dispositivo.
ms.assetid: 657ec64b-8605-4d05-a7d6-9f8bb71e6a71
keywords:
- Windows Color System (WCS), spazi dei colori dipendenti dal dispositivo
- WCS (Windows Color System), spazi dei colori dipendenti dal dispositivo
- Gestione colori immagine, spazi colore dipendenti dal dispositivo
- gestione dei colori, spazi dei colori dipendenti dal dispositivo
- colori, spazi dei colori dipendenti dal dispositivo
- spazi dei colori, dipendenti dal dispositivo
- spazi dei colori dipendenti dal dispositivo
- punto bianco
- coloranti
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22a1523ee6ba81dcdc3b69a468546871cfd21913
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/26/2021
ms.locfileid: "106320145"
---
# <a name="device-dependent-color-spaces"></a>Spazi colori Device-Dependent

La maggior parte degli [spazi dei colori](c.md) dipende dal dispositivo. Anche se un particolare dispositivo, ad esempio una stampante, può utilizzare lo spazio colore CMYK, i colori per i quali viene eseguito il rendering di valori CMYK specifici sono spesso leggermente diversi da tutti gli altri tipi di stampanti. È precisamente per questo motivo che il sistema di gestione dei colori WCS 1,0 è molto utile.

Tutti gli spazi dei colori hanno un *punto bianco*, definito come il bianco bianco che può essere prodotto in tale spazio colore. Poiché i dispositivi possono differire gli uni dagli altri, anche i punti vuoti possono variare. Tutti i colori che un dispositivo può produrre sono relativi al punto bianco. Pertanto, un sistema di gestione dei colori deve essere in grado di eseguire il mapping del punto bianco di uno spazio colore a un altro e di mantenere le posizioni relative di tutti i colori. Deve inoltre essere in grado di eseguire il mapping di un colore in uno spazio dei colori alla corrispondenza più vicina in un altro spazio di colore indipendentemente dalle differenze nei punti vuoti. WCS 1,0 è in grado di eseguire entrambe queste attività.

Lo spazio colore RGB viene spesso utilizzato nei monitoraggi computer. Di conseguenza, è dipendente dal dispositivo. Le stampanti usano in genere i [coloranti](c.md)CMYK. Ogni stampante implementa la propria versione dello spazio dei colori CMYK. Le immagini digitali potrebbero non archiviare effettivamente i colori. Potrebbero archiviare i numeri degli indici in una tavolozza di colori. Il risultato è che è molto difficile per gli sviluppatori di applicazioni singoli utilizzare o fornire un metodo standardizzato per lo sviluppo di immagini a colori da un dispositivo a un altro. I professionisti della creazione di immagini si riferiscono spesso alla frustrazione della creazione di un'immagine grafica sullo schermo di un computer e la loro disattivazione è molto diversa quando viene stampata WCS 1,0 risolve queste esigenze di imaging.

 

 




