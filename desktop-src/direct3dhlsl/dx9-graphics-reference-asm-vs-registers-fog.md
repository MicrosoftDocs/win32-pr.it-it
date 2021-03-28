---
title: Registro di nebbia
description: Questo registro di output del vertex shader contiene un colore per la nebbia per vertice.
ms.assetid: b2b06aa9-ad75-48df-857d-fd8719176713
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3c3f0e39c0670176b6233f61f0ba50596c92ca4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104976103"
---
# <a name="fog-register"></a>Registro di nebbia

Questo registro di output del vertex shader contiene un colore per la nebbia per vertice.

Un registro è costituito da proprietà che determinano il comportamento di ogni registro.



| Proprietà        | Descrizione                                                                                     |
|-----------------|-------------------------------------------------------------------------------------------------|
| Nome            | oFog                                                                                            |
| Conteggio           | Un vettore, di cui è possibile usare un solo componente e che deve essere specificato dalla maschera dei componenti |
| Autorizzazioni di I/O | Sola scrittura.                                                                                     |



 

Il valore di nebbia di output viene registrato. Il valore è il fattore di nebbia da interpolare e quindi indirizzato alla tabella Fog. Viene utilizzato solo il componente x scalare della nebbia.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri vertex shader](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




