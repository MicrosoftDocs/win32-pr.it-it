---
title: Metodo onterminated IRDVTaskPluginNotifySink (Sbtsv. h)
description: Chiamato dall'agente attività per richiedere l'arresto dell'agente attività.
ms.assetid: 163e0ce5-f4ee-4242-bdbb-977c5ede3451
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto metodo onterminated
- Servizi Desktop remoto metodo onterminated, interfaccia IRDVTaskPluginNotifySink
- Interfaccia IRDVTaskPluginNotifySink Servizi Desktop remoto, metodo onterminated
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink.OnTerminated
api_location:
- sbtsv.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b261437425b0b4dce4b2c2e17c52b6e24ea3e0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518934"
---
# <a name="irdvtaskpluginnotifysinkonterminated-method"></a>Metodo IRDVTaskPluginNotifySink:: onTerminate

Chiamato dall'agente attività per richiedere l'arresto dell'agente attività.

## <a name="syntax"></a>Sintassi


```C++
HRESULT OnTerminated(
  [in] HRESULT hr
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*risorse umane* \[ in\]
</dt> <dd>

Indica se l'arresto è dovuto a un arresto normale o a un errore. Se l'arresto è normale, questo contiene **S \_ OK**. In caso contrario, contiene un codice di errore **HRESULT** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 Enterprise<br/>                                                    |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                  |
| Intestazione<br/>                   | <dl> <dt>Sbtsv. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

 





