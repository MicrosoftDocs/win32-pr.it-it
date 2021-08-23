---
description: La proprietà Security dell'oggetto SWbemObjectPath viene usata per ottenere o impostare i componenti di sicurezza di un percorso oggetto.
ms.assetid: 26e5e990-3b78-41b6-83c4-ba0d8b0d2f00
ms.tgt_platform: multiple
title: SWbemObjectPath.Security_ proprietà (Wbemdisp.h)
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
ms.openlocfilehash: ed473049de6973da077b1ccfabdd3fe752ff4e5edd13f4a49a7c5589309ae81e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639971"
---
# <a name="swbemobjectpathsecurity_-property"></a>Proprietà SWbemObjectPath.Security \_

La **proprietà Security** dell'oggetto [**SWbemObjectPath**](swbemobjectpath.md) viene usata per ottenere o impostare i componenti di sicurezza di un percorso oggetto. Si noti che non viene usato per impostare gli attributi di sicurezza **dell'oggetto SWbemObjectPath** stesso. Viene usato solo per rappresentare i componenti di sicurezza del percorso per un [**oggetto SWbemLocator.**](swbemlocator.md) Questa proprietà è un [**oggetto SWbemSecurity.**](swbemsecurity.md)

> [!Note]  
> [**L'impostazione \_ della**](swbemobject-security-.md) proprietà Security di [**un oggetto SWbemObjectPath**](swbemobjectset.md) su **NULL** concede sempre l'accesso illimitato a tutti gli utenti. Per altre informazioni, vedere [**SWbemSecurity**](swbemsecurity.md).

 

Per altre informazioni, vedere [Convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

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
| Intestazione<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectPath<br/>                                                       |
| IID<br/>                      | IID \_ ISWbemObjectPath<br/>                                                        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemObjectPath**](swbemobjectpath.md)
</dt> <dt>

[Creazione di un'applicazione o di uno script WMI](creating-a-wmi-application-or-script.md)
</dt> <dt>

[Impostazione della sicurezza \_ del processo \_ dell'applicazione client](setting-client-application-process-security.md)
</dt> </dl>

 

 




