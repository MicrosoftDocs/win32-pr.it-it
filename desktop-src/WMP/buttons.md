---
title: Pulsanti (Windows Media Player SDK)
description: Pulsanti
ms.assetid: 1212e2d9-e8f8-45d8-8c7f-20865c9c9c94
keywords:
- Windows Media Player Skin per dispositivi mobili, panoramica dei pulsanti
- skins,panoramica dei pulsanti
- informazioni di riferimento su skin, pulsanti
- pulsanti nelle skin, informazioni su
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96128c723c5b8bbac31c82a32060704bc892dfb7
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885539"
---
# <a name="buttons-windows-media-player-sdk"></a>Pulsanti (Windows Media Player SDK)

È necessario usare uno o più pulsanti nell'interfaccia e ogni pulsante deve essere definito nel file di definizione dell'interfaccia. Se non si definisce un pulsante in questa sezione, l'interfaccia non sarà in grado di usarlo.

La sezione buttons del file di definizione dell'interfaccia inizia con questa riga:


```C++
[ Buttons ]

```



È quindi necessario aggiungere una o più righe contenenti informazioni su ognuno dei pulsanti nell'interfaccia. Una linea tipica potrebbe essere:


```C++
    PlayPause  2PushHit   84,99,67,67   Pushed @ 44,50    Disabled @ 44,50     0,255,255  Pushed @ 160,5      Pushed @ 160,98

```



Si noti che questo codice deve essere digitato come una riga che inizia con "PlayPause" e termina con "Pushed @ 160,98".

È possibile usare il modello seguente per la sezione Button del file di definizione dell'interfaccia:


```C++
//  <Function> <Type>     <Location>     <Push Image Src> <Dis Image Src>    <Hit R,G,B> <Norm 2 Image Src> <Push 2 Image Src>
//  ---------- ------     ----------     ---------------- ---------------    ----------- ------------------ ------------------

```



Anche in questo caso, si noti che queste devono essere digitate come singole righe, la prima inizia con "// Function " e termina &lt; &gt; con " Push &lt; 2 Image Src &gt; ". La seconda riga inizia con "// ----------" e termina con "------------------."

Le informazioni sui pulsanti per ogni riga nella sezione Pulsante devono essere visualizzate nell'ordine seguente. Sono necessarie solo le prime sei parti della riga. Le immagini secondarie non sono incluse a meno che non siano necessarie.

1.  [Funzione Button](button-function.md)
2.  [Tipo di pulsante](button-type.md)
3.  [Posizione del pulsante](button-location.md)
4.  [Origine immagine di cui è stato push](pushed-image-source.md)
5.  [Origine immagine per il pulsante Disabilitato](image-source-for-disabled-button.md)
6.  [Colore RGB raggiunto](hit-rgb-color.md)
7.  [Origine immagine secondaria normale](normal-secondary-image-source.md)
8.  [Origine immagine terziaria normale](normal-tertiary-image-source.md)
9.  [Origine immagine secondaria di cui è stato push](pushed-secondary-image-source.md)
10. [Origine immagine terziaria con push](pushed-tertiary-image-source.md)

Per un esempio di codice pulsante, vedere [Sezione Pulsante di esempio](sample-button-section.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni di riferimento su Skin**](skin-reference.md)
</dt> </dl>

 

 




