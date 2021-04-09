---
title: Pulsanti (Windows Media Player SDK)
description: Pulsanti
ms.assetid: 1212e2d9-e8f8-45d8-8c7f-20865c9c9c94
keywords:
- Interfacce di Windows Media Player Mobile, panoramica sui pulsanti
- interfacce, panoramica sui pulsanti
- riferimento per le interfacce, i pulsanti
- pulsanti in Skin, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0f06eb2fe21ee18a24f92e92d4fa760e9c76887
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104118863"
---
# <a name="buttons-windows-media-player-sdk"></a>Pulsanti (Windows Media Player SDK)

È possibile usare uno o più pulsanti nell'interfaccia personalizzata e ogni pulsante deve essere definito nel file di definizione dell'interfaccia. Se non si definisce un pulsante in questa sezione, l'interfaccia non sarà in grado di utilizzarla.

La sezione Buttons del file di definizione Skin inizia con questa riga:


```C++
[ Buttons ]

```



È quindi necessario aggiungere una o più righe contenenti informazioni su ognuno dei pulsanti dell'interfaccia personalizzata. Una linea tipica potrebbe essere:


```C++
    PlayPause  2PushHit   84,99,67,67   Pushed @ 44,50    Disabled @ 44,50     0,255,255  Pushed @ 160,5      Pushed @ 160,98

```



Si noti che questo codice deve essere digitato come una riga che inizia con "come playpause" e termina con "pushed @ 160, 98".

È possibile usare il modello seguente per la sezione Button del file di definizione dell'interfaccia personalizzata:


```C++
//  <Function> <Type>     <Location>     <Push Image Src> <Dis Image Src>    <Hit R,G,B> <Norm 2 Image Src> <Push 2 Image Src>
//  ---------- ------     ----------     ---------------- ---------------    ----------- ------------------ ------------------

```



Si noti anche che questi devono essere tipizzati come righe singole, il primo a partire da "// <Function> " e termina con " &lt; push 2 Image src &gt; ". La seconda riga inizia con "//----------" e termina con "------------------."

Le informazioni sul pulsante per ogni riga della sezione Button devono essere visualizzate nell'ordine seguente. Sono necessarie solo le prime sei parti della riga. Le immagini secondarie non vengono incluse a meno che non siano necessarie.

1.  [Button (funzione)](button-function.md)
2.  [Tipo di pulsante](button-type.md)
3.  [Posizione del pulsante](button-location.md)
4.  [Origine immagine push](pushed-image-source.md)
5.  [Origine immagine per il pulsante disabilitato](image-source-for-disabled-button.md)
6.  [Colore RGB raggiunto](hit-rgb-color.md)
7.  [Origine normale dell'immagine secondaria](normal-secondary-image-source.md)
8.  [Origine normale dell'immagine terziaria](normal-tertiary-image-source.md)
9.  [Origine immagine secondaria push](pushed-secondary-image-source.md)
10. [Origine dell'immagine terziaria push](pushed-tertiary-image-source.md)

Per un esempio di codice pulsante, vedere la [sezione pulsante di esempio](sample-button-section.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Riferimento all'interfaccia**](skin-reference.md)
</dt> </dl>

 

 




