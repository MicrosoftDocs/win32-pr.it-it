---
title: Funzione CommandListCast (D3dx12. h)
description: Questo modello di funzione esegue il cast di un puntatore costante a un elenco di comandi in un puntatore const a un ID3D12CommandList.
ms.assetid: 63719AA1-2119-456C-9D23-13933D38AFA9
keywords:
- CommandListCast (funzione)
topic_type:
- apiref
api_name:
- CommandListCast
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81a740258f74975fecac3e1a4df2412f1fae92f3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323430"
---
# <a name="commandlistcast-function"></a>CommandListCast (funzione)

Questo modello di funzione esegue il cast di un puntatore costante a un elenco di comandi in un puntatore const a un ID3D12CommandList.

Questo cast è utile per passare puntatori di elenchi di comandi fortemente tipizzati in [**oggetti executecommandlist**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).

## <a name="syntax"></a>Sintassi


```C++
ID3D12CommandList * const * inline CommandListCast(
   t_CommandListType * const * pp
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PP* 
</dt> <dd>

Tipo: **t \_ CommandListType \* const \***

Elenco di comandi fortemente tipizzati di cui eseguire il cast.

L'argomento di modello **t \_ CommandListType** specifica un oggetto elenco di comandi fortemente tipizzato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **ID3D12CommandList \* const \***

Elenco di comandi fortemente tipizzati, reinterpretato come un [**ID3D12CommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandlist).

## <a name="remarks"></a>Commenti

CommandListCast esegue un **\_ cast di reinterpretazione**. Il cast è valido finché viene rispettata la const dell'elenco dei comandi.

La funzione CommandListCast è definita come segue:


```C++
template <typename t_CommandListType>
inline ID3D12CommandList * const * CommandListCast(t_CommandListType * const * pp)
{
    return reinterpret_cast<ID3D12CommandList * const *>(pp);
}
          
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Libreria<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni helper per D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

 





