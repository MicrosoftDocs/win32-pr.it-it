---
title: Attributo Matrix (Shadow)(VML)
description: Attributo Matrix (Shadow)(VML)
ms.assetid: 29bebd2f-7f66-4883-8c12-57fef4a0ac9e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6124005ef3202e11dc8a4e7eeeaacba8e87e9c3a7cb3a1dd1eee55c595e40ecb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057929"
---
# <a name="matrix-attribute-shadowvml"></a>Attributo Matrix (Shadow)(VML)

Questo argomento descrive VML, una funzionalità deprecata a Windows Internet Explorer 9. Le pagine Web e le applicazioni che si basano su VML devono essere migrate a SVG o ad altri standard ampiamente supportati.

> [!Note]  
> A partire da dicembre 2011, questo argomento è stato archiviato. Di conseguenza, non viene più gestito attivamente. Per altre informazioni, vedere [Contenuto archiviato.](/previous-versions/windows/internet-explorer/ie-developer/) Per informazioni, consigli e indicazioni sulla versione corrente di Windows Internet Explorer, vedere Internet Explorer [Developer Center.](https://msdn.microsoft.com/ie/)

 

Definisce una trasformazione prospettica per un'ombreggiatura. Proprietà di lettura/scrittura. **Stringa**.

**Si applica a**

[Shadow](msdn-online-vml-shadow-element.md)

**Sintassi dei tag**

<v: *element* matrix=" *expression* ">

**Sintassi dello script**

*element* .matrix="*expression*"

*expression* = *elemento*.matrix

**Osservazioni:**

Matrice di trasformazione prospettica nel formato "sxx,sxy,syx,syy,px,py", dove s= scale e p = perspective. Se offset è in unità assolute, px, py è in unità 1/emu; in caso contrario, sono una frazione inversa delle dimensioni della forma.

*Attributo VML Standard*

 

 