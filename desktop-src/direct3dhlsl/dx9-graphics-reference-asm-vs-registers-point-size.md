---
title: Registro dimensioni punti
description: Questo registro di output del vertex shader contiene dati di dimensione del punto per vertice.
ms.assetid: 1aa6cd7d-9d29-4e7e-8448-8b9a6b251a02
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 36dbc6dc20d61baf4e0820dd0b6e10d3e6e918ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395803"
---
# <a name="point-size-register"></a>Registro dimensioni punti

Questo registro di output del vertex shader contiene dati di dimensione del punto per vertice.



| Versioni vertex shader | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|-------|------|------|-------|
| Registro dimensioni punti    | x    | x    | x     | x    | x    | x     |



 

Un registro è costituito da proprietà che determinano il comportamento di ogni registro.



| Proprietà        | Descrizione                                                                                     |
|-----------------|-------------------------------------------------------------------------------------------------|
| Nome            | oPts                                                                                            |
| Conteggio           | 1 vettore, di cui è possibile utilizzare solo un componente e che deve essere specificato dalla maschera dei componenti. |
| Autorizzazioni di I/O | Sola scrittura.                                                                                     |



 

Viene utilizzato solo il componente x scalare della dimensione del punto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri vertex shader](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




