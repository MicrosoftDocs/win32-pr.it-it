---
title: Metodo SchedulePatch della classe Win32_RDMSVirtualDesktopCollection
description: Pianifica un processo di provisioning degli aggiornamenti software che installa gli aggiornamenti software nelle macchine virtuali in una raccolta di desktop virtuali.
ms.assetid: 780d5709-9e7d-41d9-a4d0-b5d021615655
ms.tgt_platform: multiple
keywords:
- Metodo SchedulePatch Servizi Desktop remoto
- Il metodo SchedulePatch Servizi Desktop remoto , Win32_RDMSVirtualDesktopCollection classe
- Win32_RDMSVirtualDesktopCollection classe Servizi Desktop remoto , metodo SchedulePatch
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.SchedulePatch
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb29eb42f0f1d13ff1bf234c6fb41b8f414317a4b723af9a6d215cf25fa2ec95
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865511"
---
# <a name="schedulepatch-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Metodo SchedulePatch della classe \_ WIN32 RDMSVirtualDesktopCollection

Pianifica un processo di provisioning degli aggiornamenti software che installa gli aggiornamenti software nelle macchine virtuali in una raccolta di desktop virtuali.

## <a name="syntax"></a>Sintassi


```mof
uint32 SchedulePatch(
  [in] DATETIME StartTime,
  [in] DATETIME ForceLogOffTime,
  [in] string   JobInputXml
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*StartTime* \[ Pollici\]
</dt> <dd>

> [!Note]  
> Il sistema non disconnetterà gli utenti delle macchine virtuali fino all'ora specificata nel *parametro ForceLogOffTime.*

 

Data e ora di installazione degli aggiornamenti.

</dd> <dt>

*ForceLogOffTime* \[ Pollici\]
</dt> <dd>

Data e ora in cui il sistema disconnetterà gli utenti delle macchine virtuali.

</dd> <dt>

*JobInputXml* \[ Pollici\]
</dt> <dd>

Stringa in formato XML che contiene le informazioni sul processo di aggiornamento software.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo. In caso contrario, restituisce un codice di errore WMI.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                              |
| Spazio dei nomi<br/>                | Root \\ CIMv2 \\ rdms<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ RDMSVirtualDesktopCollection**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





