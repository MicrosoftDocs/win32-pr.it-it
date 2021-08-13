---
description: La proprietà ComponentClients di sola lettura restituisce un oggetto StringList che enumera il set di client di un componente specificato.
ms.assetid: 47553360-298f-4be8-819d-18f4df96667c
title: Installer.ComponentClients - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentClients
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: c94a30247bbfc39675308308457c369785bd9a67413a5b0b62af143e17e2112b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118632713"
---
# <a name="installercomponentclients-property"></a>Installer.ComponentClients - proprietà

La proprietà **ComponentClients di sola lettura** restituisce un [**oggetto StringList**](stringlist-object.md) che enumera il set di client di un componente specificato.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Installer.ComponentClients
```



## <a name="property-value"></a>Valore proprietà

GUID stringa che rappresenta il codice del componente. I codici dei componenti vengono specificati nella colonna ComponentId della [tabella Component](component-table.md).

## <a name="remarks"></a>Commenti

Per enumerare i client del componente, un'applicazione può scorrere [**l'oggetto StringList**](stringlist-object.md) usando un costrutto For Each. Poiché i client non sono ordinati, i nuovi componenti hanno un indice arbitrario. Ciò significa che la funzione può restituire i client in qualsiasi ordine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiEnumClients**](/windows/desktop/api/Msi/nf-msi-msienumclientsa)
</dt> </dl>

 

 




