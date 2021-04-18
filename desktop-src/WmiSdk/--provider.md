---
description: Funge da classe padre per la \_ \_ classe di sistema Win32Provider.
ms.assetid: e4cad7c6-4650-4334-b8c4-ac65381bced7
ms.tgt_platform: multiple
title: Classe __Provider
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Provider
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 733323c106a5d682e7eddbe3a41bf9c156520c51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313213"
---
# <a name="__provider-class"></a>\_\_Classe provider

La classe di sistema del **\_ \_ provider** è una classe di base astratta che funge da classe padre per la classe di sistema [**\_ \_ Win32Provider**](--win32provider.md) .

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[abstract]
class __Provider : __SystemClass
{
  string Name;
};
```

## <a name="members"></a>Members

La classe del **\_ \_ provider** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe del **\_ \_ provider** presenta queste proprietà.

<dl> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [ **chiave**](standard-qualifiers.md)
</dt> </dl>

Stringa indipendente dalla lingua che identifica in modo univoco il provider. Per evitare conflitti di denominazione, è consigliabile il formato seguente:

\|versione provider \| Fornitore

Questo nome di provider rappresenta ad esempio la versione 1,0 di Microsoft TestProvider:

"Microsoft \| TestProvider \| v 1.0"

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **\_ \_ provider** è derivata da [**\_ \_ SystemClass**](--systemclass.md), che non dispone di proprietà.

I provider creano istanze [**\_ \_ Win32Provider**](--win32provider.md) per specificare le informazioni relative all'implementazione fisica.

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
</dt> <dt>

[**\_\_Win32Provider**](--win32provider.md)
</dt> </dl>

 

