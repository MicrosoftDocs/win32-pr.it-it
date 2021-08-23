---
title: Metodi della proprietà IADsOctetList (Iads.h)
description: Il metodo di proprietà dell'interfaccia IADsOctetList imposta la proprietà descritta nella tabella seguente. Per altre informazioni, vedere Metodi delle proprietà dell'interfaccia.
ms.assetid: 6fe29a0d-dd53-4cc2-8152-22a0a2756c2c
ms.tgt_platform: multiple
keywords:
- Metodi della proprietà IADsOctetList ADSI
topic_type:
- apiref
api_name:
- IADsOctetList Property Methods
- IADsOctetList.OctetList
- IADsOctetList.get_OctetList
- IADsOctetList.put_OctetList
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fa434eaf9cde95adb4b43d0261ac779d5183d9f3de2284704bc75cfa564521e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023439"
---
# <a name="iadsoctetlist-property-methods"></a>Metodi della proprietà IADsOctetList

Il metodo di proprietà [**dell'interfaccia IADsOctetList**](/windows/desktop/api/Iads/nn-iads-iadsoctetlist) imposta la proprietà descritta nella tabella seguente. Per altre informazioni, vedere [Metodi delle proprietà dell'interfaccia](interface-property-methods.md).

## <a name="properties"></a>Proprietà

<dl> <dt>

**OctetList**
</dt> <dd> <dl>

Sequenza ordinata di matrici di byte.

<dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Tipo di dati scripting: **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_OctetList(
  [out] VARIANT* retVal
);
HRESULT put_OctetList(
  [in] VARIANT vOctetList
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
| IID<br/>                      | IADsOctetList IID è definito come \_ 7B28B80F-4680-11D1-A3B4-00C04FB950DC<br/>        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IADsOctetList**](/windows/desktop/api/Iads/nn-iads-iadsoctetlist)
</dt> <dt>

[**ELENCO \_ OTTETTI DI ADS \_**](/windows/desktop/api/Iads/ns-iads-ads_octet_list)
</dt> </dl>

 

 





