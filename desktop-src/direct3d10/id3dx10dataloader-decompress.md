---
description: Utilizzato per decomprimere i dati codificati. Questa operazione viene in genere utilizzata per caricare le risorse da file System, ad esempio file ZIP. Quando si esegue il caricamento da una risorsa non compressa, la fase di decompressione non deve eseguire alcuna operazione.
ms.assetid: 7f7e3ffd-8dac-403f-813b-d6d21d146fa7
title: Metodo ID3DX10DataLoader::D eComPress (D3DX10. h)
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
ms.openlocfilehash: e6f711722852cba4b671cc84416055d279fd7cc6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322763"
---
# <a name="id3dx10dataloaderdecompress-method"></a>ID3DX10DataLoader::D Metodo eComPress

Utilizzato per decomprimere i dati codificati. Questa operazione viene in genere utilizzata per caricare le risorse da file System, ad esempio file ZIP. Quando si esegue il caricamento da una risorsa non compressa, la fase di decompressione non deve eseguire alcuna operazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Decompress(
  [out] void   **ppData,
  [in]  SIZE_T *pcBytes
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppData* \[ out\]
</dt> <dd>

Tipo: **void \* \***

Puntatore ai dati non elaborati da decomprimere.

</dd> <dt>

*pcBytes* \[ in\]
</dt> <dd>

Tipo: **[ **size \_ T**](../winprog/windows-data-types.md)\***

Dimensione dei dati a cui punta ppData.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Commenti

L' [**interfaccia ID3DX10DataLoader**](id3dx10dataloader.md) può essere ereditata e i relativi membri sono stati ridefiniti. Decomprimere può essere ridefinito per supportare formati di file personalizzati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX10DataLoader](id3dx10dataloader.md)
</dt> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
