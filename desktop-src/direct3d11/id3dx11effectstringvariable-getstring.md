---
title: Metodo GetString ID3DX11EffectStringVariable (D3dx11effect. h)
description: Ottiene la stringa.
ms.assetid: ce96ae18-d316-41ba-9b2a-eac084b86098
keywords:
- Metodo GetString Direct3D 11
- Metodo GetString Direct3D 11, interfaccia ID3DX11EffectStringVariable
- Interfaccia ID3DX11EffectStringVariable Direct3D 11, metodo GetString
topic_type:
- apiref
api_name:
- ID3DX11EffectStringVariable.GetString
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15d15666bd70bf00395b7052b7820981dd8d0dcd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982142"
---
# <a name="id3dx11effectstringvariablegetstring-method"></a>Metodo ID3DX11EffectStringVariable:: GetString

Ottiene la stringa.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetString(
   LPCSTR *ppString
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppString* 
</dt> <dd>

Tipo: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)\***

Puntatore alla stringa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Commenti

> [!Note]  
> DirectX SDK non fornisce binari compilati per gli effetti. È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects. Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectStringVariable](id3dx11effectstringvariable.md)
</dt> </dl>

 

