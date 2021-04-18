---
description: Inizia l'elaborazione per creare un'immagine decodificata.
ms.assetid: 80471cc6-c66d-49d9-8593-780e41ac39b9
title: 'Metodo IDirect3DDXVADevice9:: BeginFrame (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.BeginFrame
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 3090d7868316d08fa91f36dffcc938eb31e06a7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310839"
---
# <a name="idirect3ddxvadevice9beginframe-method"></a>Metodo IDirect3DDXVADevice9:: BeginFrame

Inizia l'elaborazione per creare un'immagine decodificata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT BeginFrame(
   IDirect3DSurface9 *pDstSurface,
   DWORD             SizeInputData,
   VOID              *pInputData,
   DWORD             *pSizeOutputData,
   VOID              *pOutputData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDstSurface* 
</dt> <dd>

Puntatore all'interfaccia **IDirect3DSurface9** della superficie di destinazione non compressa.

</dd> <dt>

*SizeInputData* 
</dt> <dd>

Dimensioni del buffer specificato da *pInputData*, in byte. Il valore deve essere 2.

</dd> <dt>

*pInputData* 
</dt> <dd>

Puntatore a un buffer che contiene i dati per il tasto di scelta rapida del video. Questo buffer deve contenere l'indice del frame in base zero, specificato come valore di **parola** .

</dd> <dt>

*pSizeOutputData* 
</dt> <dd>

Dimensioni del buffer specificato da *pOutputData*, in byte. Il valore deve essere zero.

</dd> <dt>

*pOutputData* 
</dt> <dd>

Puntatore a un buffer in cui l'acceleratore video può scrivere. Impostare questo parametro su **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Per ogni chiamata a **BeginFrame**, il decodificatore deve effettuare una chiamata corrispondente a [**IDirect3DDXVADevice9:: EndFrame**](idirect3ddxvadevice9-endframe.md).

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

 

 




