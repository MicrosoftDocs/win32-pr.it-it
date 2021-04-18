---
description: Restituisce un oggetto elenco che elenca i prodotti che utilizzano un componente installato specificato.
ms.assetid: c9756526-68d7-4d04-97e2-56a5eaf816be
title: Proprietà Installer. ClientsEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ClientsEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5a609ab0ba6edc5b0e3e9bbd26bc3539858ebdee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329476"
---
# <a name="installerclientsex-property"></a>Proprietà Installer. ClientsEx

Questa proprietà restituisce un [**oggetto elenco di elementi**](recordlist-object.md) che elenca i prodotti che utilizzano un componente installato specificato. Questa proprietà chiama [**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa).

**[Windows Installer 4,5 o versioni precedenti](not-supported-in-windows-installer-4-5.md):** Non supportato. Questa proprietà è disponibile a partire da Windows Installer 5,0.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Installer.ClientsEx
```



## <a name="property-value"></a>Valore proprietà

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiEnumClientsEx**](/windows/desktop/api/Msi/nf-msi-msienumclientsexa)
</dt> </dl>

 

 




