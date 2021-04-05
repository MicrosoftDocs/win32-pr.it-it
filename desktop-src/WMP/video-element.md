---
title: Elemento VIDEO
description: Elemento VIDEO
ms.assetid: 817e0d2e-cbc3-4b61-81c0-876104125f39
keywords:
- Windows Media Player Skin, elemento VIDEO
- Skin, elemento VIDEO
- Elemento VIDEO
- riferimento per Skin, elemento VIDEO
- elementi, VIDEO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbd8ab6bd014d2968483120fd1dd98804905faa4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711104"
---
# <a name="video-element"></a>Elemento VIDEO

L'elemento **video** fornisce un modo per modificare una finestra video in un'interfaccia, usando gli attributi e gli eventi seguenti. Viene inoltre fornito un elemento **video** predefinito per praticità.

L'elemento **video** supporta gli attributi seguenti.



| Attributo                                            | Descrizione                                                                                                                                                                                                                              |
|------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [backgroundColor](video-backgroundcolor.md)         | Specifica o Recupera il colore di sfondo del controllo video.                                                                                                                                                                        |
| [cursor](video-cursor.md)                           | Specifica o Recupera il valore del cursore utilizzato quando il mouse si trova su un'area selezionabile del video.                                                                                                                               |
| [Schermo intero](video-fullscreen.md)                   | Specifica o recupera un valore che indica se il video viene visualizzato in modalità schermo intero. Può essere impostato solo in fase di esecuzione.                                                                                                               |
| [maintainAspectRatio](video-maintainaspectratio.md) | Specifica o recupera un valore che indica se il video manterrà le proporzioni durante il tentativo di adattarsi alla larghezza e all'altezza definite per il controllo.                                                                       |
| [shrinkToFit](video-shrinktofit.md)                 | Specifica o recupera un valore che indica se il video ridurrà la larghezza e l'altezza definite per il controllo video.                                                                                                           |
| [stretchToFit](video-stretchtofit.md)               | Specifica o recupera un valore che indica se il video si estenderà per la larghezza e l'altezza definite per il controllo video.                                                                                                   |
| [Descrizione comando](video-tooltip.md)                         | Specifica o Recupera il testo della descrizione comando per la finestra del video.                                                                                                                                                                            |
| [senza finestra](video-windowless.md)                   | Specifica o recupera un valore che indica se il controllo video sarà finestra o senza finestra; ovvero se l'intero rettangolo del controllo sarà sempre visibile o possa essere ritagliato. Può essere impostato solo in fase di progettazione. |
| [zoom](video-zoom.md)                               | Specifica la percentuale in base alla quale ridimensionare il video.                                                                                                                                                                                    |



 

L'elemento **video** può implementare i gestori eventi seguenti.



| Gestore di evento                          | Descrizione                                                                  |
|----------------------------------------|------------------------------------------------------------------------------|
| [onvideoend](video-onvideoend.md)     | Gestisce un evento che si verifica quando il video interrompe il rendering e viene scaricato. |
| [onvideostart](video-onvideostart.md) | Gestisce un evento che si verifica quando il video viene caricato e inizia a eseguire il rendering.  |



 

L'elemento **video** supporta gli attributi di ambiente ed è in grado di implementare i gestori eventi di ambiente, tranne nei casi indicati. Per altre informazioni, vedere [attributi di ambiente](ambient-attributes.md) e [gestori di eventi di ambiente](ambient-event-handlers.md).

Gli elementi video predefiniti sono elementi **video** normali con diverse impostazioni degli attributi comuni specificati per impostazione predefinita. Sono disponibili gli elementi video predefiniti seguenti.



| VIDEO predefinito         | Descrizione                                                |
|--------------------------|------------------------------------------------------------|
| [WMPVIDEO](wmpvideo.md) | Elemento **video** che estende il video quando viene ridimensionato. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni di riferimento sulla programmazione dell'interfaccia**](skin-programming-reference.md)
</dt> </dl>

 

 




