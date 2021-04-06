---
title: Metodi di proprietà IADsNetAddress (IADs. h)
description: Il metodo Property dell'interfaccia IADsNetAddress imposta la proprietà descritta nella tabella seguente. Per altre informazioni, vedere Metodi della proprietà di interfaccia.
ms.assetid: 1da493d6-5660-4054-8d28-89db0b56f30f
ms.tgt_platform: multiple
keywords:
- Metodi di proprietà IADsNetAddress ADSI
topic_type:
- apiref
api_name:
- IADsNetAddress Property Methods
- IADsNetAddress.AddressType
- IADsNetAddress.get_AddressType
- IADsNetAddress.put_AddressType
- IADsNetAddress.Address
- IADsNetAddress.get_Address
- IADsNetAddress.put_Address
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 073033c703db8eaa55b05058d6d2bbc3d3167f4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742690"
---
# <a name="iadsnetaddress-property-methods"></a>Metodi di proprietà IADsNetAddress

Il metodo Property dell'interfaccia [**IADsNetAddress**](/windows/desktop/api/Iads/nn-iads-iadsnetaddress) imposta la proprietà descritta nella tabella seguente. Per altre informazioni, vedere [metodi della proprietà di interfaccia](interface-property-methods.md).

## <a name="properties"></a>Proprietà

<dl> <dt>

**Indirizzo**
</dt> <dd> <dl>

Un indirizzo di rete.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Variant**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_Address(
  [out] VARIANT* retval
);
HRESULT put_Address(
  [in] VARIANT vAddress
);
```


</dt> </dl> </dd> <dt>

**AddressType**
</dt> <dd> <dl>

Tipo di protocolli di comunicazione.

<dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Tipo di dati di scripting: **Long**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AddressType(
  [out] LONG* retVal
);
HRESULT put_AddressType(
  [in] LONG lnAddressType
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
| IID<br/>                      | IID \_ IADsNetAddress è definito come B21A50A9-4080-11D1-A3AC-00C04FB950DC<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IADsNetAddress**](/windows/desktop/api/Iads/nn-iads-iadsnetaddress)
</dt> <dt>

[**\_Netaddress ADS**](/windows/win32/api/iads/ns-iads-ads_netaddress)
</dt> </dl>

 

 





