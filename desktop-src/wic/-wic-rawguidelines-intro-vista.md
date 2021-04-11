---
description: Formati di immagini non ELABORAte in Windows Vista
ms.assetid: e28b642c-03c8-4ecc-b5f5-e3911b8003a7
title: Formati di immagini non ELABORAte in Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c48b4e3ab5b0d373dbc0313267e58177b189538
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232877"
---
# <a name="raw-image-formats-in-windows-vista"></a>Formati di immagini non ELABORAte in Windows Vista

Esplora risorse di Windows Vista, raccolta foto di Windows Vista, raccolta foto di Windows Live e Windows 7 Photo Viewer utilizzano Windows Imaging Component (WIC) e pertanto supportano i formati di immagine non ELABORAta quando nel computer sono installati codec appropriati.

Poiché WIC è un'architettura di imaging estensibile, qualsiasi applicazione WIC può utilizzare nuovi formati di immagine non appena vengono installati nuovi codec nel sistema. In questo modo WIC è ideale come soluzione Plug and Play per i formati di immagine non ELABORAti prodotti dalle fotocamere digitali. Tramite WIC, le applicazioni Windows possono ottenere supporto per i nuovi modelli di fotocamera ogni volta che vengono resi disponibili codec aggiornati, idealmente con nuove fotocamere. Gli autori di codec possono supportare questi scenari implementando interfacce WIC comuni a tutti i tipi di immagine, come descritto in dettaglio in questo documento.

Attualmente, la maggior parte delle applicazioni consumer mainstream non ha alcuna conoscenza speciale dei formati di immagine RAW e non espone un'interfaccia utente per la modifica delle impostazioni di elaborazione non ELABORAte.

Tuttavia, per supportare applicazioni di imaging specializzate, gli autori di codec RAW devono implementare anche l'interfaccia [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) . Questa interfaccia espone funzionalità speciali per le immagini non ELABORAte, ad esempio la possibilità di apportare modifiche di immagine comuni e di elaborare (sviluppare) immagini non ELABORAte in spazi dei colori di colore rosso-verde-blu (RGB) specificati.

Molte altre interfacce WIC sono importanti per l'implementazione da autori di codec non ELABORAti. Questi argomenti sono illustrati in modo più dettagliato in questa serie di argomenti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

**Informazioni concettuali**
</dt> <dt>

[Panoramica del componente imaging Windows](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Linee guida per WIC per i formati di immagine RAW della fotocamera](-wic-rawguidelines.md)
</dt> <dt>

[Come scrivere un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



