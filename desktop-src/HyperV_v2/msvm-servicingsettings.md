---
description: Contiene le impostazioni utilizzate durante le operazioni di manutenzione.
ms.assetid: 17dc3c97-232c-4ac4-988c-84c3061b4133
title: Classe Msvm_ServicingSettings
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ServicingSettings
- Msvm_ServicingSettings.Version
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 16033583a012c71ef2150ff68dc06564e149de84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485269"
---
# <a name="msvm_servicingsettings-class"></a>\_Classe MSVM ServicingSettings

Contiene le impostazioni utilizzate durante le operazioni di manutenzione.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Singleton, AMENDMENT]
class Msvm_ServicingSettings
{
  string Version;
};
```

## <a name="members"></a>Members

La **classe \_ ServicingSettings di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ ServicingSettings di MSVM** dispone di queste proprietà.

<dl> <dt>

**Versione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Contiene la versione della definizione della classe.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

 




