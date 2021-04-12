---
description: La \_ \_ classe di sistema MethodInvocationEvent è definita, ma non è implementata.
ms.assetid: ea736e44-a6bc-41e5-abc5-9e21a5504f44
ms.tgt_platform: multiple
title: Classe __MethodInvocationEvent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __MethodInvocationEvent
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: bc7e8d70d027caf31a90d49abc490c2de2d52fb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232640"
---
# <a name="__methodinvocationevent-class"></a>\_\_Classe MethodInvocationEvent

La classe di sistema **\_ \_ MethodInvocationEvent** è definita, ma non è implementata.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class __MethodInvocationEvent : __InstanceOperationEvent
{
  string       Method;
  __Parameters Parameters;
  boolean      PreCall;
  uint8        SECURITY_DESCRIPTOR[];
  object       TargetInstance;
  uint64       TIME_CREATED;
};
```

## <a name="members"></a>Members

La classe **\_ \_ MethodInvocationEvent** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **\_ \_ MethodInvocationEvent** dispone di queste proprietà.

<dl> <dt>

**Metodo**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Metodo richiamato per attivare l'evento.

</dd> <dt>

**Parametri**
</dt> <dd> <dl> <dt>

Tipo di dati: **\_ \_ parametri**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento a un'istanza di che rappresenta i parametri di input e di output della chiamata al metodo.

</dd> <dt>

**Prechiamata**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **true**, l'evento viene generato prima che venga chiamato il metodo.

</dd> <dt>

**descrittore di sicurezza \_**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrittore utilizzato dal provider di eventi per determinare gli utenti che possono ricevere l'evento. Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md). Per ulteriori informazioni, vedere [descrittori di sicurezza](/windows/desktop/SecAuthZ/security-descriptors).

</dd> <dt>

**TargetInstance**
</dt> <dd> <dl> <dt>

Tipo di dati: **Object**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Istanza su cui viene richiamato il metodo. Questa proprietà viene ereditata da [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).

</dd> <dt>

**ORA di \_ creazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore univoco che indica l'ora in cui viene generato un evento. Si tratta di un valore a 64 bit che rappresenta il numero di intervalli di 100-nanosecondi dopo il 1 ° gennaio 1601. Le informazioni sono nel formato UTC (Coordinated Universal Time). Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md).

Per ulteriori informazioni sull'utilizzo di valori **UInt64** negli script, vedere [scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **\_ \_ MethodInvocationEvent** deriva da [**\_ \_ InstanceOperationEvent**](--instanceoperationevent.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |
| Spazio dei nomi<br/>                | Tutti gli spazi dei nomi WMI<br/>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_\_InstanceOperationEvent**](/windows/desktop/WmiSdk/--instanceoperationevent)
</dt> <dt>

[Classi di sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

