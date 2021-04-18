---
title: Classe Win32_RDMSDeploymentSettings
description: Gestisce le impostazioni di distribuzione per un insieme di desktop virtuali.
ms.assetid: c33563d5-a388-46d3-b23a-797aab9d472a
ms.tgt_platform: multiple
keywords:
- Classe Win32_RDMSDeploymentSettings Servizi Desktop remoto
- Classe Win32_RDMSDeploymentSettings Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_RDMSDeploymentSettings
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6be75f74a71a82800bc6fdd7ba0c4bae5a85021
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517625"
---
# <a name="win32_rdmsdeploymentsettings-class"></a>Win32 \_ RDMSDeploymentSettings (classe)

Gestisce le impostazioni di distribuzione per un insieme di desktop virtuali.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSDeploymentSettings
{
};
```

## <a name="members"></a>Members

La classe **Win32 \_ RDMSDeploymentSettings** presenta questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

La classe **Win32 \_ RDMSDeploymentSettings** presenta questi metodi.



| Metodo                                                                                                  | Descrizione                                                                                                                       |
|:--------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [**GetBaseVHDPath**](getbasevhdpath-win32-rdmsdeploymentsettings.md)                                   | Recupera il percorso di base della directory in cui vengono distribuiti i VHD dell'insieme di desktop virtuali.<br/>                 |
| [**GetConnectionString**](win32-rdmsdeploymentsettings-getconnectionstring.md)                         | Recupera la stringa di connessione del database a livello di distribuzione.<br/>                                                             |
| [**GetDiffVHDPath**](getdiffvhdpath-win32-rdmsdeploymentsettings.md)                                   | Recupera il percorso della directory in cui vengono distribuiti i dischi differenze per un insieme di desktop virtuali.<br/>            |
| [**GetExportPath**](getexportpath-win32-rdmsdeploymentsettings.md)                                     | Recupera il percorso della directory in cui vengono distribuite le macchine virtuali per un insieme di desktop virtuali.<br/>                  |
| [**GetInt32Property**](getint32property-win32-rdmsdeploymentsettings.md)                               | Recupera una proprietà integer per le impostazioni di distribuzione di un insieme di desktop virtuali.<br/>                             |
| [**GetSecondaryConnectionString**](win32-rdmsdeploymentsettings-getsecondaryconnectionstring.md)       | Recupera la stringa di connessione secondaria del database a livello di distribuzione, che può essere utilizzata per supportare la scadenza della password.<br/> |
| [**GetSMBPath**](getsmbpath-win32-rdmsdeploymentsettings.md)                                           | Recupera il percorso UNC della condivisione SMB a cui vengono distribuite le macchine virtuali dell'insieme di desktop virtuali.<br/>      |
| [**GetStringArrayDeploymentSetting**](getstringarraydeploymentsetting-win32-rdmsdeploymentsettings.md) | Recupera le impostazioni di distribuzione per un insieme di desktop virtuali.<br/>                                                    |
| [**GetStringProperty**](getstringproperty-win32-rdmsdeploymentsettings.md)                             | Recupera una proprietà di stringa per le impostazioni di distribuzione di un insieme di desktop virtuali.<br/>                               |
| [**RemoveDeploymentSetting**](removedeploymentsetting-win32-rdmsdeploymentsettings.md)                 | Elimina le impostazioni di distribuzione per un insieme di desktop virtuali.<br/>                                                      |
| [**SetBaseVHDPath**](setbasevhdpath-win32-rdmsdeploymentsettings.md)                                   | Recupera il percorso di base della directory in cui vengono distribuiti i VHD dell'insieme di desktop virtuali.<br/>                 |
| [**SetConnectionString**](win32-rdmsdeploymentsettings-setconnectionstring.md)                         | Imposta la stringa di connessione del database a livello di distribuzione.<br/>                                                                  |
| [**SetDiffVHDPath**](setdiffvhdpath-win32-rdmsdeploymentsettings.md)                                   | Aggiorna il percorso della directory in cui vengono distribuiti i dischi differenze per un insieme di desktop virtuali.<br/>              |
| [**SetExportPath**](setexportpath-win32-rdmsdeploymentsettings.md)                                     | Aggiorna il percorso della directory in cui vengono distribuite le macchine virtuali per un insieme di desktop virtuali.<br/>                    |
| [**SetInt32Property**](setint32property-win32-rdmsdeploymentsettings.md)                               | Aggiorna una proprietà integer per le impostazioni di distribuzione di un insieme di desktop virtuali.<br/>                               |
| [**SetSecondaryConnectionString**](win32-rdmsdeploymentsettings-setsecondaryconnectionstring.md)       | Imposta la stringa di connessione secondaria del database a livello di distribuzione.<br/>                                                        |
| [**SetSMBPath**](setsmbpath-win32-rdmsdeploymentsettings.md)                                           | Aggiorna il percorso UNC della condivisione SMB a cui vengono distribuite le macchine virtuali dell'insieme di desktop virtuali.<br/>        |
| [**SetStringArrayDeploymentSetting**](setstringarraydeploymentsetting-win32-rdmsdeploymentsettings.md) | Aggiorna le impostazioni di distribuzione per un insieme di desktop virtuali.<br/>                                                      |
| [**SetStringProperty**](setstringproperty-win32-rdmsdeploymentsettings.md)                             | Aggiorna una proprietà di stringa per le impostazioni di distribuzione di un insieme di desktop virtuali.<br/>                                 |



 

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

 

 





