---
description: Usato per decomprimere i dati codificati. In genere viene usato per caricare le risorse dai file system, ad esempio i file ZIP. Quando si carica da una risorsa non compressa, la fase di decompressione non deve eseguire alcuna operazione.
ms.assetid: 7f7e3ffd-8dac-403f-813b-d6d21d146fa7
title: Metodo ID3DX10DataLoader::D ecompress (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataLoader.Decompress
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: c9e532bae8cb121fc93f3fdf2a5a1ee23e597c66599277b73b3b36b15ebbb963
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989121"
---
# <a name="id3dx10dataloaderdecompress-method"></a>Metodo ID3DX10DataLoader::D ecompress

Usato per decomprimere i dati codificati. In genere viene usato per caricare le risorse dai file system, ad esempio i file ZIP. Quando si carica da una risorsa non compressa, la fase di decompressione non deve eseguire alcuna operazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Decompress(
  [out] void   **ppData,
  [in]  SIZE_T *pcBytes
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppData* \[ Cambio\]
</dt> <dd>

Tipo: **\* \* void**

Puntatore ai dati non elaborati da decomprimere.

</dd> <dt>

*pcBytes* \[ Pollici\]
</dt> <dd>

Tipo: **[ **SIZE \_ T**](../winprog/windows-data-types.md)\***

Dimensioni dei dati a cui punta ppData.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in Codici restituiti [Direct3D 10.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

[**È possibile ereditare l'interfaccia ID3DX10DataLoader**](id3dx10dataloader.md) e ridefinirne i membri. È possibile ridefinire la decompressione per supportare formati di file personalizzati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX10DataLoader](id3dx10dataloader.md)
</dt> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
