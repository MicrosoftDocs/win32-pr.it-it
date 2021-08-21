---
title: Implementazione di altre funzioni
description: Implementazione di altre funzioni
ms.assetid: 274ba948-b954-4e9e-a384-dee5b3befbcb
keywords:
- visualizzazioni, interfaccia IWMPEffects
- visualizzazioni personalizzate, interfaccia IWMPEffects
- visualizzazioni, funzione Render
- visualizzazioni personalizzate, funzione Render
- Funzione di rendering, funzioni aggiuntive
- Interfaccia IWMPEffects
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73392204357ec856c5c04f2a0f24028ea29e5f09c3aa203d95ed8e2cc7e4ded3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119508931"
---
# <a name="implementing-other-functions"></a>Implementazione di altre funzioni

Sarà sicuramente necessario scrivere un'implementazione personalizzata della **funzione Render.** Sono disponibili diverse altre funzioni che sono anche funzioni membro **dell'interfaccia IWMPEffects.** Alcune forniscono informazioni aggiuntive che è possibile scegliere di usare e altre forniscono automaticamente Windows Media Player con le informazioni generate dalla procedura guidata, ad esempio il nome della visualizzazione.

Oltre a Render, l'interfaccia **IWMPEffects** supporta le funzioni **seguenti:**



| Funzione                                                   | Descrizione                                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [DisplayPropertyPage](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-displaypropertypage) | Implementazione predefinita non fornita dalla procedura guidata.                                                                                                                                                                                                                                                           |
| [GetCapabilities](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-getcapabilities)         | Ottiene le funzionalità della visualizzazione e le passa Windows Media Player.                                                                                                                                                                                                                     |
| [GetCurrentPreset](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-getcurrentpreset)       | La procedura guidata ha creato due set di impostazioni quando ha generato il codice per la visualizzazione. Questa funzione viene chiamata quando lo sviluppatore dell'interfaccia vuole ottenere l'indice del set di impostazioni corrente. Non è necessario modificare l'implementazione di questa funzione perché usa solo le informazioni impostate da altre funzioni. |
| [GetPresetCount](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-getpresetcount)           | La procedura guidata ha creato due set di impostazioni quando ha generato il codice per la visualizzazione. È possibile modificare il conteggio modificando l'implementazione di **GetPresetCount.** Per [altre informazioni sulla](presets.md) modifica dei set di impostazioni, vedere Set di impostazioni.                                                             |
| [GetPresetTitle](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-getpresettitle)           | La procedura guidata ha creato due set di impostazioni quando ha generato il codice per la visualizzazione. È possibile modificare i titoli usati modificando l'implementazione di **GetPresetTitle.** Per [altre informazioni sulla](presets.md) modifica dei set di impostazioni, vedere Set di impostazioni.                                                       |
| [GetTitle](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-gettitle)                       | Ottiene il titolo della visualizzazione e lo passa Windows Media Player. La procedura guidata ha usato il nome del progetto per generare il nome passato.                                                                                                                                           |
| [GoFullscreen](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-gofullscreen)               | Implementazione predefinita non fornita dalla procedura guidata.                                                                                                                                                                                                                                                           |
| [Mediainfo](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-mediainfo)                     | Recupera il numero di canali audio e la frequenza di campionamento dell'audio attualmente in riproduzione.                                                                                                                                                                                                               |
| [RenderFullScreen](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-renderfullscreen)       | Implementazione predefinita non fornita dalla procedura guidata.                                                                                                                                                                                                                                                           |
| [SetCurrentPreset](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects-setcurrentpreset)       | La procedura guidata ha creato due set di impostazioni quando ha generato il codice per la visualizzazione. Questa funzione viene chiamata quando Windows Media Player vuole passare a un set di impostazioni denominato.                                                                                                                                   |



 

**L'interfaccia IWMPEffects2** supporta le funzioni aggiuntive seguenti:



| Funzione                                            | Descrizione                                                                                                                                      |
|-----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [Creare](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-create)                   | Quando si esegue il rendering in una finestra, Windows Media Player chiama questa funzione per consentire di creare una nuova finestra per il rendering.                          |
| [Distruggere](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-destroy)                 | Quando si esegue il rendering in una finestra, Windows Media Player chiama questa funzione per consentire di eliminare la finestra creata quando **è stato chiamato Create.** |
| [NotifyNewMedia](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-notifynewmedia)   | Questa funzione consente alla visualizzazione di rispondere quando un nuovo elemento multimediale è stato caricato dal lettore.                                          |
| [OnWindowMessage](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-onwindowmessage) | Questa funzione riceve i messaggi di Windows dal lettore durante il rendering in modalità senza finestra.                                                       |
| [RenderWindowed](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-renderwindowed)   | Questa funzione viene chiamata dal lettore anziché **da IWMPEffects::Render** quando il lettore esegue il rendering in modalità finestra.                          |
| [SetCore](/previous-versions/windows/desktop/api/effects/nf-effects-iwmpeffects2-setcore)                 | Questa funzione riceve un puntatore **all'interfaccia IWMPCore.**                                                                                  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Implementazione del codice**](implementing-your-code.md)
</dt> </dl>

 

 




