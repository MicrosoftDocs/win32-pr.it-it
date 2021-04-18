---
description: La \_ proprietà di sicurezza dell'oggetto SWbemObjectSet viene utilizzata per ottenere o impostare le impostazioni di sicurezza per un oggetto SWbemObjectSet. Questa proprietà è un oggetto SWbemSecurity.
ms.assetid: ee2ad6d5-c0aa-4510-ba1b-4a152d56011f
ms.tgt_platform: multiple
title: Proprietà SWbemObjectSet.Security_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.Security_
- ISWbemObjectSet.Security_
- ISWbemObjectSet.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 690c5c23a40ed3333468beeeab8ccc1f8c9a6ad2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309798"
---
# <a name="swbemobjectsetsecurity_-property"></a>Proprietà SWbemObjectSet. Security \_

La proprietà di **\_ sicurezza** dell'oggetto [**SWbemObjectSet**](swbemobjectset.md) viene utilizzata per ottenere o impostare le impostazioni di sicurezza per un oggetto **SWbemObjectSet** . Questa proprietà è un oggetto [**SWbemSecurity**](swbemsecurity.md) .

> [!Note]  
> Impostando la proprietà di [**\_ sicurezza**](swbemobject-security-.md) di un oggetto [**SWbemObjectSet**](swbemobjectset.md) su **null** , viene concesso l'accesso illimitato a tutti gli utenti in qualsiasi momento. Per ulteriori informazioni sulle implicazioni dell'accesso illimitato, vedere [**SWbemSecurity**](swbemsecurity.md).

 

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
SWbemObjectSet.Security_ As Object
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
| CLSID<br/>                    | \_SWBEMOBJECTSET CLSID<br/>                                                        |
| IID<br/>                      | \_ISWBEMOBJECTSET IID<br/>                                                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemObjectSet**](swbemobjectset.md)
</dt> <dt>

[Creazione di un'applicazione o di uno script WMI](creating-a-wmi-application-or-script.md)
</dt> <dt>

[Protezione dei client di scripting](securing-scripting-clients.md)
</dt> </dl>

 

 




