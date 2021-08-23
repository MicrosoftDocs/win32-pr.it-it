---
title: Metodi della proprietà IADsCaseIgnoreList (Iads.h)
description: Il metodo di proprietà dell'interfaccia IADsCaseIgnoreList imposta la proprietà descritta nella tabella seguente. Per altre informazioni, vedere Metodi delle proprietà dell'interfaccia.
ms.assetid: 4f73adbf-abe3-4552-a3e4-19cff22e0ad0
ms.tgt_platform: multiple
keywords:
- Metodi della proprietà IADsCaseIgnoreList ADSI
topic_type:
- apiref
api_name:
- IADsCaseIgnoreList Property Methods
- IADsCaseIgnoreList.CaseIgnoreList
- IADsCaseIgnoreList.get_CaseIgnoreList
- IADsCaseIgnoreList.put_CaseIgnoreList
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84e2f07d3c4afa6cd55f6a757ccae6f2d1076b954e0afdd0c82c8a5247af33f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118961920"
---
# <a name="iadscaseignorelist-property-methods"></a>Metodi della proprietà IADsCaseIgnoreList

Il metodo di proprietà [**dell'interfaccia IADsCaseIgnoreList**](/windows/desktop/api/Iads/nn-iads-iadscaseignorelist) imposta la proprietà descritta nella tabella seguente. Per altre informazioni, vedere [Metodi delle proprietà dell'interfaccia](interface-property-methods.md).

## <a name="properties"></a>Proprietà

<dl> <dt>

**CaseIgnoreList**
</dt> <dd> <dl>

Sequenza ordinata di stringhe senza distinzione tra maiuscole e minuscole.

<dt>

Tipo di accesso: Lettura/Scrittura
</dt> <dt>

Tipo di dati scripting: **VARIANT**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_CaseIgnoreList(
  [out] VARIANT* retVal
);
HRESULT put_CaseIgnoreList(
  [in] VARIANT vCaseIgnoreList
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
| IID<br/>                      | \_IADsCaseIgnoreList IID è definito come 7B66B533-4680-11D1-A3B4-00C04FB950DC<br/>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IADsCaseIgnoreList**](/windows/desktop/api/Iads/nn-iads-iadscaseignorelist)
</dt> <dt>

[**ELENCO DI \_ CASEIGNORE DI ADS \_**](/windows/desktop/api/Iads/ns-iads-ads_caseignore_list)
</dt> </dl>

 

 





