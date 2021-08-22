---
description: Restituisce un oggetto RecordList che fornisce il percorso completo di un componente installato specificato.
ms.assetid: 0f4f9d21-f1cc-44fd-a22f-1b6f055fef9e
title: Installer.ComponentPathEx - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentPathEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 720b10c75fcdf4a6b72f22a72d3b0860fc6089403385b0a951127f56286b6953
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118632616"
---
# <a name="installercomponentpathex-property"></a>Installer.ComponentPathEx - proprietà

Questa proprietà restituisce un [**oggetto RecordList**](recordlist-object.md) che fornisce il percorso completo di un componente installato specificato. Questa proprietà chiama [**MsiGetComponentPathEx.**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa)

**[Windows Installer 4.5 o versioni precedenti:](not-supported-in-windows-installer-4-5.md)** Non supportato. Questa proprietà è disponibile a partire da Windows Installer 5.0.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Installer.ComponentPathEx
```



## <a name="property-value"></a>Valore proprietà

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa)
</dt> </dl>

 

 




