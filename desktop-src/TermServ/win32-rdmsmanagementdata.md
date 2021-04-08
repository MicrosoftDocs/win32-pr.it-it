---
title: Classe Win32_RDMSManagementData
description: Sincronizza i dati di pubblicazione per Desktop remoto Management Services (RDBMS).
ms.assetid: 17f06294-6580-4297-9301-f88314db7775
ms.tgt_platform: multiple
keywords:
- Classe Win32_RDMSManagementData Servizi Desktop remoto
- Classe Win32_RDMSManagementData Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_RDMSManagementData
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dddf2a73673e886456eb43bfbd2cefc72250cc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047956"
---
# <a name="win32_rdmsmanagementdata-class"></a>Win32 \_ RDMSManagementData (classe)

Sincronizza i dati di pubblicazione per Desktop remoto Management Services (RDBMS).

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSManagementData
{
};
```

## <a name="members"></a>Members

La classe **Win32 \_ RDMSManagementData** presenta questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

La classe **Win32 \_ RDMSManagementData** presenta questi metodi.



| Metodo                                                                                        | Descrizione                                                            |
|:----------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [**SynchronizeAllPublishingData**](synchronizeallpublishingdata-win32-rdmsmanagementdata.md) | Sincronizza tutti i dati di pubblicazione per RDBMS.<br/>                  |
| [**SynchronizePublishingData**](synchronizepublishingdata-win32-rdmsmanagementdata.md)       | Sincronizza il set specificato di dati di pubblicazione per RDBMS.<br/> |



 

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

 

 





