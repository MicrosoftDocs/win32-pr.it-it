---
title: RAS_PARAMETERS struttura (Rassapi.h)
description: La struttura PARAMETRI RAS viene usata dalla funzione RasAdminPortGetInfo per restituire il nome e il valore di un parametro specifico del supporto associato a una porta \_ in un server RAS.
ms.assetid: b46b6176-9a0c-4d9b-b961-b20fdc41653b
keywords:
- RAS_PARAMETERS struttura RAS
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
ms.openlocfilehash: e38ec1a8febbca4319a9c098eafee3705fe59602af81b3ec94e4e974892be771
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909671"
---
# <a name="ras_parameters-structure"></a>Struttura \_ PARAMETERS RAS

\[La **struttura \_ PARAMETRI RAS** non è supportata a Windows Vista.\]

La **struttura \_ PARAMETRI RAS** viene usata dalla funzione [**RasAdminPortGetInfo**](rasadminportgetinfo.md) per restituire il nome e il valore di un parametro specifico del supporto associato a una porta in un server RAS.

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

**Tasto \_ P**
</dt> <dd>

Specifica il nome della chiave che rappresenta il parametro specifico del supporto, ad esempio MAXCONNECTBPS.

</dd> <dt>

**Tipo \_ P**
</dt> <dd>

Identifica il tipo di dati associati al parametro . Questo membro può essere uno dei valori seguenti dell'enumerazione [**RAS \_ PARAMS \_ FORMAT.**](ras-params-format-str.md)



| Valore                                                                                                                                                                                | Significato                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="ParamNumber"></span><span id="paramnumber"></span><span id="PARAMNUMBER"></span><dl> <dt>**ParamNumber**</dt> </dl> | Indica che i dati associati alla chiave sono un numero.<br/> |
| <span id="ParamString"></span><span id="paramstring"></span><span id="PARAMSTRING"></span><dl> <dt>**ParamString**</dt> </dl> | Indica che i dati associati alla chiave sono una stringa.<br/> |



 

</dd> <dt>

**Attributi \_ P**
</dt> <dd>

Riservato.

</dd> <dt>

**Valore \_ P**
</dt> <dd>

Specifica il valore associato al parametro . Questo membro è [**un'unione RAS \_ PARAMS \_ VALUE.**](ras-params-value-str.md) Se il **membro P \_ Type** è ParamNumber, il **membro Number** dell'unione contiene il valore . Se **P \_ Type** è ParamString, il **membro String** dell'unione contiene il valore .

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Rassapi.h</dt> </dl> |



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

 

 





