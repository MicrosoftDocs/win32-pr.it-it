---
description: La proprietà CIMType dell'oggetto SWbemProperty è un numero intero che può essere utilizzato per determinare il tipo CIM di questa proprietà. Questa proprietà è di sola lettura.
ms.assetid: fb570ba4-6ce3-4131-8088-2761110033ba
ms.tgt_platform: multiple
title: Proprietà SWbemProperty. CIMType (wbemdisp. h)
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
ms.openlocfilehash: 416101df1c3ae8542d3d2cd170b873407f007c67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967656"
---
# <a name="swbempropertycimtype-property"></a>Proprietà SWbemProperty. CIMType

La proprietà **CimType** dell'oggetto [**SWbemProperty**](swbemproperty.md) è un numero intero che può essere utilizzato per determinare il tipo CIM di questa proprietà. Questa proprietà è di sola lettura.

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
SWbemProperty.CIMType As Integer
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

Per ulteriori informazioni sui tipi validi per questa proprietà, vedere [**WbemCimtypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum).

Le istanze di oggetti incorporati vengono archiviate in oggetti compositi come proprietà di tipo **\_ oggetto CIM**. Per determinare la classe di un oggetto incorporato in un'istanza di una classe composita, è necessario esaminare il qualificatore **CimType** della proprietà del tipo di **\_ oggetto CIM** .

I riferimenti a oggetti in una classe Association sono archiviati in proprietà di tipo **CIM \_ Reference**. Per determinare i percorsi degli oggetti effettivi è necessario esaminare il qualificatore **CimType** della proprietà del tipo di **\_ riferimento CIM** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMPROPERTY CLSID<br/>                                                         |
| IID<br/>                      | \_ISWBEMPROPERTY IID<br/>                                                          |



 

 




