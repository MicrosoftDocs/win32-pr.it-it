---
description: 'Funzione D3DX10CheckVersion: verificare che la versione di D3DX compilata con sia la versione in esecuzione.'
ms.assetid: 57085b07-f77b-425e-a889-22c3071d7143
title: Funzione D3DX10CheckVersion (D3DX10Core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CheckVersion
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4fc8befa88fb706965a30224843745b033ea205b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105349"
---
# <a name="d3dx10checkversion-function"></a>Funzione D3DX10CheckVersion

Verificare che la versione di D3DX compilata con sia la versione in esecuzione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT D3DX10CheckVersion(
  _In_ UINT D3DSdkVersion,
  _In_ UINT D3DX10SdkVersion
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*D3DSdkVersion* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Usare D3D10 \_ SDK \_ VERSION. Vedere la sezione Osservazioni.

</dd> <dt>

*D3DX10SdkVersion* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Usare D3DX10 \_ SDK \_ VERSION. Vedere la sezione Osservazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la versione non corrisponde, la funzione restituirà FALSE (un numero minore o uguale a 0, il numero stesso non ha significato).

## <a name="remarks"></a>Commenti

Usare questa funzione durante l'inizializzazione dell'applicazione.


```
HRESULT hr;
    
if( FAILED( D3DX10CheckVersion(D3D10_SDK_VERSION, D3DX10_SDK_VERSION) ) )
    return E_FAIL;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10Core.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[per utilizzo generico funzioni](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
