---
title: Video (Windows Media Player SDK)
description: Video
ms.assetid: 3c654494-19b5-401e-bed8-02f7cc7d7f4e
keywords:
- Windows Media Player Mobile Skins, video
- interfacce, video
- informazioni di riferimento per Skins, video
- video in Skin, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb3d505acec3f6917c7ed3d182c656ff5e9f29f0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300808"
---
# <a name="video-windows-media-player-sdk"></a>Video (Windows Media Player SDK)

Una visualizzazione video consente all'utente di visualizzare i file video digitali. L'area di visualizzazione video è visibile solo quando il video viene riprodotto o sospeso. Quando si progetta l'interfaccia, è consigliabile riservare spazio nell'immagine di sfondo per contenere la visualizzazione video. In caso contrario, la visualizzazione video potrebbe sovrapporsi a qualsiasi immagine visibile, ad esempio il file in background, i pulsanti e gli TrackBar, che impediscono all'utente di gestire i controlli sull'interfaccia.

La sezione video del file di definizione Skin deve iniziare con questa riga:


```C++
[ Video ]

```



È quindi necessario aggiungere una riga che specifica la posizione e le dimensioni dell'area di visualizzazione video nell'interfaccia.


```C++
0,38,240,172

```



È possibile usare il modello seguente per la sezione video del file di definizione dell'interfaccia personalizzata:


```C++
//  <Location>
//  ----------

```



Le sezioni seguenti forniscono ulteriori dettagli.

-   [Posizione video](video-location.md)
-   [Origine immagine video](video-image-source.md)
-   [Dimensioni del video](video-size.md)
-   [Sezione video di esempio](sample-video-section.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Riferimento all'interfaccia**](skin-reference.md)
</dt> </dl>

 

 




