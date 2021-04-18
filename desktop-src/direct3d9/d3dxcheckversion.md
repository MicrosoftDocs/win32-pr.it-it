---
description: Verificare che la versione di D3DX compilata con sia la versione in esecuzione.
ms.assetid: a4e745dd-d573-4e8f-9516-f6a7475f5cc5
title: Funzione D3DXCheckVersion (D3dx9core. h)
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
ms.openlocfilehash: 7b392d706e54780924115471906096f6b63d1a80
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323019"
---
# <a name="d3dxcheckversion-function"></a>D3DXCheckVersion (funzione)

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

*D3DSDKVersion* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Usare la \_ versione di D3D SDK \_ . Vedere la sezione Osservazioni.

</dd> <dt>

*D3DXSDKVersion* \[ in\]
</dt> <dd>

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Usare la \_ versione dell'SDK di D3DX \_ . Vedere la sezione Osservazioni.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **bool**](../winprog/windows-data-types.md)**

Restituisce **true** se la versione di D3DX compilata in base a è la versione in esecuzione con; in caso contrario, viene restituito **false** .

## <a name="remarks"></a>Commenti

Usare questa funzione durante l'inizializzazione dell'applicazione come la seguente:


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
| Intestazione<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni per utilizzo generico](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
