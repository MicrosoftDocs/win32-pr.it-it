---
description: Restituisce un oggetto RecordList che elenca i componenti installati.
ms.assetid: a91656de-2ebc-45b5-86f8-b13f35c6a762
title: Installer.ComponentsEx - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentsEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1805780c7d21018ec51273b00df88493e25a38dd4525428ba605f8fa9934ceaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118632319"
---
# <a name="installercomponentsex-property"></a>Installer.ComponentsEx - proprietà

Questa proprietà restituisce un [**oggetto RecordList**](recordlist-object.md) che elenca i componenti installati. Questa proprietà chiama [**MsiEnumComponentsEx.**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa)

**[Windows Installer 4.5 o versioni precedenti:](not-supported-in-windows-installer-4-5.md)** Non supportato. Questa proprietà è disponibile a partire da Windows Installer 5.0.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Installer.ComponentsEx
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

[**MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa)
</dt> </dl>

 

 




