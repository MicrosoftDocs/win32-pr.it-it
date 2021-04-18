---
description: Restituisce il livello del driver.
ms.assetid: e8c85201-7850-4c8d-a124-ceb76d4e24d5
title: Funzione D3DXGetDriverLevel (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetDriverLevel
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 83f756f6b6ab5864f14e797879be243f871fb9e1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322668"
---
# <a name="d3dxgetdriverlevel-function"></a>D3DXGetDriverLevel (funzione)

Restituisce il livello del driver.

## <a name="syntax"></a>Sintassi


```C++
UINT D3DXGetDriverLevel(
  _In_ LPDIRECT3DDEVICE9 pDevice
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PDEVICE* \[ in\]
</dt> <dd>

Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) che rappresenta il dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **uint**](../winprog/windows-data-types.md)**

Livello del driver. Vedere la sezione Osservazioni.

## <a name="remarks"></a>Commenti

Questo metodo restituisce la versione del driver, che è una delle seguenti:

-   700-driver a livello di Direct3D 7
-   800-driver a livello Direct3D 8
-   900-driver a livello Direct3D 9

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx9core. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni per utilizzo generico](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
