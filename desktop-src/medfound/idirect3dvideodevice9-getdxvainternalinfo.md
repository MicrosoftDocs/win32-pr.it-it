---
description: Esegue una query per la quantità di memoria Scratch che l'HAL (Hardware Abstraction Layer) alloca per l'uso privato.
ms.assetid: 20e3dbef-daf5-487a-8d50-e2ebdb712cc0
title: 'Metodo IDirect3DVideoDevice9:: GetDXVAInternalInfo (DXVA. h)'
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
ms.openlocfilehash: aa512130b622d192acc37d8c309f462f8ecc87e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308752"
---
# <a name="idirect3dvideodevice9getdxvainternalinfo-method"></a>Metodo IDirect3DVideoDevice9:: GetDXVAInternalInfo

Esegue una query per la quantità di memoria Scratch che l'HAL (Hardware Abstraction Layer) alloca per l'uso privato.

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

Puntatore a un GUID che specifica il profilo DXVA. Per ottenere un elenco dei profili supportati, chiamare [**IDirect3DVideoDevice9:: GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md).

</dd> <dt>

*pUncompData* 
</dt> <dd>

Puntatore a una struttura [**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) che specifica le dimensioni e il formato pixel dei dati non compressi.

</dd> <dt>

*pMemoryUsed* 
</dt> <dd>

Riceve la quantità di memoria Scratch che l'HAL allocherà in byte.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                    |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                              |
| Intestazione<br/>                   | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDirect3DVideoDevice9**](idirect3dvideodevice9.md)
</dt> </dl>

 

 




