---
title: Classe InstalledStoreProgram Win32 \_
description: La classe Win32 \_ InstalledStoreProgram rappresenta un'applicazione Windows store.
ms.assetid: 154c19c7-f2e5-48bd-b05b-3022e45f2aa4
keywords:
- Win32_InstalledStoreProgram classe Application e Device Inventory Provider
- Win32_InstalledStoreProgram classe Application e Device Inventory Provider , descritto
topic_type:
- apiref
api_name:
- Win32_InstalledStoreProgram
- Win32_InstalledStoreProgram.ProgramId
- Win32_InstalledStoreProgram.Name
- Win32_InstalledStoreProgram.Vendor
- Win32_InstalledStoreProgram.Version
- Win32_InstalledStoreProgram.Language
- Win32_InstalledStoreProgram.Architecture
api_location:
- Root\CIMv2
api_type:
- Schema
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 613baba9990da8403417aa4f8639ed7e9b5a7a5f
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122917910"
---
# <a name="win32_installedstoreprogram-class"></a>Classe InstalledStoreProgram Win32 \_

La **classe Win32 \_ InstalledStoreProgram** rappresenta un'applicazione Windows store.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
class Win32_InstalledStoreProgram
{
  string ProgramId;
  string Name;
  string Vendor;
  string Version;
  string Language;
  string Architecture;
};
```

## <a name="members"></a>Members

La **classe Win32 \_ InstalledStoreProgram** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Win32 \_ InstalledStoreProgram** ha queste proprietà.

<dl> <dt>

**Architettura**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Architetture del processore supportate per l'applicazione Windows store.

</dd> <dt>

**Lingua**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Lingue supportate per l'applicazione Windows store.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome dell'applicazione Windows store.

</dd> <dt>

**ProgramId**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Identificatore univoco dell'applicazione Windows store.

</dd> <dt>

**Fornitore**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Editore dell'applicazione Windows store.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Versione dell'applicazione Windows store.

</dd> </dl>

## <a name="requirements"></a>Requisiti



|                                     |                                                                                      |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                            |
| Spazio dei nomi<br/>                | Root\\CIMv2<br/>                                                               |
| MOF<br/>                      | <dl> <dt>Aeinv.mof</dt> </dl> |



 

 





