---
title: Classe Win32_RDMSEnvironment
description: Gestisce un ambiente Desktop remoto Management Services (RDBMS).
ms.assetid: 8a3b10c1-d01d-4e52-8915-29159cc406cc
ms.tgt_platform: multiple
keywords:
- Classe Win32_RDMSEnvironment Servizi Desktop remoto
- Classe Win32_RDMSEnvironment Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a78acb964471844be74481d1ddfa2d4cf56a173
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301449"
---
# <a name="win32_rdmsenvironment-class"></a>Win32 \_ RDMSEnvironment (classe)

Gestisce un ambiente Desktop remoto Management Services (RDBMS).

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSEnvironment
{
};
```

## <a name="members"></a>Members

La classe **Win32 \_ RDMSEnvironment** presenta questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

La classe **Win32 \_ RDMSEnvironment** presenta questi metodi.



| Metodo                                                                   | Descrizione                                                                                          |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**GetActiveServer**](getactiveserver-win32-rdmsenvironment.md)         | Recupera il nome di dominio completo (FQDN) dell'ambiente RDBMS.<br/>                 |
| [**GetClientAccessName**](getclientaccessname-win32-rdmsenvironment.md) | Recupera il nome del record di risorse (DNS) di Domain Name System (RR) dell'ambiente RDBMS.<br/> |
| [**SetActiveServer**](setactiveserver-win32-rdmsenvironment.md)         | Imposta il nome di dominio completo dell'ambiente RDBMS sul nodo corrente.<br/>                                |
| [**SetClientAccessName**](setclientaccessname-win32-rdmsenvironment.md) | Aggiorna il nome RR DNS dell'ambiente RDBMS.<br/>                                          |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                              |
| Spazio dei nomi<br/>                | Radice \\ CIMV2 \\ RDBMS<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Provider di Desktop remoto Management Services](rdms-api-reference.md)
</dt> </dl>

 

 





