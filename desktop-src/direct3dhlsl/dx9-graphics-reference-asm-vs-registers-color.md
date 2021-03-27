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
ms.openlocfilehash: 38ee29ebafd9e7374fa868c6d84ad45f6c07dedf
ms.sourcegitcommit: 3f366316c02c411c4c5e14620a699f6f30608634
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/04/2021
ms.locfileid: "104350871"
---
# <a name="color-register"></a>Registro colori

Questi registri di output del vertex shader contengono un valore di colore. 

| Registrazione | Descrizione              |
|----------|--------------------------|
| oD0      | registro colori diffuso.  |
| oD1      | registro colori speculare. |



 

Il valore oD0 viene interpolato e viene scritto nel registro colori pixel shader 0 (V0). Il valore oD1 viene interpolato e scritto nel registro colori pixel shader 1 (V1). Per ulteriori informazioni sui registri dei colori pixel shader, vedere l'argomento pixel shader [Registro colori input](dx9-graphics-reference-asm-ps-registers-input-color.md) .

## <a name="remarks"></a>Commenti

Esempio


```
min oD0, r0, c1.x    
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registri vertex shader](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




