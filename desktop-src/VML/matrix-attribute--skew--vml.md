---
title: Attributo Matrice (a inclinazione)(VML)
description: Attributo Matrice (a inclinazione)(VML)
ms.assetid: 8d039865-2261-458b-8edf-01374af65cea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d7fd3989807951f06df963c6899a2c81ce6e7faaa76432172e4391a4ce11029
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768450"
---
# <a name="matrix-attribute-skewvml"></a>Attributo Matrice (a inclinazione)(VML)

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce una trasformazione prospettica di un'a inclinazione. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Inclinazione](msdn-online-vml-skew-element.md)

**Sintassi dei tag**

<o: *element* matrix=" *expression* ">

**Sintassi dello script**

*element* .matrix="*expression*"

*expression* = *elemento*.matrix

**Osservazioni:**

La matrice è una stringa nel formato "sxx, sxy, syx, syy, px, py", dove s è scale, p è perspective e x e y sono valori x e y. Se [Offset](offset-attribute--skew--vml.md) è in unità assolute, px e py sono in unità emu^-1 [](msdn-online-vml-units.md) (in caso contrario sono una frazione inversa delle dimensioni della forma). Il valore predefinito è "1,0,0,1,0,0".

*Microsoft Office Attributo Extensions*

 

 