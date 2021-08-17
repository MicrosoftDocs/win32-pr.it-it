---
title: Registro dimensioni punto
description: Questo registro di output vertex shader contiene dati relativi alle dimensioni del punto di vertice.
ms.assetid: 1aa6cd7d-9d29-4e7e-8448-8b9a6b251a02
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6de5c2fba55ce9cdfcee535ec001a89cbebcdddc5e3685224f9eb0c560870534
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119665"
---
# <a name="point-size-register"></a>Registro dimensioni punto

Questo registro di output vertex shader contiene dati relativi alle dimensioni del punto di vertice.



| Versioni di vertex shader | 1\_1 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|-------|------|------|-------|
| Registro dimensioni punto    | x    | x    | x     | x    | x    | x     |



 

Un registro è costituito da proprietà che determinano il comportamento di ogni registro.



| Proprietà        | Descrizione                                                                                     |
|-----------------|-------------------------------------------------------------------------------------------------|
| Nome            | Opta                                                                                            |
| Conteggio           | 1 vettore, di cui solo un componente può essere usato e deve essere specificato dalla maschera del componente. |
| Autorizzazioni di I/O | Sola scrittura.                                                                                     |



 

Viene usato solo il componente x scalare delle dimensioni in punti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri vertex shader](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




