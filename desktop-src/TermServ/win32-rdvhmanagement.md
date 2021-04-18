---
title: Classe Win32_RdvhManagement
description: Viene descritto un servizio di gestione di Desktop remoto host virtuale (RDVH).
ms.assetid: 2a81786c-e772-4596-9846-a46828f9b48b
ms.tgt_platform: multiple
keywords:
- Classe Win32_RdvhManagement Servizi Desktop remoto
- Classe Win32_RdvhManagement Servizi Desktop remoto, descritta
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
ms.openlocfilehash: b01e2cde81173035d00587782dc45d9ddeb66fcf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301741"
---
# <a name="win32_rdvhmanagement-class"></a>Win32 \_ RdvhManagement (classe)

Viene descritto un servizio di gestione di Desktop remoto host virtuale (RDVH).

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[dynamic, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_RdvhManagement
{
};
```

## <a name="members"></a>Members

La classe **Win32 \_ RdvhManagement** presenta questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

La classe **Win32 \_ RdvhManagement** presenta questi metodi.



| Metodo                                                                                  | Descrizione                                                                                                                                                             |
|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RdvCreateUserDiskTemplate**](rdvcreateuserdisktemplate-win32-rdvhmanagement.md)     | Crea il modello di disco utente della dimensione massima specificata e nella posizione specificata. Tutti i dischi utente creati avranno dimensioni massime corrispondenti alle dimensioni massime del modello.<br/> |
| [**RdvMigrateVmToDifferentHost**](rdvmigratevmtodifferenthost-win32-rdvhmanagement.md) | Avvia una migrazione in tempo reale della macchina virtuale in scenari VDI<br/>                                                                                               |
| [**RdvCopyBaseVmLocally**](rdvcopybasevmlocally-win32-rdvhmanagement.md)               | Copia il percorso della macchina virtuale di base localmente nel server Host di virtualizzazione DR<br/>                                                                                                           |
| [**RdvCreateUserDiskTemplate**](rdvcreateuserdisktemplate-win32-rdvhmanagement.md)     | Crea il modello di disco utente della dimensione massima specificata e nella posizione specificata. Tutti i dischi utente creati avranno dimensioni massime corrispondenti alle dimensioni massime del modello.<br/> |
| [**RdvMigrateVmToDifferentHost**](rdvmigratevmtodifferenthost-win32-rdvhmanagement.md) | Avvia una migrazione in tempo reale di una macchina virtuale in scenari VDI.<br/>                                                                                              |
| [**RdvSetupVMPermissions**](rdvsetupvmpermissions-win32-rdvhmanagement.md)             | Imposta le autorizzazioni nella macchina virtuale per il chiamante<br/>                                                                                                                        |
| [**RdvUndoVMPermissions**](rdvundovmpermissions-win32-rdvhmanagement.md)               | Ripristina le autorizzazioni in una macchina virtuale impostata da RdvSetupVMPermissions<br/>                                                                                                       |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                  |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                             |
| Spazio dei nomi<br/>                | Radice \\ CIMV2 \\ TerminalServices<br/>                                                   |
| MOF<br/>                      | <dl> <dt>TSVmHost. mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



 

 





