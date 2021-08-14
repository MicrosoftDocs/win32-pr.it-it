---
description: Segnala un evento di creazione dello spazio dei nomi, ovvero un tipo di evento intrinseco generato quando viene aggiunto un nuovo spazio dei nomi allo spazio dei nomi corrente.
ms.assetid: 50b9860a-d6e8-4dab-a7d0-09da9dd37b6b
ms.tgt_platform: multiple
title: __NamespaceCreationEvent classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NamespaceCreationEvent
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 2f84e0c584d3afb63b166523a5920d4d5b3367638bc0000c33a8cfba979e64c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118320725"
---
# <a name="__namespacecreationevent-class"></a>\_\_Classe NamespaceCreationEvent

La **\_ \_ classe di sistema NamespaceCreationEvent** segnala un evento [](determining-the-type-of-event-to-receive.md) di creazione dello spazio dei nomi, ovvero un tipo di evento intrinseco generato quando viene aggiunto un nuovo spazio dei nomi allo spazio dei nomi corrente.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class __NamespaceCreationEvent : __NamespaceOperationEvent
{
  uint8       SECURITY_DESCRIPTOR[];
  __Namespace TargetNamespace;
  uint64      TIME_CREATED;
};
```

## <a name="members"></a>Members

La **\_ \_ classe NamespaceCreationEvent** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **\_ \_ classe NamespaceCreationEvent** ha queste proprietà.

<dl> <dt>

**DESCRITTORE \_ DI SICUREZZA**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrittore utilizzato dal provider di eventi per determinare quali utenti possono ricevere l'evento. Questa proprietà viene ereditata [**\_ \_ dall'evento**](--event.md).

</dd> <dt>

**Targetnamespace**
</dt> <dd> <dl> <dt>

Tipo di dati: **\_ \_ Spazio dei nomi**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Copia [**\_ \_ dell'istanza dello**](--namespace.md) spazio dei nomi creata. La **proprietà Name** dell'istanza **\_ \_ namespace** indica lo spazio dei nomi creato. Questa proprietà viene ereditata da [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md).

</dd> <dt>

**ORA \_ DI CREAZIONE**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore univoco che indica l'ora in cui è stato generato l'evento. Valore a 64 bit che rappresenta il numero di intervalli di 100 nanosecondi dopo il 1° gennaio 1601. Le informazioni sono nel formato Coordinated Universal Time (UTC). Questa proprietà viene ereditata [**\_ \_ dall'evento**](--event.md).

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Commenti

La **\_ \_ classe NamespaceCreationEvent** è derivata da [**\_ \_ NamespaceOperationEvent**](--namespaceoperationevent.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |
| Spazio dei nomi<br/>                | Tutti gli spazi dei nomi WMI<br/>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_\_NamespaceOperationEvent**](/windows/desktop/WmiSdk/--namespaceoperationevent)
</dt> <dt>

[Classi di sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

