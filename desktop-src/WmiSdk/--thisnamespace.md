---
description: Include i privilegi di protezione per lo spazio dei nomi sotto forma di descrittore di sicurezza.
ms.assetid: 84e514f5-b114-4bfc-ab0b-9745f249168b
ms.tgt_platform: multiple
title: Classe __thisNAMESPACE
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
ms.openlocfilehash: 440ccdf0eda794b5d648cae756f9a9c808eb2db6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316587"
---
# <a name="__thisnamespace-class"></a>\_\_Classe thisNAMESPACE

La classe di sistema **\_ \_ thisNamespace** include i privilegi di protezione per lo spazio dei nomi sotto forma di descrittore di sicurezza. Questa classe e una singola istanza si trovano in tutti gli spazi dei nomi.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[singleton]
class __thisNAMESPACE : __SystemClass
{
  uint8 SECURITY_DESCRIPTOR[];
};
```

## <a name="members"></a>Members

La classe **\_ \_ thisNamespace** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **\_ \_ thisNamespace** dispone di queste proprietà.

<dl> <dt>

**descrittore di sicurezza \_**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **Uint8**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrittore di sicurezza che descrive chi può accedere allo spazio dei nomi e chi può leggere o scrivere nello spazio dei nomi. Questa proprietà viene ereditata dall' [**\_ \_ evento**](--event.md). Per ulteriori informazioni sul formato dei descrittori di sicurezza, vedere [descrittori di sicurezza](/windows/desktop/SecAuthZ/security-descriptors) nella sezione sicurezza del Windows SDK.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'istanza singleton di **\_ \_ thisNamespace** è di sola lettura. Per modificare le impostazioni della proprietà del descrittore di sicurezza, utilizzare i metodi della classe [**\_ \_ SystemSecurity**](--systemsecurity.md) . La classe **\_ \_ thisNamespace** deriva da [**\_ \_ SystemClass**](--systemclass.md).

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

 

