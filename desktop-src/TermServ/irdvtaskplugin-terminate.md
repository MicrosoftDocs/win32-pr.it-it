---
title: Metodo Terminate IRDVTaskPlugin
description: Chiamato quando l'agente attività viene arrestato.
ms.assetid: b693a318-1da7-4207-8046-a62b7ccca471
ms.tgt_platform: multiple
keywords:
- Termina metodo Servizi Desktop remoto
- Metodo Terminate Servizi Desktop remoto, interfaccia IRDVTaskPlugin
- Metodo Terminate dell'interfaccia IRDVTaskPlugin Servizi Desktop remoto ,
topic_type:
- apiref
api_name:
- IRDVTaskPlugin.Terminate
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0ccfcb1a59f0db6d29881d139d16bd08308a40df2c1233beab66b0b4814caa84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129268"
---
# <a name="irdvtaskpluginterminate-method"></a>Metodo IRDVTaskPlugin::Terminate

Chiamato quando l'agente attività viene arrestato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Terminate(
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
|-------------------------------------|-----------------------------------|
| Client minimo supportato<br/> | Windows 7 Enterprise<br/>   |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IRDVTaskPlugin**](irdvtaskplugin.md)
</dt> </dl>

 

 





