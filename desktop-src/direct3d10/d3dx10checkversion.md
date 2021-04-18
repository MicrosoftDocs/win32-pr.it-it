---
description: Verificare che la versione di D3DX compilata con sia la versione in esecuzione.
ms.assetid: 57085b07-f77b-425e-a889-22c3071d7143
title: Funzione D3DX10CheckVersion (D3DX10Core. h)
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
ms.openlocfilehash: 3b41996f16cb97d91dc59f8d368f13b905992388
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323381"
---
# <a name="d3dx10checkversion-function"></a>D3DX10CheckVersion (funzione)

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

*D3DSdkVersion* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Usare la \_ versione dell'SDK di D3D10 \_ . Vedere la sezione Osservazioni.

</dd> <dt>

*D3DX10SdkVersion* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Usare la \_ versione dell'SDK di d3dx10 \_ . Vedere la sezione Osservazioni.

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
| Intestazione<br/>  | <dl> <dt>D3DX10Core. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni per utilizzo generico](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
