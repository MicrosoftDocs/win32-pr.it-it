---
title: Metodo ID3DX11EffectVariable GetMemberByIndex (D3dx11effect. h)
description: Ottiene un membro della struttura in base all'indice.
ms.assetid: 256f65aa-5f49-4b83-8dde-ddb6b31c581a
keywords:
- Metodo GetMemberByIndex Direct3D 11
- Metodo GetMemberByIndex Direct3D 11, interfaccia ID3DX11EffectVariable
- Interfaccia ID3DX11EffectVariable Direct3D 11, metodo GetMemberByIndex
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetMemberByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4be490251a83907dcd16231d62d492caf05768f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995978"
---
# <a name="id3dx11effectvariablegetmemberbyindex-method"></a>Metodo ID3DX11EffectVariable:: GetMemberByIndex

Ottiene un membro della struttura in base all'indice.

## <a name="syntax"></a>Sintassi


```C++
ID3DX11EffectVariable* GetMemberByIndex(
   UINT Index
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Index* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Indice a base zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **ID3DX11EffectVariable**](id3dx11effectvariable.md)\***

Puntatore a un [**ID3DX11EffectVariable**](id3dx11effectvariable.md).

## <a name="remarks"></a>Commenti

Se la variabile Effect è una struttura, usare questo metodo per cercare un membro in base all'indice.

> [!Note]  
> DirectX SDK non fornisce binari compilati per gli effetti. È necessario usare Effects 11 source per compilare l'applicazione di tipo Effects. Per ulteriori informazioni sull'utilizzo dell'origine Effects 11, vedere [differenze tra gli effetti 10 e gli effetti 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Libreria<br/> | <dl> <dt>N/d (la libreria Effects 11 è disponibile online come origine condivisa).</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

