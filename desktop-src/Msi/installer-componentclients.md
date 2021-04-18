---
description: La proprietà ComponentClients di sola lettura restituisce un oggetto String enumerando il set di client di un componente specificato.
ms.assetid: 47553360-298f-4be8-819d-18f4df96667c
title: Proprietà Installer. ComponentClients
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
ms.openlocfilehash: 2241babae283f367a15c8f742b51af280ed1a3b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329028"
---
# <a name="installercomponentclients-property"></a>Proprietà Installer. ComponentClients

La proprietà **ComponentClients** di sola lettura restituisce un oggetto [**String**](stringlist-object.md) enumerando il set di client di un componente specificato.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Installer.ComponentClients
```



## <a name="property-value"></a>Valore proprietà

GUID di stringa che rappresenta il codice componente del componente. I codici dei componenti vengono specificati nella colonna ComponentId della [tabella Component](component-table.md).

## <a name="remarks"></a>Commenti

Per enumerare i client del componente, un'applicazione può eseguire l'iterazione dell'oggetto [**String**](stringlist-object.md) con un oggetto per ogni costrutto. Poiché i client non sono ordinati, eventuali nuovi componenti hanno un indice arbitrario. Ciò significa che la funzione può restituire client in qualsiasi ordine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiEnumClients**](/windows/desktop/api/Msi/nf-msi-msienumclientsa)
</dt> </dl>

 

 




