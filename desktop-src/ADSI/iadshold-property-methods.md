---
title: Metodi di proprietà IADsHold (IADs. h)
description: Il metodo Property dell'interfaccia IADsHold imposta la proprietà descritta nella tabella seguente. Per altre informazioni, vedere Metodi della proprietà di interfaccia.
ms.assetid: 55968bc1-c44a-4db4-acc8-e1b6f1e4ad4c
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsHold ADSI
topic_type:
- apiref
api_name:
- IADsHold Property Methods
- IADsHold.ObjectName
- IADsHold.get_ObjectName
- IADsHold.put_ObjectName
- IADsHold.Amount
- IADsHold.get_Amount
- IADsHold.put_Amount
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cae2499efb461e6c13397fdaef75e515f0a1a21a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120742"
---
# <a name="iadshold-property-methods"></a>Metodi di proprietà IADsHold

Il metodo Property dell'interfaccia [**IADsHold**](/windows/desktop/api/Iads/nn-iads-iadshold) imposta la proprietà descritta nella tabella seguente. Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).

## <a name="properties"></a>Proprietà

<dl> <dt>

**Amount**
</dt> <dd> <dl>

Importo degli addebiti addebitati all'utente per il periodo di attesa mentre il server verifica il saldo dell'account dell'utente.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Amount(
  [out] LONG* retval
);
HRESULT put_Amount(
  [in] LONG lnAmount
);
```


</dt> </dl> </dd> <dt>

**ObjectName**
</dt> <dd> <dl>

Nome dell'oggetto che rappresenta un utente in attesa.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_ObjectName(
  [out] BSTR* retVal
);
HRESULT put_ObjectName(
  [in] BSTR bstrObjectName
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
| IID<br/>                      | IID \_ IADsHold è definito come B3EB3B37-4080-11D1-A3AC-00C04FB950DC<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IADsHold**](/windows/desktop/api/Iads/nn-iads-iadshold)
</dt> </dl>

 

 





