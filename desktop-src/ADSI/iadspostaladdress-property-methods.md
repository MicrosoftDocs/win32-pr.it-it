---
title: Metodi della proprietà IADsPostalAddress (Iads.h)
description: Il metodo di proprietà dell'interfaccia IADsPostalAddress imposta la proprietà descritta nella tabella seguente. Per altre informazioni, vedere Metodi delle proprietà dell'interfaccia.
ms.assetid: f7e61c69-f3a6-4ca6-a276-3cd859252571
ms.tgt_platform: multiple
keywords:
- Metodi della proprietà IADsPostalAddress ADSI
topic_type:
- apiref
api_name:
- IADsPostalAddress Property Methods
- IADsPostalAddress.PostalAddress
- IADsPostalAddress.get_PostalAddress
- IADsPostalAddress.put_PostalAddress
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd01887751a4389984a4bc765d924d6c8a8e81dd9a65be3b7a868a3cbb845cf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118691128"
---
# <a name="iadspostaladdress-property-methods"></a>Metodi della proprietà IADsPostalAddress

Il metodo di proprietà [**dell'interfaccia IADsPostalAddress**](/windows/desktop/api/Iads/nn-iads-iadspostaladdress) imposta la proprietà descritta nella tabella seguente. Per altre informazioni, vedere [Metodi delle proprietà dell'interfaccia](interface-property-methods.md).

## <a name="properties"></a>Proprietà

<dl> <dt>

**PostalAddress**
</dt> <dd> <dl>

Matrice di sei stringhe che contiene l'indirizzo postale dell'utente.

<dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Tipo di dati scripting: **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PostalAddress(
  [out] VARIANT* retVal
);
HRESULT put_PostalAddress(
  [in] VARIANT vPostalAddress
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
| IID<br/>                      | IADsPostalAddress IID è definito come \_ 7ADECF29-4680-11D1-A3B4-00C04FB950DC<br/>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IADsPostalAddress**](/windows/desktop/api/Iads/nn-iads-iadspostaladdress)
</dt> <dt>

[**ADS \_ POSTALADDRESS**](/windows/win32/api/iads/ns-iads-ads_postaladdress)
</dt> </dl>

 

 





