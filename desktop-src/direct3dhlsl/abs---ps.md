---
title: abs - ps
description: Calcola il valore assoluto. | abs - ps
ms.assetid: e97db550-2a03-421a-86f4-a6fc5f8e0bca
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e3e7af7b2d30e9d9f2092cb6671610f008ec781d
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994878"
---
# <a name="abs---ps"></a>abs - ps

Calcola il valore assoluto.

## <a name="syntax"></a>Sintassi



|              |
|--------------|
| abs dst, src |



 

dove

-   dst è il registro di destinazione.
-   src è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| abs                   |      |      |      |      | x    | x    | x     | x    | x     |



 

Questa istruzione funziona come illustrato di seguito.


```
dest.x = abs(src.x)
dest.y = abs(src.y)
dest.z = abs(src.z)
dest.w = abs(src.w)
```



## <a name="instruction-information"></a>Informazioni sulle istruzioni



|                          |            |
|--------------------------|------------|
| Sistema operativo minimo | Windows 98 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




