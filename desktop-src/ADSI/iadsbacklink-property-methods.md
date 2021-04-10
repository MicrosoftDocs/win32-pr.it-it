---
title: Metodi di proprietà IADsBackLink (IADs. h)
description: Il metodo Property dell'interfaccia IADsBackLink imposta la proprietà descritta nella tabella seguente. Per altre informazioni, vedere Metodi della proprietà di interfaccia.
ms.assetid: 0a66fa6d-1bf5-4ff0-8bbd-625a69cf9594
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsBackLink ADSI
topic_type:
- apiref
api_name:
- IADsBackLink Property Methods
- IADsBackLink.RemoteID
- IADsBackLink.get_RemoteID
- IADsBackLink.put_RemoteID
- IADsBackLink.ObjectName
- IADsBackLink.get_ObjectName
- IADsBackLink.put_ObjectName
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c2220fff3a18b0822c0167b387ec10c324d95aa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120755"
---
# <a name="iadsbacklink-property-methods"></a>Metodi di proprietà IADsBackLink

Il metodo Property dell'interfaccia [**IADsBackLink**](/windows/desktop/api/Iads/nn-iads-iadsbacklink) imposta la proprietà descritta nella tabella seguente. Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).

## <a name="properties"></a>Proprietà

<dl> <dt>

**ObjectName**
</dt> <dd> <dl>

Nome di un oggetto a cui è associato l'attributo **back link** .

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ObjectName(
  [out] BSTR* retval
);
HRESULT put_ObjectName(
  [in] BSTR bstrSubjectName
);
```


</dt> </dl> </dd> <dt>

**RemoteID**
</dt> <dd> <dl>

Identificatore del server remoto che richiede un riferimento esterno all'oggetto specificato da **ObjectName**.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_RemoteID(
  [out] LONG* retVal
);
HRESULT put_RemoteID(
  [in] LONG bstrProtectedAttrName
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
| IID<br/>                      | IID \_ IADsBackLink è definito come FD1302BD-4080-11D1-A3AC-00C04FB950DC<br/>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IADsBackLink**](/windows/desktop/api/Iads/nn-iads-iadsbacklink)
</dt> <dt>

[**\_BACKLINK annunci**](/windows/win32/api/iads/ns-iads-ads_backlink)
</dt> </dl>

 

 





