---
description: Crea un dispositivo di decodificatore DirectX Video Acceleration (DXVA).
ms.assetid: aeebf65f-1bde-4a33-87cd-25c62dcc0248
title: 'Metodo IDirect3DVideoDevice9:: CreateDXVADevice (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.CreateDXVADevice
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 50ce7cee350479f4286921b6cdf69b319033c721
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130342"
---
# <a name="idirect3dvideodevice9createdxvadevice-method"></a>Metodo IDirect3DVideoDevice9:: CreateDXVADevice

Crea un dispositivo di decodificatore DirectX Video Acceleration (DXVA).

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateDXVADevice(
   GUID                 *pGuid,
   DXVAUncompDataInfo   *pUncompData,
   LPVOID               pData,
   DWORD                DataSize,
   IDirect3DDXVADevice9 **ppDXVADevice
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pGuid* 
</dt> <dd>

Puntatore a un GUID che specifica il dispositivo da creare.

</dd> <dt>

*pUncompData* 
</dt> <dd>

Puntatore a una struttura [**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) che specifica il formato dell'immagine non compressa.

</dd> <dt>

*pData* 
</dt> <dd>

Puntatore a una struttura **DXVA \_ ConnectMode** che specifica la modalità DXVA e il profilo con restrizioni.

</dd> <dt>

*DataSize* 
</dt> <dd>

Dimensione della struttura **\_ ConnectMode di DXVA** in byte.

</dd> <dt>

*ppDXVADevice* 
</dt> <dd>

Riceve un puntatore all'interfaccia [**IDirect3DDXVADevice9**](idirect3ddxvadevice9.md) . Il chiamante deve rilasciare l'interfaccia.

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

 

 




