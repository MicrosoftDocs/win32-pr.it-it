---
title: TrackBar
description: TrackBar
ms.assetid: b9676697-c3ab-465c-8b50-eb784f53bb11
keywords:
- Windows Media Player Mobile Skins, trackbars
- interfacce, TrackBar
- riferimento per Skin, trackbars
- trackbars in Skin, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb7b64f7bada6f927b25aeecb71d584aa1ec2a68
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298649"
---
# <a name="trackbars"></a>TrackBar

Un TrackBar Visualizza un'immagine che cambia in piccoli incrementi. Gli TrackBar vengono utilizzati per i controlli volume e la posizione di riproduzione. È possibile utilizzare gli oggetti TrackBar per visualizzare informazioni sull'elemento multimediale corrente o per consentire all'utente di modificare le impostazioni o la posizione di riproduzione. Ad esempio, è possibile utilizzare un TrackBar per consentire all'utente di modificare il volume e un altro TrackBar in grado di mostrare all'utente la posizione di riproduzione corrente. Gli TrackBar hanno un'immagine Thumb che definisce l'impostazione corrente del valore TrackBar.

La sezione trackbars del file di definizione Skin deve iniziare con questa riga:


```C++
[ Trackbars ]

```



È quindi necessario aggiungere una o più righe che contengono informazioni su ogni TrackBar nell'interfaccia.


```C++
    Seek        5,25,226,17    Disabled @ 4,1      SeekThumb.bmp      18,17
    Volume      32,220,172,23  Disabled @ 32,27    VolumeThumb.bmp    23,22

```



È possibile usare il modello seguente per la sezione trackbars del file di definizione dell'interfaccia utente:


```C++
//  <Type> <Location>     <Dis Image Src> <Thumb Image Src> <Thumb Size>
//  ------ ----------     --------------- ----------------- ------------

```



È necessario utilizzare l'ordine seguente per le informazioni di TrackBar per ogni riga nella sezione trackbars (ogni parte della riga è obbligatoria):

1.  [Tipo TrackBar](trackbar-type.md)
2.  [Posizione TrackBar](trackbar-location.md)
3.  [Origine immagine per TrackBar disabilitato](image-source-for-disabled-trackbar.md)
4.  [Origine immagine Thumb](thumb-image-source.md)
5.  [Dimensioni Thumb](thumb-size.md)

Per un esempio di codice trackbars, vedere la [sezione Sample trackbars](sample-trackbars-section.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Riferimento all'interfaccia**](skin-reference.md)
</dt> </dl>

 

 




