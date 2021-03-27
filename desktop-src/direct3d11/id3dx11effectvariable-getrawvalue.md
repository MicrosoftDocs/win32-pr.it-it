---
title: Metodo ID3DX11EffectVariable GetRawValue (D3dx11effect. h)
description: Recuperare i dati.
ms.assetid: 1b2a319c-880c-4f5a-b4e9-17405351b7d9
keywords:
- Metodo GetRawValue Direct3D 11
- Metodo GetRawValue Direct3D 11, interfaccia ID3DX11EffectVariable
- Interfaccia ID3DX11EffectVariable Direct3D 11, metodo GetRawValue
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetRawValue
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be03051433e3ae4fd5891d1859529bb305b08bb0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982475"
---
# <a name="id3dx11effectvariablegetrawvalue-method"></a>Metodo ID3DX11EffectVariable:: GetRawValue

Recuperare i dati.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetRawValue(
   void *pData,
   UINT Offset,
   UINT Count
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pData* 
</dt> <dd>

Tipo: **void \***

Puntatore alla variabile.

</dd> <dt>

*Offset* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Offset (in byte) dall'inizio del puntatore ai dati.

</dd> <dt>

*Count* 
</dt> <dd>

Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Numero di byte da ottenere.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Restituisce uno dei seguenti [codici restituiti Direct3D 11](d3d11-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Commenti

Questo metodo non esegue alcuna conversione o controllo dei tipi; si tratta quindi di un modo molto rapido per accedere agli elementi della matrice.

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

 

