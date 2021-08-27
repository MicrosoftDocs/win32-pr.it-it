---
title: Metodo IRDVTaskPluginNotifySink OnTerminated (Sbtsv.h)
description: Chiamato dall'agente attività per richiedere l'arresto dell'agente attività.
ms.assetid: 163e0ce5-f4ee-4242-bdbb-977c5ede3451
ms.tgt_platform: multiple
keywords:
- Metodo OnTerminated Servizi Desktop remoto
- Metodo OnTerminated Servizi Desktop remoto, interfaccia IRDVTaskPluginNotifySink
- Interfaccia IRDVTaskPluginNotifySink Servizi Desktop remoto , metodo OnTerminated
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
ms.openlocfilehash: 29ab2a3e8ddea5999b6d63322dbeb9fca07983e591e849f22a3e98e27c67609a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129133"
---
# <a name="irdvtaskpluginnotifysinkonterminated-method"></a>Metodo IRDVTaskPluginNotifySink::OnTerminated

Chiamato dall'agente attività per richiedere l'arresto dell'agente attività.

## <a name="syntax"></a>Sintassi


```C++
HRESULT OnTerminated(
  [in] HRESULT hr
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*hr* \[ Pollici\]
</dt> <dd>

Indica se l'arresto è dovuto a un arresto normale o a un errore. Se l'arresto è normale, contiene **S \_ OK**. In caso contrario, contiene un **codice di errore HRESULT.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 Enterprise<br/>                                                    |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                  |
| Intestazione<br/>                   | <dl> <dt>Sbtsv.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IRDVTaskPluginNotifySink**](irdvtaskpluginnotifysink.md)
</dt> </dl>

 

 





