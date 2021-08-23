---
title: Register Disas
description: Questo registro di output del vertex shader contiene un colore per vertice.
ms.assetid: b2b06aa9-ad75-48df-857d-fd8719176713
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b6aeaea0e51960f8f4bf768b855ac31236b2bb330cfda3390fd9e61dab4ec1f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854581"
---
# <a name="fog-register"></a>Register Disas

Questo registro di output del vertex shader contiene un colore per vertice.

Un registro è costituito da proprietà che determinano il comportamento di ogni registro.



| Proprietà        | Descrizione                                                                                     |
|-----------------|-------------------------------------------------------------------------------------------------|
| Nome            | oFog                                                                                            |
| Conteggio           | Un vettore, di cui può essere usato un solo componente e deve essere specificato dalla maschera del componente |
| Autorizzazioni di I/O | Sola scrittura.                                                                                     |



 

Il valore di output viene registrato. Il valore è il fattore di interpolazione da interpolare e quindi instradare alla tabella delle stabilimenti. Viene usato solo il componente x scalare dell'oggetto .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri vertex shader](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




