---
title: Plug-in di Windows Media Player
description: Plug-in di Windows Media Player
ms.assetid: 6265084b-e1ff-455b-aca8-dc008d94ed43
keywords:
- Windows Media Player, plug-in
- Plug-in di Windows Media Player, informazioni
- plug-in, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7d666874590f380e6f3828031b297d483ffff7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300193"
---
# <a name="windows-media-player-plug-ins"></a>Plug-in di Windows Media Player

Microsoft Windows Media Player espone interfacce che consentono di estendere le funzionalità in diversi modi. Le sezioni seguenti descrivono le architetture di plug-in supportate e il processo di creazione di un plug-in:



| Sezione                                                                                                         | Descrizione                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Creazione di un plug-in](building-a-plug-in.md)                                                                    | È possibile creare diversi tipi di plug-in usando Visual Studio e la creazione guidata plug-in di Windows Media Player.                                                                                                                                                                                             |
| [Visualizzazioni personalizzate di Windows Media Player](windows-media-player-custom-visualizations.md)                    | Le visualizzazioni di Windows Media Player sono oggetti Component Object Model (COM) usati per visualizzare immagini visive sincronizzate con la parte audio della riproduzione multimediale del lettore. È possibile creare visualizzazioni personalizzate usando Microsoft Visual C++.                                             |
| [Plug-in di interfaccia utente di Windows Media Player](windows-media-player-user-interface-plug-ins.md)                | I plug-in di interfaccia utente di Windows Media Player aggiungono nuove funzionalità al riquadro **Now Playing** del lettore in modalità completa. È possibile creare plug-in che usano l'area di visualizzazione, una finestra separata, l'area delle impostazioni, l'area dei metadati o plug-in in background che non espongono alcuna interfaccia utente visibile. |
| [Plug-in di Windows Media Player DSP](windows-media-player-dsp-plug-ins.md)                                      | I plug-in di Windows Media Player DSP modificano o elaborano i dati audio e video prima del rendering da parte del lettore. I plug-in DSP sono gli oggetti DMO (DirectX Media Objects) che si connettono al lettore tramite interfacce COM.                                                                                           |
| [Plug-in per il rendering di Windows Media Player (deprecato)](/previous-versions/windows/desktop/legacy/dd564683(v=vs.85)) | I plug-in per il rendering di Windows Media Player decodificano (se necessario) ed eseguono il rendering di dati personalizzati contenuti in un flusso di formato Windows Media. I plug-in per il rendering sono gli oggetti DMO (DirectX Media Objects) che si connettono al lettore tramite interfacce COM.                                                                  |
| [Plug-in di conversione di Windows Media Player](windows-media-player-conversion-plug-ins.md)                        | I plug-in di conversione di Windows Media Player convertono i file multimediali digitali creati usando le tecnologie non fornite da Microsoft, in formato ASF (Advanced Systems Format).                                                                                                                                 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Windows Media Player SDK**](windows-media-player-sdk.md)
</dt> </dl>

 

 