---
description: La proprietà di sicurezza dell'oggetto SWbemObjectPath viene utilizzata per ottenere o impostare i componenti di sicurezza di un percorso dell'oggetto.
ms.assetid: 26e5e990-3b78-41b6-83c4-ba0d8b0d2f00
ms.tgt_platform: multiple
title: Proprietà SWbemObjectPath.Security_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Security_
- ISWbemObjectPath.Security_
- ISWbemObjectPath.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 000f3f5e334ef0eba3dbd687d7bdc4b594442305
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226811"
---
# <a name="swbemobjectpathsecurity_-property"></a>Proprietà SWbemObjectPath. Security \_

La proprietà di **sicurezza** dell'oggetto [**SWbemObjectPath**](swbemobjectpath.md) viene utilizzata per ottenere o impostare i componenti di sicurezza di un percorso dell'oggetto. Si noti che non viene usato per impostare gli attributi di sicurezza dell'oggetto **SWbemObjectPath** . Viene utilizzato solo per rappresentare i componenti di sicurezza del percorso di un oggetto [**SWbemLocator**](swbemlocator.md) . Questa proprietà è un oggetto [**SWbemSecurity**](swbemsecurity.md) .

> [!Note]  
> Impostando la proprietà di [**\_ sicurezza**](swbemobject-security-.md) di un oggetto [**SWbemObjectPath**](swbemobjectset.md) su **null** , viene concesso l'accesso illimitato a tutti gli utenti in qualsiasi momento. Per ulteriori informazioni, vedere [**SWbemSecurity**](swbemsecurity.md).

 

Per altre informazioni, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
SWbemObjectPath.Security_ As Object
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
| CLSID<br/>                    | \_SWBEMOBJECTPATH CLSID<br/>                                                       |
| IID<br/>                      | \_ISWBEMOBJECTPATH IID<br/>                                                        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemObjectPath**](swbemobjectpath.md)
</dt> <dt>

[Creazione di un'applicazione o di uno script WMI](creating-a-wmi-application-or-script.md)
</dt> <dt>

[Impostazione della \_ sicurezza del processo dell'applicazione client \_](setting-client-application-process-security.md)
</dt> </dl>

 

 




