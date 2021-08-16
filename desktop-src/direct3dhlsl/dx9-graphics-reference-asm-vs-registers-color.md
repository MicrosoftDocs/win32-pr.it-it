---
title: Registro colori
description: Questi registri di output del vertex shader contengono un valore di colore.
ms.assetid: fd36e207-7312-4c7e-b664-b2de9ba1ebcf
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b19850985002ad9c36a6a6366f744106cb041db858f9df9b755996e114fdf6c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118512287"
---
# <a name="color-register"></a>Registro colori

Questi registri di output del vertex shader contengono un valore di colore. 

| Registrazione | Descrizione              |
|----------|--------------------------|
| oD0      | registro colori diffusa.  |
| oD1      | registro dei colori speculari. |



 

Il valore oD0 è interpolato e viene scritto nel registro pixel shader colore 0 (v0). Il valore oD1 viene interpolato e scritto nel registro pixel shader colore 1 (v1). Per altre informazioni sui pixel shader dei colori, vedere l'argomento pixel shader [Input Color Register (Registro](dx9-graphics-reference-asm-ps-registers-input-color.md) colori di input).

## <a name="remarks"></a>Commenti

Esempio


```
min oD0, r0, c1.x    
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri vertex shader](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




