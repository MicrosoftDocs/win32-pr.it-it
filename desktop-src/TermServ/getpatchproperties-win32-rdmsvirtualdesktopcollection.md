---
title: Metodo GetPatchProperties della classe Win32_RDMSVirtualDesktopCollection
description: Recupera le proprietà di un processo di provisioning degli aggiornamenti software per le macchine virtuali in una raccolta di desktop virtuali.
ms.assetid: 9f228d89-0613-49c7-8169-48491c3a2d9b
ms.tgt_platform: multiple
keywords:
- Metodo GetPatchProperties Servizi Desktop remoto
- Metodo GetPatchProperties Servizi Desktop remoto , Win32_RDMSVirtualDesktopCollection classe
- Win32_RDMSVirtualDesktopCollection classe Servizi Desktop remoto metodo , GetPatchProperties
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
ms.openlocfilehash: 969a73e372dee430b280d4d16c267c6d8b75dda236c3ae7362d2392cb1bf8bf3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099511"
---
# <a name="getpatchproperties-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Metodo GetPatchProperties della classe \_ WIN32 RDMSVirtualDesktopCollection

Recupera le proprietà di un processo di provisioning degli aggiornamenti software per le macchine virtuali in una raccolta di desktop virtuali.

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

*StartTime* \[ Cambio\]
</dt> <dd>

Data e ora di installazione degli aggiornamenti.

</dd> <dt>

*ForceLogOffTime* \[ Cambio\]
</dt> <dd>

Data e ora in cui il sistema disconnetterà gli utenti delle macchine virtuali.

</dd> <dt>

*JobGuid* \[ Cambio\]
</dt> <dd>

GUID **che** identifica in modo univoco il processo di provisioning.

</dd> <dt>

*Stato* \[ Cambio\]
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
| Spazio dei nomi<br/>                | Rdms \\ CIMv2 \\ radice<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ RDMSVirtualDesktopCollection**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





