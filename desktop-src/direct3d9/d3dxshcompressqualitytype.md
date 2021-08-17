---
description: Impostazione di compressione sferica aricale (SH).
ms.assetid: 214d6efb-419d-4eea-8360-322885c26bc3
title: Enumerazione D3DXSHCOMPRESSQUALITYTYPE (D3dx9mesh.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHCOMPRESSQUALITYTYPE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 482483bb38c708c9b09004d48bd4f1e1e0ec0e4b9463a6d20f210b4fe8b1d44c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117731279"
---
# <a name="d3dxshcompressqualitytype-enumeration"></a>Enumerazione D3DXSHCOMPRESSQUALITYTYPE

Impostazione di compressione sferica aricale (SH).

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DXSHCOMPRESSQUALITYTYPE { 
  D3DXSHCQUAL_FASTLOWQUALITY   = 1,
  D3DXSHCQUAL_SLOWHIGHQUALITY  = 2,
  D3DXSHCQUAL_FORCE_DWORD      = 0x7fffffff
} D3DXSHCOMPRESSQUALITYTYPE, *LPD3DXSHCOMPRESSQUALITYTYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DXSHCQUAL_FASTLOWQUALITY"></span><span id="d3dxshcqual_fastlowquality"></span>**D3DXSHCQUAL \_ FASTLOWQUALITY**
</dt> <dd>

La compressione dei dati è di bassa qualità, ma è veloce da comprimere.

</dd> <dt>

<span id="D3DXSHCQUAL_SLOWHIGHQUALITY"></span><span id="d3dxshcqual_slowhighquality"></span>**D3DXSHCQUAL \_ SLOWHIGHQUALITY**
</dt> <dd>

La compressione dei dati è di alta qualità, ma la compressione è lenta.

</dd> <dt>

<span id="D3DXSHCQUAL_FORCE_DWORD"></span><span id="d3dxshcqual_force_dword"></span>**D3DXSHCQUAL \_ FORCE \_ DWORD**
</dt> <dd>

Forza la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori consentirebbero la compilazione di questa enumerazione a una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9mesh.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




