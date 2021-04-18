---
description: Esegue un'operazione di decodifica DXVA (DirectX Video Acceleration).
ms.assetid: cb87a087-ca53-470e-ab46-f4022cfd7869
title: 'Metodo IDirect3DDXVADevice9:: Execute (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.Execute
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: d624146c32b5f7eaeb4e680cf03878e8d065ee5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310838"
---
# <a name="idirect3ddxvadevice9execute-method"></a>Metodo IDirect3DDXVADevice9:: Execute

Esegue un'operazione di decodifica DXVA (DirectX Video Acceleration).

## <a name="syntax"></a>Sintassi


```C++
HRESULT Execute(
   DWORD          FunctionNum,
   VOID           *pInputData,
   DWORD          InputSize,
   VOID           *OutputData,
   DWORD          OutputSize,
   DWORD          NumBuffers,
   DXVABufferInfo *pBufferInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*FunctionNum* 
</dt> <dd>

**Valore DWORD** che contiene uno o più numeri di funzione DXVA. Per informazioni dettagliate, vedere la [specifica DXVA 1,0](/windows-hardware/drivers/display/directx-video-acceleration).

</dd> <dt>

*pInputData* 
</dt> <dd>

Puntatore a un buffer che contiene i dati di input per l'operazione di decodifica. Il significato di questi dati dipende dal tipo di superficie e dal numero di funzione.

</dd> <dt>

*InputSize* 
</dt> <dd>

Dimensioni in byte dei dati di input.

</dd> <dt>

*OutputData* 
</dt> <dd>

Puntatore a un buffer in cui l'acceleratore video scrive i dati di output.

</dd> <dt>

*OutputSize* 
</dt> <dd>

Dimensioni in byte del buffer *outputData* .

</dd> <dt>

*NumBuffers* 
</dt> <dd>

Numero di elementi nella matrice *pBufferInfo* .

</dd> <dt>

*pBufferInfo* 
</dt> <dd>

Puntatore a una matrice di strutture [**DXVABufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvabufferinfo) .

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

 

 
