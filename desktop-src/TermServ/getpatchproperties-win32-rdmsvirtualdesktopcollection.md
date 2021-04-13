---
title: Metodo GetPatchProperties della classe Win32_RDMSVirtualDesktopCollection
description: Recupera le proprietà di un processo di provisioning degli aggiornamenti software per le macchine virtuali in un insieme di desktop virtuali.
ms.assetid: 9f228d89-0613-49c7-8169-48491c3a2d9b
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetPatchProperties
- Metodo GetPatchProperties Servizi Desktop remoto, classe Win32_RDMSVirtualDesktopCollection
- Classe Win32_RDMSVirtualDesktopCollection Servizi Desktop remoto, metodo GetPatchProperties
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.GetPatchProperties
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f0ca45c97512818aa5f8a9ea851d18fa5554c32
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518184"
---
# <a name="getpatchproperties-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Metodo GetPatchProperties della \_ classe RDMSVirtualDesktopCollection Win32

Recupera le proprietà di un processo di provisioning degli aggiornamenti software per le macchine virtuali in un insieme di desktop virtuali.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetPatchProperties(
  [out] DATETIME StartTime,
  [out] DATETIME ForceLogOffTime,
  [out] string   JobGuid,
  [out] uint32   State
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*StartTime* \[ out\]
</dt> <dd>

Data e ora in cui installare gli aggiornamenti.

</dd> <dt>

*ForceLogOffTime* \[ out\]
</dt> <dd>

Data e ora in cui il sistema disconnetterà gli utenti delle macchine virtuali.

</dd> <dt>

*JobGuid* \[ out\]
</dt> <dd>

**GUID** che identifica in modo univoco il processo di provisioning.

</dd> <dt>

*Stato* \[ di out\]
</dt> <dd>

Stato del processo di provisioning.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                              |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ RDBMS<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_RDMSVirtualDesktopCollection Win32**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





