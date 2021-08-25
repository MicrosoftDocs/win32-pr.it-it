---
description: 'Funzione D3DXCheckVersion: verificare che la versione di D3DX compilata con sia la versione in esecuzione.'
ms.assetid: a4e745dd-d573-4e8f-9516-f6a7475f5cc5
title: Funzione D3DXCheckVersion (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckVersion
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 26831f3a1a5f08494a7382cd412c30dcd24c1482c01dca684962a580068d380d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894121"
---
# <a name="d3dxcheckversion-function"></a>Funzione D3DXCheckVersion

Verificare che la versione di D3DX compilata con sia la versione in esecuzione.

## <a name="syntax"></a>Sintassi


```C++
BOOL D3DXCheckVersion(
  _In_ UINT D3DSDKVersion,
  _In_ UINT D3DXSDKVersion
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*D3DSDKVersion* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Usare D3D \_ SDK \_ VERSION. Vedere la sezione Osservazioni.

</dd> <dt>

*D3DXSDKVersion* \[ Pollici\]
</dt> <dd>

Tipo: **[ **UINT**](../winprog/windows-data-types.md)**

Usare D3DX \_ SDK \_ VERSION. Vedere la sezione Osservazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**

Restituisce **TRUE** se la versione di D3DX compilata è la versione in esecuzione. In caso contrario, **viene** restituito FALSE.

## <a name="remarks"></a>Commenti

Usare questa funzione durante l'inizializzazione dell'applicazione in questo modo:


```
HRESULT CD3DXMyApplication::Initialize(HINSTANCE hInstance, 
  LPCSTR szWindowName, LPCSTR szClassName, UINT uWidth, UINT uHeight)
{
    HRESULT hr;
    
    if (!D3DXCheckVersion(D3D_SDK_VERSION, D3DX_SDK_VERSION))
        return E_FAIL;
    
    ...
}
```



Usare [**Direct3DCreate9**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9) per verificare che sia installato il runtime corretto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Per utilizzo generico funzioni](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
