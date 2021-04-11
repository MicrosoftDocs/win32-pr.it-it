---
description: Disponibilità di codec e supporto della piattaforma
ms.assetid: 6b3d09c9-e91f-4c62-92f7-c2643e51987f
title: Disponibilità di codec e supporto della piattaforma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc485c5f8db9ff7883263cd614578705eccd3fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232879"
---
# <a name="codec-availability-and-platform-support"></a>Disponibilità di codec e supporto della piattaforma

È consigliabile che i fornitori di fotocamere includano codec non ELABORAti di Windows Imaging Component (WIC) nella distribuzione del software con nuove fotocamere e che il codec aggiornato venga installato con l'installazione del software fornitore predefinita Windows 7, Windows Vista e Windows XP. I fornitori di fotocamere devono inoltre fornire il codec WIC più recente come download dai rispettivi siti di supporto tecnico.

## <a name="codec-discovery"></a>Individuazione codec

Microsoft sta effettuando le seguenti operazioni per consentire agli utenti di fare riferimento ai siti Web dei fornitori per i download di codec:

-   In Esplora risorse, se un utente fa doppio clic su un file non riconosciuto (il caso predefinito quando un file non elaborato si trova nel computer, ma il codec non è ancora installato), una finestra di dialogo indica che il file non è stato riconosciuto e chiede se l'utente vuole trovare un programma che riconosce il file. Microsoft gestisce un servizio di reindirizzamento esistente per l'invio di utenti ai siti Web dei fornitori in grado di fornire il programma per la comprensione del file. Questa funzionalità è disponibile in Windows XP e in Windows Vista.
-   La raccolta foto di Windows, la raccolta foto di Windows Live e il Visualizzatore foto di Windows 7 riconoscono un set di estensioni di file come file non ELABORAti. Se i file di tale set si trovano nelle cartelle esaminate da una di queste applicazioni e non è ancora installato un codec per il file, viene visualizzata una finestra di dialogo, come descritto nel paragrafo precedente.

Per ulteriori informazioni sull'individuazione dei codec, vedere disponibilità di codec e supporto della piattaforma.

## <a name="windows-xp-platform-support"></a>Supporto della piattaforma Windows XP

Microsoft ha rilasciato Windows XP SP3 con WIC e un programma di installazione WIC autonomo per Windows XP SP2. Questi utilizzano codec WIC per abilitare il supporto per anteprime e anteprime su tali piattaforme. È pertanto importante che il download e l'installazione di codec siano supportati e testati in Windows 7, Windows Vista e Windows XP.

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

 

 



