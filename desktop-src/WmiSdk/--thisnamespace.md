---
description: Contiene i diritti di sicurezza per lo spazio dei nomi sotto forma di descrittore di sicurezza.
ms.assetid: 84e514f5-b114-4bfc-ab0b-9745f249168b
ms.tgt_platform: multiple
title: __thisNAMESPACE classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __thisNAMESPACE
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 02e92bd8cb1c1827af86d23320e7347baa08c395d32def8c9b8adea2fcfd35bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132024"
---
# <a name="__thisnamespace-class"></a>\_\_Classe thisNAMESPACE

La **\_ \_ classe di sistema thisNAMESPACE** contiene i diritti di sicurezza per lo spazio dei nomi sotto forma di descrittore di sicurezza. Questa classe e una singola istanza si trovano in tutti gli spazi dei nomi.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[singleton]
class __thisNAMESPACE : __SystemClass
{
  uint8 SECURITY_DESCRIPTOR[];
};
```

## <a name="members"></a>Members

La **\_ \_ classe thisNAMESPACE** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **\_ \_ classe thisNAMESPACE** ha queste proprietà.

<dl> <dt>

**DESCRITTORE \_ DI SICUREZZA**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrittore di sicurezza che descrive chi può accedere allo spazio dei nomi e chi può leggere o scrivere nello spazio dei nomi. Questa proprietà viene ereditata [**\_ \_ dall'evento**](--event.md). Per altre informazioni sul formato dei descrittori di sicurezza, vedere [Descrittori](/windows/desktop/SecAuthZ/security-descriptors) di sicurezza nella sezione Sicurezza di Windows SDK.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'istanza singleton **\_ \_ di thisNAMESPACE** è di sola lettura. Per modificare le impostazioni della proprietà del descrittore di sicurezza, usare i metodi della [**\_ \_ classe SystemSecurity.**](--systemsecurity.md) La **\_ \_ classe thisNAMESPACE** deriva da [**\_ \_ SystemClass**](--systemclass.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |
| Spazio dei nomi<br/>                | Tutti gli spazi dei nomi WMI<br/>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_\_SystemClass**](/windows/desktop/WmiSdk/--systemclass)
</dt> <dt>

[Classi di sistema WMI](wmi-system-classes.md)
</dt> </dl>

 

