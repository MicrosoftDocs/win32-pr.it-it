---
title: Implementazione di altre funzioni
description: Implementazione di altre funzioni
ms.assetid: 274ba948-b954-4e9e-a384-dee5b3befbcb
keywords:
- Visualizzazioni, interfaccia IWMPEffects
- Visualizzazioni personalizzate, interfaccia IWMPEffects
- Visualizzazioni, funzione render
- Visualizzazioni personalizzate, funzione render
- Funzione render, funzioni aggiuntive
- Interfaccia IWMPEffects
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ed6efa5cc9a0697653e558f27165b66d5f230fd
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398596"
---
# <a name="implementing-other-functions"></a>Implementazione di altre funzioni

Sarà sicuramente opportuno scrivere un'implementazione personalizzata della funzione **Render** . Sono disponibili diverse altre funzioni che sono anche funzioni membro dell'interfaccia **IWMPEffects** . In alcuni casi verranno fornite informazioni aggiuntive che è possibile scegliere di usare e altre forniranno automaticamente Media Player di Windows con informazioni generate dalla procedura guidata, ad esempio il nome della visualizzazione.

L'interfaccia **IWMPEffects** supporta le funzioni seguenti oltre al **rendering**:



| Funzione                                                   | Descrizione                                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DisplayPropertyPage](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-displaypropertypage) | Implementazione predefinita non fornita dalla procedura guidata.                                                                                                                                                                                                                                                           |
| [GetCapabilities](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-getcapabilities)         | Ottiene le funzionalità della visualizzazione e le passa a Windows Media Player.                                                                                                                                                                                                                     |
| [GetCurrentPreset](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-getcurrentpreset)       | La procedura guidata ha creato due set di impostazioni quando ha generato il codice per la visualizzazione. Questa funzione viene chiamata quando lo sviluppatore di Skin desidera ottenere l'indice del set di impostazioni corrente. Non è necessario modificare l'implementazione di questa funzione perché usa solo le informazioni impostate da altre funzioni. |
| [GetPresetCount](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-getpresetcount)           | La procedura guidata ha creato due set di impostazioni quando ha generato il codice per la visualizzazione. È possibile modificare il conteggio modificando l'implementazione di **GetPresetCount**. Per ulteriori informazioni sulla modifica dei set di impostazioni, vedere [set di impostazioni](presets.md) .                                                             |
| [GetPresetTitle](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-getpresettitle)           | La procedura guidata ha creato due set di impostazioni quando ha generato il codice per la visualizzazione. È possibile modificare i titoli usati modificando l'implementazione di **GetPresetTitle**. Per ulteriori informazioni sulla modifica dei set di impostazioni, vedere [set di impostazioni](presets.md) .                                                       |
| [GetTitle](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-gettitle)                       | Ottiene il titolo della visualizzazione e lo passa a Windows Media Player. La procedura guidata ha usato il nome del progetto per generare il nome che viene passato di nuovo.                                                                                                                                           |
| [GoFullscreen](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-gofullscreen)               | Implementazione predefinita non fornita dalla procedura guidata.                                                                                                                                                                                                                                                           |
| [MediaInfo](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-mediainfo)                     | Recupera il numero di canali audio e la frequenza di campionamento dell'audio attualmente in riproduzione.                                                                                                                                                                                                               |
| [RenderFullScreen](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-renderfullscreen)       | Implementazione predefinita non fornita dalla procedura guidata.                                                                                                                                                                                                                                                           |
| [SetCurrentPreset](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-setcurrentpreset)       | La procedura guidata ha creato due set di impostazioni quando ha generato il codice per la visualizzazione. Questa funzione viene chiamata quando Windows Media Player desidera passare a un set di impostazioni denominato.                                                                                                                                   |



 

L'interfaccia **IWMPEffects2** supporta le funzioni aggiuntive seguenti:



| Funzione                                            | Descrizione                                                                                                                                      |
|-----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Creare](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-create)                   | Quando si esegue il rendering in una finestra, Windows Media Player chiama questa funzione per consentire la creazione di una nuova finestra per il rendering.                          |
| [Eliminare](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-destroy)                 | Quando si esegue il rendering in una finestra, Windows Media Player chiama questa funzione per consentire all'utente di eliminare definitivamente la finestra creata al momento della chiamata di **create** . |
| [NotifyNewMedia](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-notifynewmedia)   | Questa funzione consente alla visualizzazione di rispondere quando un nuovo elemento multimediale è stato caricato dal lettore.                                          |
| [OnWindowMessage](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-onwindowmessage) | Questa funzione riceve i messaggi di Windows dal lettore durante il rendering in modalità senza finestra.                                                       |
| [RenderWindowed](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-renderwindowed)   | Questa funzione viene chiamata dal lettore anziché da **IWMPEffects:: Render** quando il lettore esegue il rendering in modalità finestra.                          |
| [Secore](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-setcore)                 | Questa funzione riceve un puntatore all'interfaccia **IWMPCore** .                                                                                  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Implementazione del codice**](implementing-your-code.md)
</dt> </dl>

 

 




