---
title: Struttura RAS_PARAMETERS (rassapi. h)
description: La \_ struttura dei parametri RAS viene utilizzata dalla funzione RasAdminPortGetInfo per restituire il nome e il valore di un parametro specifico del supporto associato a una porta su un server RAS.
ms.assetid: b46b6176-9a0c-4d9b-b961-b20fdc41653b
keywords:
- RAS struttura RAS_PARAMETERS
topic_type:
- apiref
api_name:
- RAS_PARAMETERS
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fffaefa8a6f2cffb895cc18882ed8fc0c382a4bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518520"
---
# <a name="ras_parameters-structure"></a>\_Struttura dei parametri RAS

\[La struttura dei **\_ parametri RAS** non è supportata a partire da Windows Vista.\]

La struttura dei **\_ parametri RAS** viene utilizzata dalla funzione [**RasAdminPortGetInfo**](rasadminportgetinfo.md) per restituire il nome e il valore di un parametro specifico del supporto associato a una porta su un server RAS.

## <a name="syntax"></a>Sintassi


```C++
typedef struct RAS_PARAMETERS {
  CHAR              P_Key[RASSAPI_MAX_PARAM_KEY_SIZE];
  RAS_PARAMS_FORMAT P_Type;
  BYTE              P_Attributes;
  RAS_PARAMS_VALUE  P_Value;
} RAS_PARAMETERS;
```



## <a name="members"></a>Members

<dl> <dt>

**\_Tasto P**
</dt> <dd>

Specifica il nome della chiave che rappresenta il parametro specifico del supporto, ad esempio MAXCONNECTBPS.

</dd> <dt>

**\_Tipo P**
</dt> <dd>

Identifica il tipo di dati associato al parametro. Questo membro può essere uno dei valori seguenti dall'enumerazione del [**\_ \_ formato RAS params**](ras-params-format-str.md) .



| Valore                                                                                                                                                                                | Significato                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="ParamNumber"></span><span id="paramnumber"></span><span id="PARAMNUMBER"></span><dl> <dt>**ParamNumber**</dt> </dl> | Indica che i dati associati alla chiave sono numerici.<br/> |
| <span id="ParamString"></span><span id="paramstring"></span><span id="PARAMSTRING"></span><dl> <dt>**ParamString**</dt> </dl> | Indica che i dati associati alla chiave sono una stringa.<br/> |



 

</dd> <dt>

**\_Attributi P**
</dt> <dd>

Riservato.

</dd> <dt>

**\_Valore P**
</dt> <dd>

Specifica il valore associato al parametro. Questo membro è un'Unione del [**\_ \_ valore params RAS**](ras-params-value-str.md) . Se il membro di **\_ tipo P** è ParamNumber, il membro **Number** dell'Unione contiene il valore. Se **P \_ Type** è ParamString, il membro di **stringa** dell'Unione contiene il valore.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Rassapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica del servizio di accesso remoto (RAS)](about-remote-access-service.md)
</dt> <dt>

[Strutture di amministrazione del server RAS](ras-server-administration-structures.md)
</dt> <dt>

[**RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md)
</dt> <dt>

[**RasAdminConnectionHangupNotification**](rasadminconnectionhangupnotification.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

 





