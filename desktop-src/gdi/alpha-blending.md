---
description: La fusione alfa viene utilizzata per visualizzare una bitmap Alpha, ovvero una bitmap con pixel trasparenti o semitrasparenti.
ms.assetid: 52a044cc-a471-4951-adbe-32319b8e3129
title: Fusione alfa (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f68cb34d189fb80d23cbb5eeec9d9006aa93a1eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978826"
---
# <a name="alpha-blending-windows-gdi"></a>Fusione alfa (Windows GDI)

La *fusione alfa* viene utilizzata per visualizzare una bitmap Alpha, ovvero una bitmap con pixel trasparenti o semitrasparenti. Oltre a un canale di colore rosso, verde e blu, ogni pixel in una bitmap alfa presenta un componente di trasparenza noto come *canale alfa*. Il canale alfa contiene in genere tutti i bit di un canale colori. Un canale alfa a 8 bit, ad esempio, può rappresentare 256 livelli di trasparenza, da 0 (l'intera bitmap è trasparente) a 255 (l'intera bitmap è opaca).

I meccanismi di fusione alfa vengono richiamati chiamando [**AlphaBlend**](/windows/desktop/api/WinGdi/nf-wingdi-alphablend), che fa riferimento alla struttura [**BlendFunction**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction) .

I valori alfa per pixel sono supportati solo per l'RGB BI 32-bpp \_ . Questa formula viene definita come segue:


```C++
typedef struct {
  BYTE   Blue;
  BYTE   Green;
  BYTE   Red;
  BYTE   Alpha;
};
```



Questa operazione viene rappresentata in memoria, come illustrato nella tabella seguente.



|       |       |       |       |
|-------|-------|-------|-------|
| 31:24 | 23:16 | 15:08 | 07:00 |
| Alfa | Red   | Green | Blu  |



 

Le bitmap possono essere visualizzate anche con un fattore di trasparenza applicato all'intera bitmap. Qualsiasi formato bitmap può essere visualizzato con un valore alfa costante globale impostando **SourceConstantAlpha** nella struttura [**BlendFunction**](/windows/desktop/api/Wingdi/ns-wingdi-blendfunction) . Il valore alfa costante globale presenta 256 livelli di trasparenza, da 0 (intera bitmap completamente trasparente) a 255 (l'intera bitmap è completamente opaca). Il valore alfa della costante globale è combinato con il valore alfa per pixel.

Per un esempio, vedere [fusione alfa di una bitmap](alpha-blending-a-bitmap.md).

 

 



