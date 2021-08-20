---
description: Ottiene un elenco di formati pixel non compressi di cui è possibile eseguire il rendering usando un profilo DXVA (DirectX Video Acceleration) specificato.
ms.assetid: 7c69ea5f-6054-4430-95b5-820db6854fc0
title: Metodo IDirect3DVideoDevice9::GetUncompressedDXVAFormats (Dxva.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetUncompressedDXVAFormats
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 3d7f27060d0c9e43f1852c86697826986c0c095c14a19fbfafa53978e96cbe79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117878798"
---
# <a name="idirect3dvideodevice9getuncompresseddxvaformats-method"></a>Metodo IDirect3DVideoDevice9::GetUncompressedDXVAFormats

Ottiene un elenco di formati pixel non compressi di cui è possibile eseguire il rendering usando un profilo DXVA (DirectX Video Acceleration) specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetUncompressedDXVAFormats(
   GUID      *pGuid,
   DWORD     *pNumFormats,
   D3DFORMAT *pFormats
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pGuid* 
</dt> <dd>

Puntatore a un GUID che specifica il profilo DXVA. Per ottenere un elenco dei profili supportati, chiamare [**IDirect3DVideoDevice9::GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md).

</dd> <dt>

*pNumFormats* 
</dt> <dd>

Nell'input specifica il numero di elementi nella *matrice pFormats.* Se *pFormats* è **NULL,** il valore di `*pNumFormats` deve essere zero.

Nell'output, *se pFormats* **è NULL,** *pNumFormats* riceve il numero di formati pixel supportati. In caso *contrario, pNumFormats* riceve il numero effettivo di formati di pixel copiati nella *matrice pFormats.*

</dd> <dt>

*pFormats* 
</dt> <dd>

Indirizzo di una matrice di **valori D3DFORMAT** o **NULL.** Se il valore è diverso **da NULL,** la matrice riceve un elenco di formati pixel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Commenti

Chiamare questo metodo due volte. Nella prima chiamata impostare *pFormats* su **NULL.** Il *parametro pNumFormats* riceve il numero di formati. Allocare **una matrice D3DFORMAT** con le dimensioni richieste e chiamare di nuovo il metodo . Questa volta, impostare *pFormats* sull'indirizzo della matrice. Il metodo riempie la matrice con l'elenco di formati di pixel.

Il driver deve restituire i formati in ordine decrescente di preferenza, con il formato preferito elencato per primo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                    |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Dxva.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDirect3DVideoDevice9**](idirect3dvideodevice9.md)
</dt> </dl>

 

 




