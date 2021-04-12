---
description: La proprietà Name di un oggetto SWbemPrivilege è una stringa che descrive in modo univoco un privilegio.
ms.assetid: cc1cdde7-20ad-4ff7-ad49-43eb46c15df9
ms.tgt_platform: multiple
title: Proprietà SWbemPrivilege.Name (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilege.Name
- ISWbemPrivilege.Name
- ISWbemPrivilege.get_Name
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b83ccc7c2757c5d5a0746efd4434db3d108b6992
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233797"
---
# <a name="swbemprivilegename-property"></a>Proprietà SWbemPrivilege.Name

La proprietà **Name** di un oggetto [**SWbemPrivilege**](swbemprivilege.md) è una stringa che descrive in modo univoco un privilegio. Ad esempio, il privilegio che controlla se un utente può eseguire il metodo Shutdown di un oggetto ha la stringa "SeShutdownPrivilege" nella proprietà **SWbemPrivilege.Name** . Questa proprietà è di sola lettura.

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
SWbemPrivilege.Name As 
```



## <a name="property-value"></a>Valore proprietà

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMPRIVILEGE CLSID<br/>                                                        |
| IID<br/>                      | \_ISWBEMPRIVILEGE IID<br/>                                                         |



 

 




