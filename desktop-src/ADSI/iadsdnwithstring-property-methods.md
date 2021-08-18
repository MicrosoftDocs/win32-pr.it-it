---
title: Metodi della proprietà IADsDNWithString (Iads.h)
description: Il metodo di proprietà dell'interfaccia IADsDNWithString imposta la proprietà descritta nella tabella seguente. Per altre informazioni, vedere Metodi delle proprietà di interfaccia.
ms.assetid: d3fb67b6-9f7d-4de5-bf01-f9c5b9e4f086
ms.tgt_platform: multiple
keywords:
- Metodi della proprietà IADsDNWithString ADSI
topic_type:
- apiref
api_name:
- IADsDNWithString Property Methods
- IADsDNWithString.StringValue
- IADsDNWithString.get_StringValue
- IADsDNWithString.put_StringValue
- IADsDNWithString.DNString
- IADsDNWithString.get_DNString
- IADsDNWithString.put_DNString
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51082f31aa9e456ded5498a4711d3ddcfe3c03241235aa14c39920071b110e35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082505"
---
# <a name="iadsdnwithstring-property-methods"></a>Metodi della proprietà IADsDNWithString

Il metodo di proprietà [**dell'interfaccia IADsDNWithString**](/windows/desktop/api/Iads/nn-iads-iadsdnwithstring) imposta la proprietà descritta nella tabella seguente. Per altre informazioni, vedere [Metodi delle proprietà di interfaccia.](interface-property-methods.md)

## <a name="properties"></a>Proprietà

<dl> <dt>

**DNString**
</dt> <dd> <dl>

Stringa DN associata a un valore stringa.

<dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_DNString(
  [out] BSTR* retval
);
HRESULT put_DNString(
  [in] BSTR bstrDN
);
```


</dt> </dl> </dd> <dt>

**StringValue**
</dt> <dd> <dl>

Valore stringa associato a un DN di un oggetto.

<dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **BSTR**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_StringValue(
  [out] BSTR* retVal
);
HRESULT put_StringValue(
  [in] BSTR varBV
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
| IID<br/>                      | IID \_ IADsDNWithString è definito come 370DF02E-F934-11D2-BA96-00C04FB6D0D1<br/>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IADsDNWithString**](/windows/desktop/api/Iads/nn-iads-iadsdnwithstring)
</dt> <dt>

[**ADS \_ DN \_ WITH \_ STRING**](/windows/win32/api/iads/ns-iads-ads_dn_with_string)
</dt> </dl>

 

 





