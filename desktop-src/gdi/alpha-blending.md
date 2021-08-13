---
description: La fusione alfa viene usata per visualizzare una bitmap alfa, ovvero una bitmap con pixel trasparenti o semitrasparenti.
ms.assetid: 52a044cc-a471-4951-adbe-32319b8e3129
title: Alpha Blending (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eb59f6b628236124305e4564803fa826c279bfdc2353725a62029b293cb1e90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119470131"
---
# <a name="alpha-blending-windows-gdi"></a>Alpha Blending (Windows GDI)

*La fusione alfa* viene usata per visualizzare una bitmap alfa, ovvero una bitmap con pixel trasparenti o semitrasparenti. Oltre a un canale di colori rosso, verde e blu, ogni pixel in una bitmap alfa ha un componente di trasparenza noto come *canale alfa.* Il canale alfa contiene in genere tutti i bit di un canale di colore. Ad esempio, un canale alfa a 8 bit può rappresentare 256 livelli di trasparenza, da 0 (l'intera bitmap è trasparente) a 255 (l'intera bitmap è opaca).

I meccanismi di fusione alfa vengono richiamati chiamando [**AlphaBlend**](/windows/desktop/api/WinGdi/nf-wingdi-alphablend), che fa riferimento alla [**struttura BLENDFUNCTION.**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction)

I valori alfa per pixel sono supportati solo per RGB BI a 32 \_ bpp. Questa formula è definita come:


```C++
typedef struct {
  BYTE   Blue;
  BYTE   Green;
  BYTE   Red;
  BYTE   Alpha;
};
```



È rappresentato in memoria come illustrato nella tabella seguente.

:::row:::
    :::column:::
        31:24
    :::column-end:::
    :::column:::
        23:16
    :::column-end:::
    :::column:::
        15:08
    :::column-end:::
    :::column:::
        07:00
    :::column-end:::
:::row-end:::

:::row:::
    :::column:::
        Alfa
    :::column-end:::
    :::column:::
        Red
    :::column-end:::
    :::column:::
        Green
    :::column-end:::
    :::column:::
        Blu
    :::column-end:::
:::row-end:::

Le bitmap possono anche essere visualizzate con un fattore di trasparenza applicato all'intera bitmap. Qualsiasi formato bitmap può essere visualizzato con un valore alfa costante globale impostando **SourceConstantAlpha** nella [**struttura BLENDFUNCTION.**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction) Il valore alfa costante globale ha 256 livelli di trasparenza, da 0 (l'intera bitmap è completamente trasparente) a 255 (l'intera bitmap è completamente opaca). Il valore alfa costante globale viene combinato con il valore alfa per pixel.

Per un esempio, vedere [Alpha Blending a Bitmap (Fusione alfa di una bitmap).](alpha-blending-a-bitmap.md)

 

 



