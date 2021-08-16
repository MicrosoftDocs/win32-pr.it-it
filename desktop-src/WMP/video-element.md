---
title: Elemento VIDEO
description: Elemento VIDEO
ms.assetid: 817e0d2e-cbc3-4b61-81c0-876104125f39
keywords:
- Windows Media Player skin, elemento VIDEO
- skins,elemento VIDEO
- Elemento VIDEO
- informazioni di riferimento per le skin, elemento VIDEO
- elementi,VIDEO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7b72df7472829fe9979c9f7a30558e340a69aeb2f7024641623ba6be1a46424
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054199"
---
# <a name="video-element"></a>Elemento VIDEO

**L'elemento VIDEO** consente di modificare una finestra video in un'interfaccia, usando gli attributi e gli eventi seguenti. Per praticità viene fornito anche un elemento **VIDEO** predefinito.

**L'elemento VIDEO** supporta gli attributi seguenti.



| Attributo                                            | Descrizione                                                                                                                                                                                                                              |
|------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Backgroundcolor](video-backgroundcolor.md)         | Specifica o recupera il colore di sfondo del controllo Video.                                                                                                                                                                        |
| [cursor](video-cursor.md)                           | Specifica o recupera il valore del cursore utilizzato quando il mouse si trova su un'area selezionabile del video.                                                                                                                               |
| [Fullscreen](video-fullscreen.md)                   | Specifica o recupera un valore che indica se il video viene visualizzato in modalità schermo intero. Può essere impostato solo in fase di esecuzione.                                                                                                               |
| [maintainAspectRatio](video-maintainaspectratio.md) | Specifica o recupera un valore che indica se il video manterrà le proporzioni quando si tenta di rientrare nella larghezza e nell'altezza definite per il controllo.                                                                       |
| [shrinkToFit](video-shrinktofit.md)                 | Specifica o recupera un valore che indica se il video verrà compattato alla larghezza e all'altezza definite per il controllo Video.                                                                                                           |
| [stretchToFit](video-stretchtofit.md)               | Specifica o recupera un valore che indica se il video si estenderà fino alla larghezza e all'altezza definite per il controllo Video.                                                                                                   |
| [Descrizione comandi](video-tooltip.md)                         | Specifica o recupera il testo della descrizione comando per la finestra video.                                                                                                                                                                            |
| [senza finestra](video-windowless.md)                   | Specifica o recupera un valore che indica se il controllo Video sarà finestrato o senza finestra. che indica se l'intero rettangolo del controllo sarà sempre visibile o può essere ritagliato. Può essere impostato solo in fase di progettazione. |
| [Zoom](video-zoom.md)                               | Specifica la percentuale in base alla quale ridimensionare il video.                                                                                                                                                                                    |



 

**L'elemento VIDEO** può implementare i gestori eventi seguenti.



| Gestore di evento                          | Descrizione                                                                  |
|----------------------------------------|------------------------------------------------------------------------------|
| [onvideoend](video-onvideoend.md)     | Gestisce un evento che si verifica quando il video arresta il rendering e viene scaricato. |
| [onvideostart](video-onvideostart.md) | Gestisce un evento che si verifica quando il video viene caricato e inizia il rendering.  |



 

**L'elemento VIDEO** supporta gli attributi di ambiente e può implementare i gestori eventi di ambiente, tranne dove specificato. Per altre informazioni, vedere [Attributi di ambiente](ambient-attributes.md) e Gestori eventi di [ambiente](ambient-event-handlers.md).

Gli elementi video predefiniti sono elementi **VIDEO normali** con diverse impostazioni di attributo comuni specificate per impostazione predefinita. Sono disponibili gli elementi video predefiniti seguenti.



| VIDEO predefinito         | Descrizione                                                |
|--------------------------|------------------------------------------------------------|
| [WMPVIDEO](wmpvideo.md) | Elemento **VIDEO** che estende il video quando viene ridimensionato. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni di riferimento sulla programmazione dell'interfaccia**](skin-programming-reference.md)
</dt> </dl>

 

 




