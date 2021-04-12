---
description: Termina l'elaborazione per creare un'immagine decodificata.
ms.assetid: 4b47cd53-6ce0-47b0-83ed-84926e92430f
title: 'Metodo IDirect3DDXVADevice9:: EndFrame (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.EndFrame
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: a6a737fe6c4c3020b7ebfe7fee98281e6c83f168
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130343"
---
# <a name="idirect3ddxvadevice9endframe-method"></a>Metodo IDirect3DDXVADevice9:: EndFrame

Termina l'elaborazione per creare un'immagine decodificata.

## <a name="syntax"></a>Sintassi


```C++
HRESULT EndFrame(
   DWORD SizeMiscData,
   VOID  *pMiscData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SizeMiscData* 
</dt> <dd>

Dimensioni del buffer specificato da *pMiscData*, in byte. Il valore deve essere 2.

</dd> <dt>

*pMiscData* 
</dt> <dd>

Puntatore a un buffer che contiene i dati per il tasto di scelta rapida del video. Questo buffer deve contenere lo stesso indice frame passato al metodo [**IDirect3DDXVADevice9:: BeginFrame**](idirect3ddxvadevice9-beginframe.md) nel parametro *pInputData* .

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

 

 




