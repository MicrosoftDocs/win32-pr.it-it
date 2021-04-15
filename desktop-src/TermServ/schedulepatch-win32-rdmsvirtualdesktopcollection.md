---
title: Metodo SchedulePatch della classe Win32_RDMSVirtualDesktopCollection
description: Pianifica un processo di provisioning degli aggiornamenti software che installa gli aggiornamenti software nelle macchine virtuali in un insieme di desktop virtuali.
ms.assetid: 780d5709-9e7d-41d9-a4d0-b5d021615655
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SchedulePatch
- Metodo SchedulePatch Servizi Desktop remoto, classe Win32_RDMSVirtualDesktopCollection
- Classe Win32_RDMSVirtualDesktopCollection Servizi Desktop remoto, metodo SchedulePatch
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
ms.openlocfilehash: 7d9585e3d13ea1f02115506741c153d62c33fcc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476421"
---
# <a name="schedulepatch-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Metodo SchedulePatch della \_ classe RDMSVirtualDesktopCollection Win32

Pianifica un processo di provisioning degli aggiornamenti software che installa gli aggiornamenti software nelle macchine virtuali in un insieme di desktop virtuali.

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

*StartTime* \[ in\]
</dt> <dd>

> [!Note]  
> Il sistema non disconnette gli utenti delle macchine virtuali fino al momento specificato nel parametro *ForceLogOffTime* .

 

Data e ora in cui installare gli aggiornamenti.

</dd> <dt>

*ForceLogOffTime* \[ in\]
</dt> <dd>

Data e ora in cui il sistema disconnetterà gli utenti delle macchine virtuali.

</dd> <dt>

*JobInputXml* \[ in\]
</dt> <dd>

Stringa in formato XML che contiene le informazioni sul processo di aggiornamento software.

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

 

 





