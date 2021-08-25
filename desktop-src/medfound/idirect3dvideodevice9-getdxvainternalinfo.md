---
description: Esegue query sulla quantità di memoria scratch allocata dal livello di astrazione hardware (HAL) per l'uso privato.
ms.assetid: 20e3dbef-daf5-487a-8d50-e2ebdb712cc0
title: Metodo IDirect3DVideoDevice9::GetDXVAInternalInfo (Dxva.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetDXVAInternalInfo
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: dd15dfdbd35db56262487482e811210970852dcee4e791d710e0551b84e9e620
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777211"
---
# <a name="idirect3dvideodevice9getdxvainternalinfo-method"></a>Metodo IDirect3DVideoDevice9::GetDXVAInternalInfo

Esegue query sulla quantità di memoria scratch allocata dal livello di astrazione hardware (HAL) per l'uso privato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetDXVAInternalInfo(
   GUID               *pGuid,
   DXVAUncompDataInfo *pUncompData,
   DWORD              *pMemoryUsed
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pGuid* 
</dt> <dd>

Puntatore a un GUID che specifica il profilo DXVA. Per ottenere un elenco dei profili supportati, chiamare [**IDirect3DVideoDevice9::GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md).

</dd> <dt>

*pUncompData* 
</dt> <dd>

Puntatore a [**una struttura DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) che specifica le dimensioni e il formato pixel dei dati non compressi.

</dd> <dt>

*pMemoryUsed* 
</dt> <dd>

Riceve la quantità di memoria virtuale allocata dall'HAL, in byte.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                    |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>Dxva.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDirect3DVideoDevice9**](idirect3dvideodevice9.md)
</dt> </dl>

 

 




