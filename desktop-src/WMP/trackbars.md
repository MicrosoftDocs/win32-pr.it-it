---
title: Trackbar
description: Trackbar
ms.assetid: b9676697-c3ab-465c-8b50-eb784f53bb11
keywords:
- Windows Media Player Skin per dispositivi mobili, trackbar
- skin, trackbar
- informazioni di riferimento su skin, trackbar
- trackbar negli skin, informazioni su
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eb311994ccdfb48eb1ea9e010b268cdef13fd1fc8a2154d491f6e4103a91ec3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119762671"
---
# <a name="trackbars"></a>Trackbar

Un trackbar visualizza un'immagine che cambia in piccoli incrementi. I trackbar vengono usati per i controlli del volume e per i controlli della posizione di riproduzione. È possibile usare i trackbar per visualizzare informazioni sull'elemento multimediale corrente o per consentire all'utente di modificare le impostazioni o la posizione di riproduzione. Ad esempio, è possibile usare un trackbar per consentire all'utente di regolare il volume e un altro trackbar che può mostrare all'utente la posizione di riproduzione corrente. I trackbar hanno un'immagine thumb che definisce l'impostazione corrente del valore del trackbar.

La sezione Trackbars del file di definizione dell'interfaccia deve iniziare con questa riga:


```C++
[ Trackbars ]

```



È quindi necessario aggiungere una o più righe contenenti informazioni su ogni trackbar nell'interfaccia.


```C++
    Seek        5,25,226,17    Disabled @ 4,1      SeekThumb.bmp      18,17
    Volume      32,220,172,23  Disabled @ 32,27    VolumeThumb.bmp    23,22

```



È possibile usare il modello seguente per la sezione Trackbars del file di definizione dell'interfaccia:


```C++
//  <Type> <Location>     <Dis Image Src> <Thumb Image Src> <Thumb Size>
//  ------ ----------     --------------- ----------------- ------------

```



È necessario usare l'ordine seguente per le informazioni del trackbar per ogni riga nella sezione Trackbars (ogni parte della riga è obbligatoria):

1.  [Tipo di trackbar](trackbar-type.md)
2.  [Posizione del trackbar](trackbar-location.md)
3.  [Origine immagine per trackbar disabilitato](image-source-for-disabled-trackbar.md)
4.  [Origine immagine thumb](thumb-image-source.md)
5.  [Dimensioni del cursore](thumb-size.md)

Per un esempio di codice Trackbars, vedere [Sezione Trackbars di esempio.](sample-trackbars-section.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni di riferimento su Skin**](skin-reference.md)
</dt> </dl>

 

 




