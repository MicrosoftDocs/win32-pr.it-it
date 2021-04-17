---
title: Metodi di proprietà IADsTimestamp (IADs. h)
description: Il metodo Property dell'interfaccia IADsTimestamp imposta la proprietà descritta nella tabella seguente. Per altre informazioni, vedere Metodi della proprietà di interfaccia.
ms.assetid: 0f00d270-3c11-4c60-95b3-178130e31caa
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsTimestamp ADSI
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
ms.openlocfilehash: a77db7a6a3b3814cd10beca5da5e3166ab1b61a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476348"
---
# <a name="iadstimestamp-property-methods"></a>Metodi di proprietà IADsTimestamp

Il metodo Property dell'interfaccia [**IADsTimestamp**](/windows/desktop/api/Iads/nn-iads-iadstimestamp) imposta la proprietà descritta nella tabella seguente. Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).

## <a name="properties"></a>Proprietà

<dl> <dt>

**EventID**
</dt> <dd> <dl>

Identificatore dell'evento.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Long**
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

Numero di secondi con valore zero 12:00 AM, gennaio 1970, UTC.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Long**
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
| Intestazione<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsTimestamp è definito come B2F5A901-4080-11D1-A3AC-00C04FB950DC<br/>        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IADsTimestamp**](/windows/desktop/api/Iads/nn-iads-iadstimestamp)
</dt> <dt>

[**\_timestamp ADS**](/windows/win32/api/iads/ns-iads-ads_timestamp)
</dt> </dl>

 

 





