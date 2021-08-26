---
title: Win32_RDMSDesktopAssignment classe
description: Descrive l'assegnazione di Desktop utente raccolta Desktop remoto.
ms.assetid: d3370cf2-65db-4e01-9ea3-9a71340bf71b
ms.tgt_platform: multiple
keywords:
- Win32_RDMSDesktopAssignment classe Servizi Desktop remoto
- Win32_RDMSDesktopAssignment classe Servizi Desktop remoto , descritto
topic_type:
- apiref
api_name:
- Win32_RDMSDesktopAssignment
- Win32_RDMSDesktopAssignment.CollectionAlias
- Win32_RDMSDesktopAssignment.DesktopName
- Win32_RDMSDesktopAssignment.UserName
- Win32_RDMSDesktopAssignment.UserDomain
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88576607777fe55d2fb2d4d9232ddc9d4b23849503e56f53fe4cd99f3931ddea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868211"
---
# <a name="win32_rdmsdesktopassignment-class"></a>Classe \_ RDMSDesktopAssignment Win32

Descrive l'assegnazione di Desktop utente raccolta Desktop remoto.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSDesktopAssignment
{
  string CollectionAlias;
  string DesktopName;
  string UserName;
  string UserDomain;
};
```

## <a name="members"></a>Members

La **classe \_ WIN32 RDMSDesktopAssignment** include questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe \_ WIN32 RDMSDesktopAssignment** include questi metodi.



| Metodo                                                                                 | Descrizione                              |
|:---------------------------------------------------------------------------------------|:-----------------------------------------|
| [**AddDesktopAssignment**](win32-rdmsdesktopassignment-adddesktopassignment.md)       | Aggiunge un'assegnazione desktop.<br/>    |
| [**RemoveDesktopAssignment**](win32-rdmsdesktopassignment-removedesktopassignment.md) | Rimuove un'assegnazione desktop.<br/> |



 

### <a name="properties"></a>Proprietà

La **classe \_ WIN32 RDMSDesktopAssignment** ha queste proprietà.

<dl> <dt>

**CollectionAlias**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Alias della raccolta.

</dd> <dt>

**DesktopName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nome del desktop.

</dd> <dt>

**UserDomain**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nome di dominio dell'account utente.

</dd> <dt>

**UserName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> <dt>

Qualificatori: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nome dell'account utente.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                              |
| Spazio dei nomi<br/>                | Radice \\ cimv2 \\ rdms<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



 

