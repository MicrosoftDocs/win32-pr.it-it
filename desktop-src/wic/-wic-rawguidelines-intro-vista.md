---
description: Formati di immagine RAW in Windows Vista
ms.assetid: e28b642c-03c8-4ecc-b5f5-e3911b8003a7
title: Formati di immagine RAW in Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88026e85780706ca2bd5f23f5ca43ec49ae614d4c65e42ec19367b01b3f43423
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118709859"
---
# <a name="raw-image-formats-in-windows-vista"></a>Formati di immagine RAW in Windows Vista

Windows Vista Explorer, Windows Vista Raccolta foto, Window Live Raccolta foto e Windows 7 Visualizzatore foto usano tutti Windows Imaging Component (WIC) e pertanto supportano i formati di immagine RAW quando nel computer sono installati codec appropriati.

Poiché WIC è un'architettura di creazione di immagini estendibile, qualsiasi applicazione WIC può utilizzare nuovi formati di immagine non appena vengono installati nuovi codec nel sistema. WiC è quindi ideale come soluzione Plug and Play per i formati di immagine RAW prodotti dalle fotocamere digitali. Tramite WIC, Windows applicazioni possono ottenere il supporto per i nuovi modelli di fotocamera ogni volta che vengono resi disponibili codec aggiornati (idealmente in box con nuove fotocamere). Gli autori di codec possono supportare questi scenari implementando interfacce WIC comuni a tutti i tipi di immagine, come descritto più dettagliatamente in questo documento.

Attualmente, la maggior parte delle applicazioni consumer mainstream non ha una conoscenza speciale dei formati di immagine RAW e non espone un'interfaccia utente per modificare le impostazioni di elaborazione RAW.

Tuttavia, per supportare applicazioni di creazione di immagini specializzate, gli autori di codec RAW devono implementare anche [**l'interfaccia IWICDevelopRaw.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) Questa interfaccia espone funzionalità speciali per le immagini RAW, ad esempio la possibilità di apportare modifiche comuni alle immagini ed elaborare (sviluppare) immagini RAW in spazi colori RGB (Red-Green-Blue) specificati.

Diverse altre interfacce WIC sono importanti per l'implementazione da parte degli autori di codec RAW. Questi argomenti vengono illustrati in modo più dettagliato in questa serie di argomenti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Windows Panoramica del componente di creazione dell'immagine](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Linee guida WIC per i formati di immagine RAW della fotocamera](-wic-rawguidelines.md)
</dt> <dt>

[Come scrivere un codec WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



