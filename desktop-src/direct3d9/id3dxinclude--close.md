---
description: Metodo implementato dall'utente per la chiusura di un \# file di inclusione dello shader.
ms.assetid: de54ce56-3884-443a-9879-4e7290bcfb8d
title: 'Metodo ID3DXInclude:: Close (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXInclude.Close
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b60d01d59a4e54fa0d50c16a3fc845ea4e316792
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323537"
---
# <a name="id3dxincludeclose-method"></a>Metodo ID3DXInclude:: Close

Metodo implementato dall'utente per la chiusura di un \# file di inclusione dello shader.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Close(
  [in] LPCVOID pData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pData* \[ in\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntatore al buffer restituito che contiene le direttive include. Si tratta del puntatore restituito dalla chiamata [**ID3DXInclude:: Open**](id3dxinclude--open.md) corrispondente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il metodo implementato dall'utente deve restituire S \_ OK. Se il callback ha esito negativo durante la lettura del \# file di inclusione, l'API che ha causato la chiamata al callback avrà esito negativo. I possibili valori sono i seguenti:

-   Lo shader HLSL non riuscirà a eseguire una delle \* \* \* funzioni D3DXCompileShader.
-   L'assembly shader non riuscirà a eseguire una delle \* \* \* funzioni D3DXAssembleShader.
-   L'effetto avrà esito negativo per una delle \* \* \* funzioni D3DXCreateEffect o D3DXCreateEffectCompiler \* \* \* .

## <a name="remarks"></a>Commenti

Se [**ID3DXInclude:: Open**](id3dxinclude--open.md) ha avuto esito positivo, viene garantita la chiamata a **ID3DXInclude:: Close** prima che l'API che usa questa interfaccia restituisca.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Shader. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXInclude](id3dxinclude.md)
</dt> <dt>

[**ID3DXInclude:: Open**](id3dxinclude--open.md)
</dt> </dl>

 

 
