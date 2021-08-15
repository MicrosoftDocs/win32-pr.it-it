---
description: Classe di base astratta che funge da classe padre per tutti gli eventi intrinseci ed estensivi.
ms.assetid: 4d2e4715-041c-49e9-b948-a148dfe85483
ms.tgt_platform: multiple
title: __Event classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Event
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: a74abb8a02676ba97ffb7a41df6ee4a3bd7f428d5288e376f85d61927fbb0e06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118821092"
---
# <a name="__event-class"></a>\_\_Classe di evento

La **\_ \_ classe** di sistema Event è una classe di base astratta che funge da classe padre per tutti gli eventi intrinseci ed estensivi. Tutti i nuovi tipi di evento devono infine derivare da **\_ \_ Event**. Gli eventi intrinseci derivano direttamente da questa classe. Gli eventi estensivi definiti dall'utente derivano da una sottoclasse di questa classe denominata [**\_ \_ ExtrinsicEvent**](--extrinsicevent.md).

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[abstract]
class __Event : __IndicationRelated
{
  uint8  SECURITY_DESCRIPTOR[];
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Members

La **\_ \_ classe Event** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **\_ \_ classe Event** ha queste proprietà.

<dl> <dt>

**DESCRITTORE \_ DI SICUREZZA**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrittore utilizzato dal provider di eventi per determinare quali utenti possono ricevere l'evento. Per altre informazioni, vedere [Costanti di sicurezza WMI](wmi-security-constants.md).

</dd> <dt>

**ORA \_ DI CREAZIONE**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore univoco che indica l'ora in cui viene generato l'evento. Valore a 64 bit che rappresenta il numero di intervalli di 100 nanosecondi dopo il 1° gennaio 1601. Le informazioni sono nel formato Coordinated Universal Time (UTC).

Per altre informazioni sull'uso **dei valori uint64** negli script, vedere [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

</dd> </dl>

## <a name="remarks"></a>Commenti

La **\_ \_ classe Event** è derivata da [**\_ \_ IndicationRelated,**](--indicationrelated.md)che non dispone di proprietà.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |
| Spazio dei nomi<br/>                | Tutti gli spazi dei nomi WMI<br/>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_\_Indicazione Correlata**](/windows/desktop/WmiSdk/--indicationrelated)
</dt> <dt>

[Classi di sistema WMI](wmi-system-classes.md)
</dt> <dt>

[Determinazione del tipo di evento da ricevere](determining-the-type-of-event-to-receive.md)
</dt> <dt>

[**\_\_ClassOperationEvent**](--classoperationevent.md)
</dt> <dt>

[**\_\_InstanceOperationEvent**](--instanceoperationevent.md)
</dt> <dt>

[**\_\_NamespaceOperationEvent**](--namespaceoperationevent.md)
</dt> </dl>

 

