---
description: L'oggetto SWbemPrivilege rappresenta un singolo privilegio. Questo oggetto non può essere creato dalla chiamata CreateObject di VBScript.
ms.assetid: 18ee4587-6347-4075-b5e9-c5fb02f3cbf7
ms.tgt_platform: multiple
title: Oggetto SWbemPrivilege (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilege
- ISWbemPrivilege
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c3be448b4088011cd4d628a7d98b448af550b010
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058264"
---
# <a name="swbemprivilege-object"></a>Oggetto SWbemPrivilege

L'oggetto **SWbemPrivilege** rappresenta un singolo privilegio. Questo oggetto non può essere creato dalla chiamata **CreateObject** di VBScript.

## <a name="members"></a>Membri

L'oggetto **SWbemPrivilege** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **SWbemPrivilege** dispone di queste proprietà.



| Proprietà                                                     | Tipo di accesso           | Descrizione                                                                      |
|:-------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------|
| [**DisplayName**](swbemprivilege-displayname.md)<br/> | Sola lettura<br/>  | Nome visualizzato del privilegio.<br/>                                       |
| [**Identificatore**](swbemprivilege-identifier.md)<br/>   | Lettura/Scrittura<br/> | Integer che rappresenta il privilegio da impostare o recuperare.<br/> |
| [**IsEnabled**](swbemprivilege-isenabled.md)<br/>     | Lettura/Scrittura<br/> | Valore booleano che indica se questo privilegio è abilitato.<br/>            |
| [**Nome**](swbemprivilege-name.md)<br/>               | Sola lettura<br/>  | Nome del privilegio.<br/>                                               |



 

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



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Esecuzione di operazioni con privilegi](executing-privileged-operations.md)
</dt> <dt>

[Oggetti API di scripting](scripting-api-objects.md)
</dt> </dl>

 

 




