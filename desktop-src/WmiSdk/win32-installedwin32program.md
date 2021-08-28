---
title: Classe Win32 \_ InstalledWin32Program
description: La classe Win32 \_ InstalledWin32Program rappresenta un'applicazione Win32 installata.
ms.assetid: 2eef00da-8597-4852-b4fb-4276d05fd724
keywords:
- Win32_InstalledWin32Program classe Application e Device Inventory Provider
- Win32_InstalledWin32Program classe Application e Device Inventory Provider , descritto
topic_type:
- apiref
api_name:
- Win32_InstalledWin32Program
- Win32_InstalledWin32Program.ProgramId
- Win32_InstalledWin32Program.Name
- Win32_InstalledWin32Program.Vendor
- Win32_InstalledWin32Program.Version
- Win32_InstalledWin32Program.Language
- Win32_InstalledWin32Program.MsiPackageCode
- Win32_InstalledWin32Program.MsiProductCode
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
ms.openlocfilehash: 51cfbf56591bca71f8364d97a9a4adb0d995c4c3
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122917904"
---
# <a name="win32_installedwin32program-class"></a>Classe Win32 \_ InstalledWin32Program

La **classe Win32 \_ InstalledWin32Program** rappresenta un'applicazione Win32 installata.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
class Win32_InstalledWin32Program
{
  string ProgramId;
  string Name;
  string Vendor;
  string Version;
  string Language;
  string MsiPackageCode;
  string MsiProductCode;
};
```

## <a name="members"></a>Members

La **classe Win32 \_ InstalledWin32Program** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Win32 \_ InstalledWin32Program** ha queste proprietà.

<dl> <dt>

**Lingua**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Lingue supportate per l'applicazione Win32 installata.

</dd> <dt>

**MsiPackageCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Codice del pacchetto MSI, se l'applicazione Win32 è stata installata usando un'istanza del servizio gestito.

</dd> <dt>

**MsiProductCode**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Codice del prodotto MSI, se l'applicazione Win32 è stata installata usando un'istanza del servizio gestito.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome dell'applicazione Win32 installata.

</dd> <dt>

**ProgramId**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Identificatore univoco dell'applicazione Win32 installata. Questo valore consente di correlare **Win32 \_ InstalledWin32Program** [**con Win32 \_ InstalledProgramFramework**](win32-installedprogramframework.md).

</dd> <dt>

**Fornitore**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Autore dell'applicazione Win32 installata.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Versione dell'applicazione Win32 installata.

</dd> </dl>

## <a name="requirements"></a>Requisiti



|                                     |                                                                                      |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                           |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                            |
| Spazio dei nomi<br/>                | Root\\CIMv2<br/>                                                               |
| MOF<br/>                      | <dl> <dt>Aeinv.mof</dt> </dl> |



 

 





