---
title: Metodo ProvisioningPrepJob della classe Win32_RDMSVirtualDesktopCollection
description: Consente di creare un processo di provisioning di desktop virtuale.
ms.assetid: 240D4BE6-95BD-4858-8F8F-A00C92042AEF
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo ProvisioningPrepJob
- Metodo ProvisioningPrepJob Servizi Desktop remoto, interfaccia Win32_RDMSVirtualDesktopCollection
- Interfaccia Win32_RDMSVirtualDesktopCollection Servizi Desktop remoto, metodo ProvisioningPrepJob
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningPrepJob
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9727dec0e31dd199f324ed01a4510041ba3558f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964135"
---
# <a name="provisioningprepjob-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Metodo ProvisioningPrepJob della \_ classe RDMSVirtualDesktopCollection Win32

Consente di creare un processo di provisioning di desktop virtuale.

## <a name="syntax"></a>Sintassi


```mof
uint32 ProvisioningPrepJob(
  [in]  string  CollectionAlias,
  [in]  string  VMHostName,
  [in]  string  VMName,
  [in]  string  ExportToLocation,
  [in]  boolean bSysPrep,
  [in]  string  MachineName,
  [in]  string  UserName,
  [in]  string  Password,
  [out] string  JobGuid
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*CollectionAlias* \[ in\]
</dt> <dd>

Alias della raccolta che ospita il desktop virtuale.

</dd> <dt>

*VMHostName* \[ in\]
</dt> <dd>

Nome host della macchina virtuale.

</dd> <dt>

*VMName* \[ in\]
</dt> <dd>

Nome della macchina virtuale.

</dd> <dt>

*ExportToLocation* \[ in\]
</dt> <dd>

Percorso completo della posizione in cui esportare il processo di provisioning.

</dd> <dt>

*bSysPrep* \[ in\]
</dt> <dd>

Indica se il processo di provisioning rappresenta una distribuzione di Sysprep.

</dd> <dt>

*Nomecomputer* \[ in\]
</dt> <dd>

Nome del computer che ospita la macchina virtuale.

</dd> <dt>

*Nome utente* \[ in\]
</dt> <dd>

Nome utente dell'amministratore della macchina virtuale.

</dd> <dt>

*Password* \[ di in\]
</dt> <dd>

Password dell'amministratore della macchina virtuale.

</dd> <dt>

*JobGuid* \[ out\]
</dt> <dd>

**GUID** che identifica in modo univoco il processo di provisioning.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                              |
| Spazio dei nomi<br/>                | Radice \\ CIMV2 \\ RDBMS<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_RDMSVirtualDesktopCollection Win32**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





