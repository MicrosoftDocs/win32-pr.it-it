---
title: opzione/Win64
description: L'opzione/Win64 indica al compilatore MIDL di generare file stub o un file di libreria dei tipi per un ambiente a 64 bit. Nota Questa opzione è obsoleta.
ms.assetid: 6f4780d3-6415-42af-a8ee-3884a8cebe26
keywords:
- /Win64 switch MIDL
topic_type:
- apiref
api_name:
- /win64
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e61906126607c0a8d4b81ef76805bb4b7e0d4145
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104333692"
---
# <a name="win64-switch"></a>opzione/Win64

L'opzione **/Win64** indica al compilatore MIDL di generare file stub o un file di libreria dei tipi per un ambiente a 64 bit.

> [!Note]  
> Questa opzione è obsoleta. Usare invece l'opzione [**/ia64**](-ia64.md) o [**/amd64**](-amd64.md) . L'opzione **/Win64** equivale all'opzione **/ia64** .

 

``` syntax
midl /win64
```

## <a name="switch-options"></a>Opzioni switch

Questa opzione non ha parametri.

## <a name="remarks"></a>Commenti

L'opzione **/Win64** equivale a impostare l'opzione [**/ENV**](-env.md) su Win64.

> [!Note]  
> Non è possibile usare MIDL.exe per produrre un TLB a 64 bit in Windows 2000.

 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**/ENV**](-env.md)
</dt> <dt>

[**/ia64**](-ia64.md)
</dt> <dt>

[**/amd64**](-amd64.md)
</dt> </dl>

 

 




