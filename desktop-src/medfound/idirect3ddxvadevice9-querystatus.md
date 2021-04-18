---
description: Esegue una query sullo stato di lettura/scrittura di una superficie di decodifica DXVA (DirectX Video Acceleration).
ms.assetid: 8a4c3173-5911-49ec-8cb8-e30f96a4f1c9
title: 'Metodo IDirect3DDXVADevice9:: QueryStatus (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.QueryStatus
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: ae2b16ef27b1e172b7927652304104563e120709
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308754"
---
# <a name="idirect3ddxvadevice9querystatus-method"></a>Metodo IDirect3DDXVADevice9:: QueryStatus

Esegue una query sullo stato di lettura/scrittura di una superficie di decodifica DXVA (DirectX Video Acceleration).

## <a name="syntax"></a>Sintassi


```C++
HRESULT QueryStatus(
   IDirect3DSurface9 *pSurface,
   DWORD             Flags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSurface* 
</dt> <dd>

Puntatore all'interfaccia **IDirect3DSurface9** della superficie su cui eseguire una query.

</dd> <dt>

*Flag* 
</dt> <dd>

Specifica il tipo di query da eseguire.



| Valore                                                                                                                             | Significato                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="0x00"></span><span id="0X00"></span><dl> <dt>**0x00**</dt> </dl> | Verificare se la superficie è sicura da utilizzare per la scrittura.<br/> |
| <span id="0x01"></span><span id="0X01"></span><dl> <dt>**0x01**</dt> </dl> | Verificare se la superficie è sicura da utilizzare per la lettura.<br/> |



 

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

[**IDirect3DDXVADevice9**](idirect3ddxvadevice9.md)
</dt> </dl>

 

 




