---
title: Win32_RdvhManagement classe
description: Descrive un Desktop remoto di gestione host virtuale (RDVH).
ms.assetid: 2a81786c-e772-4596-9846-a46828f9b48b
ms.tgt_platform: multiple
keywords:
- Win32_RdvhManagement classe Servizi Desktop remoto
- Win32_RdvhManagement classe Servizi Desktop remoto , descritto
topic_type:
- apiref
api_name:
- Win32_RdvhManagement
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ea403621aa23cb999bdf2fe692e2d4e053866492608e71346d978cb764ab005
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119422581"
---
# <a name="win32_rdvhmanagement-class"></a>Classe \_ RdvhManagement Win32

Descrive un Desktop remoto di gestione host virtuale (RDVH).

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[dynamic, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_RdvhManagement
{
};
```

## <a name="members"></a>Members

La **classe \_ Win32 RdvhManagement** ha questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

La **classe \_ Win32 RdvhManagement** include questi metodi.



| Metodo                                                                                  | Descrizione                                                                                                                                                             |
|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RdvCreateUserDiskTemplate**](rdvcreateuserdisktemplate-win32-rdvhmanagement.md)     | Crea un modello di disco utente con le dimensioni massime specificate e nel percorso specificato. Tutti i dischi utente creati avranno dimensioni massime corrispondenti alle dimensioni massime del modello.<br/> |
| [**RdvMigrateVmToDifferentHost**](rdvmigratevmtodifferenthost-win32-rdvhmanagement.md) | Avvia una migrazione in tempo reale della macchina virtuale in scenari VDI<br/>                                                                                               |
| [**RdvCopyBaseVmLocally**](rdvcopybasevmlocally-win32-rdvhmanagement.md)               | Copia il percorso della macchina virtuale di base in locale Host di virtualizzazione DR server<br/>                                                                                                           |
| [**RdvCreateUserDiskTemplate**](rdvcreateuserdisktemplate-win32-rdvhmanagement.md)     | Crea un modello di disco utente con le dimensioni massime specificate e nel percorso specificato. Tutti i dischi utente creati avranno dimensioni massime corrispondenti alle dimensioni massime del modello.<br/> |
| [**RdvMigrateVmToDifferentHost**](rdvmigratevmtodifferenthost-win32-rdvhmanagement.md) | Avvia una migrazione in tempo reale della macchina virtuale in scenari VDI.<br/>                                                                                              |
| [**RdvSetupVMPermissions**](rdvsetupvmpermissions-win32-rdvhmanagement.md)             | Imposta le autorizzazioni nella macchina virtuale per il chiamante<br/>                                                                                                                        |
| [**Autorizzazioni RdvUndoVMPermissions**](rdvundovmpermissions-win32-rdvhmanagement.md)               | Ripristina le autorizzazioni nella macchina virtuale impostata da RdvSetupVMPermissions<br/>                                                                                                       |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                  |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                             |
| Spazio dei nomi<br/>                | Radice \\ cimv2 \\ TerminalServices<br/>                                                   |
| MOF<br/>                      | <dl> <dt>TSVmHost.mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



 

 





