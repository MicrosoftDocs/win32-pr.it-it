---
description: La proprietà CIMType dell'oggetto SWbemProperty è un numero intero che può essere usato per determinare il tipo CIM di questa proprietà. Questa proprietà è di sola lettura.
ms.assetid: fb570ba4-6ce3-4131-8088-2761110033ba
ms.tgt_platform: multiple
title: Proprietà SWbemProperty.CIMType (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty.CIMType
- ISWbemProperty.CIMType
- ISWbemProperty.get_CIMType
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9f3b92cca8d17af8814a7891d0d4f97c7e003b1a999a42c63b6abe59d50e8ac9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991931"
---
# <a name="swbempropertycimtype-property"></a>Proprietà SWbemProperty.CIMType

La **proprietà CIMType** dell'oggetto [**SWbemProperty**](swbemproperty.md) è un numero intero che può essere usato per determinare il tipo CIM di questa proprietà. Questa proprietà è di sola lettura.

Per una spiegazione di questa sintassi, vedere [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
SWbemProperty.CIMType As Integer
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

Per altre informazioni sui tipi validi per questa proprietà, vedere [**WbemCimtypeEnum.**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum)

Le istanze di oggetti incorporati vengono archiviate in oggetti compositi come proprietà di tipo **CIM \_ OBJECT.** Per determinare la classe di un oggetto incorporato in un'istanza di una classe composita, è necessario esaminare il qualificatore **CIMType** della proprietà del tipo **CIM \_ OBJECT.**

I riferimenti agli oggetti in una classe di associazione vengono archiviati in proprietà di tipo **CIM \_ REFERENCE.** Per determinare i percorsi effettivi degli oggetti, è necessario esaminare il **qualificatore CIMType** della **proprietà del tipo \_ CIM REFERENCE.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemProperty<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemProperty<br/>                                                          |



 

 




