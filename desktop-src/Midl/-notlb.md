---
title: opzione/notlb
description: L'opzione/notlb impedisce al compilatore MIDL di generare un file della libreria dei tipi (TLB).
ms.assetid: 58f4210d-d3c3-42ce-b311-4ddd85bc396a
keywords:
- /notlb switch MIDL
topic_type:
- apiref
api_name:
- /notlb
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81911b6afb00d61713f966ba9e1981b979e51008
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104471966"
---
# <a name="notlb-switch"></a>opzione/notlb

L'opzione **/notlb** impedisce al compilatore MIDL di generare un file della libreria dei tipi (tlb).

``` syntax
midl /notlb
```

## <a name="switch-options"></a>Opzioni switch

Questa opzione non ha parametri.

## <a name="remarks"></a>Commenti

Per impostazione predefinita, il compilatore MIDL genererà un file TLB ogni volta che viene rilevata un'istruzione di [**libreria**](library.md) . Questa opzione sostituisce il comportamento predefinito.

Quando si specifica l'opzione **/notlb** , tutti gli altri Stub, intestazioni e così via vengono generati come di consueto.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**/TLB**](-tlb.md)
</dt> </dl>

 

 




