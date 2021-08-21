---
title: Metodi della proprietà IADsTimestamp (Iads.h)
description: Il metodo di proprietà dell'interfaccia IADsTimestamp imposta la proprietà descritta nella tabella seguente. Per altre informazioni, vedere Metodi delle proprietà dell'interfaccia.
ms.assetid: 0f00d270-3c11-4c60-95b3-178130e31caa
ms.tgt_platform: multiple
keywords:
- Metodi della proprietà IADsTimestamp ADSI
topic_type:
- apiref
api_name:
- IADsTimestamp Property Methods
- IADsTimestamp.WholeSeconds
- IADsTimestamp.get_WholeSeconds
- IADsTimestamp.put_WholeSeconds
- IADsTimestamp.EventID
- IADsTimestamp.get_EventID
- IADsTimestamp.put_EventID
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a105a2ba246c38b7cf6c5bdd1c7420096397e294bb29d5bed446b31d3ca9763
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118427568"
---
# <a name="iadstimestamp-property-methods"></a>Metodi della proprietà IADsTimestamp

Il metodo di proprietà [**dell'interfaccia IADsTimestamp**](/windows/desktop/api/Iads/nn-iads-iadstimestamp) imposta la proprietà descritta nella tabella seguente. Per altre informazioni, vedere [Metodi delle proprietà dell'interfaccia](interface-property-methods.md).

## <a name="properties"></a>Proprietà

<dl> <dt>

**EventID**
</dt> <dd> <dl>

Identificatore dell'evento.

<dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Tipo di dati scripting: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_EventID(
  [out] LONG* retval
);
HRESULT put_EventID(
  [in] LONG lnEventID
);
```


</dt> </dl> </dd> <dt>

**WholeSeconds**
</dt> <dd> <dl>

Numero di secondi con valore zero pari a 12:00 AM, gennaio 1970, UTC.

<dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Tipo di dati scripting: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_WholeSeconds(
  [out] LONG* retVal
);
HRESULT put_WholeSeconds(
  [in] LONG lnWholeSeconds
);
```


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Iads.h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | \_IADsTimestamp IID è definito come B2F5A901-4080-11D1-A3AC-00C04FB950DC<br/>        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IADsTimestamp**](/windows/desktop/api/Iads/nn-iads-iadstimestamp)
</dt> <dt>

[**TIMESTAMP DI ADS \_**](/windows/win32/api/iads/ns-iads-ads_timestamp)
</dt> </dl>

 

 





