---
description: La proprietà Security dell'oggetto SWbemLocator viene usata per leggere o impostare le impostazioni di sicurezza per \_ un oggetto SWbemLocator. Questa proprietà è un oggetto SWbemSecurity.
ms.assetid: 75987bef-21ae-4420-b069-afab90499218
ms.tgt_platform: multiple
title: SWbemLocator.Security_ proprietà (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLocator.Security_
- ISWbemLocator.Security_
- ISWbemLocator.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6c5fa2ba102de1135c0019e2dcfb291f55672cabb00cea1c59d8a655f21c882e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955171"
---
# <a name="swbemlocatorsecurity_-property"></a>Proprietà SWbemLocator.Security \_

La **\_ proprietà Security** dell'oggetto [**SWbemLocator**](swbemlocator.md) viene usata per leggere o impostare le impostazioni di sicurezza per un **oggetto SWbemLocator.** Questa proprietà è un [**oggetto SWbemSecurity.**](swbemsecurity.md)

> [!Note]  
> **L'impostazione \_ della** proprietà Security di [**un oggetto SWbemLocator**](swbemlocator.md) su **NULL** concede sempre l'accesso illimitato a tutti gli utenti. Per altre informazioni, vedere [**SWbemSecurity**](swbemsecurity.md).

 

Per una spiegazione di questa sintassi, vedere [Convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
SWbemLocator.Security_ As Object
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

Le proprietà di un **oggetto SWbemLocator.Security \_** non hanno valori predefiniti. Se si tenta di ottenere il valore [**di SWbemSecurity.AuthenticationLevel**](swbemsecurity-authenticationlevel.md) o [**SWbemSecurity.ImpersonationLevel**](swbemsecurity-impersonationlevel.md) in un [**oggetto SWbemLocator**](swbemlocator.md) prima di impostarlo, viene restituito un errore [wbemErrFailed.](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemLocator<br/>                                                          |
| IID<br/>                      | IID \_ ISWbemLocator<br/>                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemLocator**](swbemlocator.md)
</dt> <dt>

[Creazione di un'applicazione o di uno script WMI](creating-a-wmi-application-or-script.md)
</dt> <dt>

[Esecuzione di operazioni con privilegi tramite VBScript](executing-privileged-operations-using-vbscript.md)
</dt> <dt>

[Impostazione della sicurezza \_ del processo \_ dell'applicazione client](setting-client-application-process-security.md)
</dt> <dt>

[**Oggetto SWbemSecurity**](swbemsecurity.md)
</dt> <dt>

[Protezione di una connessione WMI remota](securing-a-remote-wmi-connection.md)
</dt> </dl>

 

 




