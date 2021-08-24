---
title: Funzione D3D12CalcSubresource (D3dx12.h)
description: Calcola un indice di sottorisorsa per una trama.
ms.assetid: 5C63A315-E21E-498B-A832-6BA2D17FF9A7
keywords:
- Funzione D3D12CalcSubresource
topic_type:
- apiref
api_name:
- D3D12CalcSubresource
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08c704be7087d95d739685bc2823ec1c31a027b4406a3110986220927fdbbffa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751721"
---
# <a name="d3d12calcsubresource-function"></a>Funzione D3D12CalcSubresource

Calcola un indice di sottorisorsa per una trama.

## <a name="syntax"></a>Sintassi


```C++
UINT inline D3D12CalcSubresource(
   UINT MipSlice,
   UINT ArraySlice,
   UINT PlaneSlice,
   UINT MipLevels,
   UINT ArraySize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*MipSlice* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Indice in base zero per il livello mipmap da risolvere. 0 indica il primo livello di mipmap più dettagliato.

</dd> <dt>

*ArraySlice* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Indice in base zero per il livello di matrice da risolvere. usare sempre 0 per le trame di volume (3D).

</dd> <dt>

*PlaneSlice* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Indice in base zero per il livello del piano da risolvere.

</dd> <dt>

*MipLevels* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Numero di livelli mipmap nella risorsa.

</dd> <dt>

*ArraySize* 
</dt> <dd>

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Numero di elementi nella matrice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Indice uguale a MipSlice + (ArraySlice \* MipLevels).

## <a name="remarks"></a>Commenti

Un buffer è una risorsa non strutturata e viene quindi definito come contenente una singola sottorisorsa. Le API che accettano buffer non necessitano di un indice di sottorisorsa. Una trama, d'altra parte, è altamente strutturata. Ogni oggetto trama può contenere una o più sottorisorse a seconda delle dimensioni della matrice e del numero di livelli di mipmap.

Per le trame di volume (3D), tutte le sezioni per un determinato livello di mipmap sono un singolo indice di sottorisorsa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx12.h</dt> </dl>  |
| Libreria<br/> | <dl> <dt>D3D12.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni helper per D3D12](helper-functions-for-d3d12.md)
</dt> <dt>

[Sottorisorse](subresources.md)
</dt> </dl>

 

