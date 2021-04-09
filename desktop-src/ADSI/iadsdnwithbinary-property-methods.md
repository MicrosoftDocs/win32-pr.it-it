---
title: Metodi di proprietà IADsDNWithBinary (IADs. h)
description: Il metodo Property dell'interfaccia IADsDNWithBinary imposta la proprietà descritta nella tabella seguente. Per altre informazioni, vedere Metodi della proprietà di interfaccia.
ms.assetid: 3e9ceabb-7a38-4a63-ab62-240ff521e373
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsDNWithBinary ADSI
topic_type:
- apiref
api_name:
- IADsDNWithBinary Property Methods
- IADsDNWithBinary.BinaryValue
- IADsDNWithBinary.get_BinaryValue
- IADsDNWithBinary.put_BinaryValue
- IADsDNWithBinary.DNString
- IADsDNWithBinary.get_DNString
- IADsDNWithBinary.put_DNString
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adf0398a141596de677d7d1739e84ff7525da9a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120750"
---
# <a name="iadsdnwithbinary-property-methods"></a>Metodi di proprietà IADsDNWithBinary

Il metodo Property dell'interfaccia [**IADsDNWithBinary**](/windows/desktop/api/Iads/nn-iads-iadsdnwithbinary) imposta la proprietà descritta nella tabella seguente. Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).

## <a name="properties"></a>Proprietà

<dl> <dt>

**BinaryValue**
</dt> <dd> <dl>

GUID di un oggetto associato a un DN.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_BinaryValue(
  [out] VARIANT* retVal
);
HRESULT put_BinaryValue(
  [in] VARIANT varBV
);
```


</dt> </dl> </dd> <dt>

**DNString**
</dt> <dd> <dl>

Stringa DN associata al GUID di un oggetto.

<dt>

Tipo di accesso: lettura/scrittura
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


</dt> </dl> </dd> </dl>

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>IADs. h</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsDNWithBinary è definito come 7E99C0A2-F935-11D2-BA96-00C04FB6D0D1<br/>     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IADsDNWithBinary**](/windows/desktop/api/Iads/nn-iads-iadsdnwithbinary)
</dt> <dt>

[**\_DN Ads \_ con \_ binario**](/windows/win32/api/iads/ns-iads-ads_dn_with_binary)
</dt> </dl>

 

 





