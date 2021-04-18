---
title: Funzione D3D12CalcSubresource (D3dx12. h)
description: Calcola un indice di una sottorisorsa per una trama.
ms.assetid: 5C63A315-E21E-498B-A832-6BA2D17FF9A7
keywords:
- D3D12CalcSubresource (funzione)
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
ms.openlocfilehash: e872d13ba5221ad50003d789b87f65fc64821dd0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322180"
---
# <a name="d3d12calcsubresource-function"></a>D3D12CalcSubresource (funzione)

Calcola un indice di una sottorisorsa per una trama.

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

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Indice in base zero per il livello mipmap da indirizzare; 0 indica il primo livello di mipmap più dettagliato.

</dd> <dt>

*ArraySlice* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Indice in base zero per il livello di matrice da indirizzare. usare sempre 0 per le trame del volume (3D).

</dd> <dt>

*PlaneSlice* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Indice in base zero per il livello del piano da indirizzare.

</dd> <dt>

*MipLevels* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Il numero di livelli di mipmap nella risorsa.

</dd> <dt>

*ArraySize* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Numero di elementi nella matrice.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Indice che equivale a MipSlice + (ArraySlice \* MipLevels).

## <a name="remarks"></a>Commenti

Un buffer è una risorsa non strutturata e pertanto viene definito come contenente una singola sottorisorsa. Le API che accettano i buffer non necessitano di un indice di sottorisorse. Un trame d'altra parte è altamente strutturato. Ogni oggetto texture può contenere una o più sottorisorse in base alle dimensioni della matrice e al numero di livelli di mipmap.

Per le trame volume (3D), tutte le sezioni per un determinato livello di mipmap sono un singolo indice di sottorisorsa.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Libreria<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni helper per D3D12](helper-functions-for-d3d12.md)
</dt> <dt>

[Sottorisorse](subresources.md)
</dt> </dl>

 

