---
title: Win32_CentralPublishingChangeEvent classe
description: Evento che rappresenta una modifica alle impostazioni RDV centrali.
ms.assetid: 95be015e-a185-4548-a7f7-a22b351a34c8
ms.tgt_platform: multiple
keywords:
- Win32_CentralPublishingChangeEvent classe Servizi Desktop remoto
- Win32_CentralPublishingChangeEvent classe Servizi Desktop remoto , descritto
topic_type:
- apiref
api_name:
- Win32_CentralPublishingChangeEvent
- Win32_CentralPublishingChangeEvent.SECURITY_DESCRIPTOR
- Win32_CentralPublishingChangeEvent.TIME_CREATED
- Win32_CentralPublishingChangeEvent.TargetInstance
- Win32_CentralPublishingChangeEvent.OperationType
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bbc38d132920bd5ffcaa2208d8f1aa94c8629bb0c5399f6b8776654d078cd47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868521"
---
# <a name="win32_centralpublishingchangeevent-class"></a>Classe \_ CentralPublishingChangeEvent Win32

Evento che rappresenta una modifica alle impostazioni RDV centrali.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
class Win32_CentralPublishingChangeEvent : __ExtrinsicEvent
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
  object TargetInstance;
  uint32 OperationType;
};
```

## <a name="members"></a>Members

La **classe Win32 \_ CentralPublishingChangeEvent** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Win32 \_ CentralPublishingChangeEvent** ha queste proprietà.

<dl> <dt>

**Tipo operazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di operazione corrispondente all'evento.

<dt>

<span id="Create"></span><span id="create"></span><span id="CREATE"></span>

**Crea** (0)


</dt> <dd></dd> <dt>

<span id="Modify"></span><span id="modify"></span><span id="MODIFY"></span>

**Modifica** (1)


</dt> <dd></dd> <dt>

<span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>

**Elimina** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**DESCRITTORE \_ DI SICUREZZA**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrittore utilizzato dal provider di eventi per determinare quali utenti possono ricevere l'evento. Questa proprietà viene ereditata [**\_ \_ dall'evento**](/windows/desktop/WmiSdk/--event). Per altre informazioni sulle costanti utilizzate per impostare questo descrittore di sicurezza, vedere [Costanti di sicurezza WMI](/windows/desktop/WmiSdk/wmi-security-constants).

</dd> <dt>

**TargetInstance**
</dt> <dd> <dl> <dt>

Tipo di dati: **object**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Oggetto modificato dall'operazione corrispondente all'evento.

</dd> <dt>

**ORA \_ DI CREAZIONE**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore univoco che indica l'ora in cui è stato generato l'evento. Valore a 64 bit che rappresenta il numero di intervalli di 100 nanosecondi dopo il 1° gennaio 1601. Le informazioni sono nel formato UTC (Coordinated Universal Times). Questa proprietà viene ereditata [**\_ \_ dall'evento**](/windows/desktop/WmiSdk/--event).

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                           |
| Spazio dei nomi<br/>                | TerminalServices \\ cimv2 \\ radice<br/>                                                 |
| MOF<br/>                      | <dl> <dt>Tscpub.mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TscPubWmi.dll</dt> </dl> |



 

