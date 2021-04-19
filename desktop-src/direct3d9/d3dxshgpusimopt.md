---
description: Descrive la risoluzione del buffer z dell'ombreggiatura che verrà usata nella simulazione di illuminazione diretta PRT (pre-Computed Radiance Transfer) nella GPU.
ms.assetid: 05354328-9b6f-45f5-a913-47ede170b03f
title: Enumerazione D3DXSHGPUSIMOPT (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHGPUSIMOPT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: a94845faf4c34657f486cfa371c5d41a12dc4336
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323301"
---
# <a name="d3dxshgpusimopt-enumeration"></a>Enumerazione D3DXSHGPUSIMOPT

Descrive la risoluzione del buffer z dell'ombreggiatura che verrà usata nella simulazione di illuminazione diretta PRT (pre-Computed Radiance Transfer) nella GPU. È anche possibile specificare un buffer z di qualità superiore per ridurre il rumore nei risultati della simulazione di illuminazione diretta, anche se la simulazione sarà più lenta.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DXSHGPUSIMOPT { 
  D3DXSHGPUSIMOPT_SHADOWRES256   = 1,
  D3DXSHGPUSIMOPT_SHADOWRES512   = 0,
  D3DXSHGPUSIMOPT_SHADOWRES1024  = 2,
  D3DXSHGPUSIMOPT_SHADOWRES2048  = 3,
  D3DXSHGPUSIMOPT_HIGHQUALITY    = 4,
  D3DXSHGPUSIMOPT_FORCE_DWORD    = 0x7fffffff
} D3DXSHGPUSIMOPT, *LPD3DXSHGPUSIMOPT;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DXSHGPUSIMOPT_SHADOWRES256"></span><span id="d3dxshgpusimopt_shadowres256"></span>**\_SHADOWRES256 D3DXSHGPUSIMOPT**
</dt> <dd>

Simulazione a bassa risoluzione. Per codificare il buffer z dell'ombreggiatura viene utilizzata una trama con pixel 256 x 256.

</dd> <dt>

<span id="D3DXSHGPUSIMOPT_SHADOWRES512"></span><span id="d3dxshgpusimopt_shadowres512"></span>**\_SHADOWRES512 D3DXSHGPUSIMOPT**
</dt> <dd>

Simulazione di media risoluzione. Per codificare il buffer z dell'ombreggiatura viene utilizzata una trama con pixel 512 x 512. Si tratta del valore predefinito.

</dd> <dt>

<span id="D3DXSHGPUSIMOPT_SHADOWRES1024"></span><span id="d3dxshgpusimopt_shadowres1024"></span>**\_SHADOWRES1024 D3DXSHGPUSIMOPT**
</dt> <dd>

Simulazione ad alta risoluzione. Per codificare il buffer z dell'ombreggiatura viene utilizzata una trama con pixel 1024 x 1024.

</dd> <dt>

<span id="D3DXSHGPUSIMOPT_SHADOWRES2048"></span><span id="d3dxshgpusimopt_shadowres2048"></span>**\_SHADOWRES2048 D3DXSHGPUSIMOPT**
</dt> <dd>

Simulazione con la massima risoluzione. Per codificare il buffer z dell'ombreggiatura viene utilizzata una trama con pixel 2048 x 2048.

</dd> <dt>

<span id="D3DXSHGPUSIMOPT_HIGHQUALITY"></span><span id="d3dxshgpusimopt_highquality"></span>**\_Highquality D3DXSHGPUSIMOPT**
</dt> <dd>

La simulazione ha una precisione elevata, indipendentemente dalla risoluzione selezionata. L'impostazione di questo valore ridurrà il rumore nei risultati della simulazione di illuminazione diretta, anche se la simulazione sarà più lenta. Può essere combinato con uno dei valori di risoluzione.

</dd> <dt>

<span id="D3DXSHGPUSIMOPT_FORCE_DWORD"></span><span id="d3dxshgpusimopt_force_dword"></span>**D3DXSHGPUSIMOPT \_ Force \_ DWORD**
</dt> <dd>

Impone la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile specificare solo uno dei valori di risoluzione e può essere combinato con il valore di alta qualità.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




