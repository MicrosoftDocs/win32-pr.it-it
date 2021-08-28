---
title: Classe Win32 \_ InstalledProgramFramework
description: La classe Win32 InstalledProgramFramework rappresenta un framework tecnologico con cui viene compilata o utilizzata un'istanza \_ di Win32 \_ InstalledWin32Program in fase di esecuzione.
ms.assetid: bb5c18c7-ec71-4579-8190-942de4fccd9e
keywords:
- Win32_InstalledProgramFramework classe Application e Device Inventory Provider
- Win32_InstalledProgramFramework classe Application e Device Inventory Provider , descritto
topic_type:
- apiref
api_name:
- Win32_InstalledProgramFramework
- Win32_InstalledProgramFramework.FrameworkName
- Win32_InstalledProgramFramework.FrameworkPublisher
- Win32_InstalledProgramFramework.FrameworkVersion
- Win32_InstalledProgramFramework.FrameworkVersionActual
- Win32_InstalledProgramFramework.ProgramId
- Win32_InstalledProgramFramework.IsPrivate
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
ms.openlocfilehash: 3e447544dbfdebd6e4f4dd12752171089b8da041
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122917896"
---
# <a name="win32_installedprogramframework-class"></a>Classe Win32 \_ InstalledProgramFramework

La **classe Win32 \_ InstalledProgramFramework** rappresenta un framework tecnologico con cui viene compilata o utilizzata un'istanza [**di Win32 \_ InstalledWin32Program**](win32-installedwin32program.md) in fase di esecuzione. I framework che questa classe può attualmente segnalare sono OpenSSL, Visual Basic, Visual C++ .Net, Visual C++, Java (rileva solo i file binari di runtime Java) e CLR.

> [!Note]  
> Il set di framework che questa classe può rilevare può essere aggiornato nel tempo.

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
class Win32_InstalledProgramFramework
{
  string  FrameworkName;
  string  FrameworkPublisher;
  string  FrameworkVersion;
  string  FrameworkVersionActual;
  string  ProgramId;
  boolean IsPrivate;
};
```

## <a name="members"></a>Members

La **classe Win32 \_ InstalledProgramFramework** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Win32 \_ InstalledProgramFramework** ha queste proprietà.

<dl> <dt>

**Frameworkname**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Nome del framework da cui dipende l'applicazione identificata da **ProgramId.**

</dd> <dt>

**FrameworkPublisher**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Editore del framework.

</dd> <dt>

**FrameworkVersion**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Versione del framework da cui l'applicazione ha una dipendenza.

</dd> <dt>

**FrameworkVersionActual**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Versione del framework effettivamente utilizzata dall'applicazione in fase di esecuzione, se il framework può essere rilevato.

</dd> <dt>

**IsPrivate**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

TRUE se l'applicazione aggrega una copia privata del framework.

</dd> <dt>

**ProgramId**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Identificatore univoco [**dell'istanza di Win32 \_ InstalledWin32Program,**](win32-installedwin32program.md) a cui sono associati i dati del framework.

</dd> </dl>

## <a name="requirements"></a>Requisiti



|                                     |                                                                                      |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                           |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                            |
| Spazio dei nomi<br/>                | Root\\CIMv2<br/>                                                               |
| MOF<br/>                      | <dl> <dt>Aeinv.mof</dt> </dl> |



 

 





