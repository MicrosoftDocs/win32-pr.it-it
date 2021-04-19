---
description: La proprietà ShortcutTarget dell'oggetto Installer esamina un collegamento e ne restituisce il prodotto, il nome della funzionalità e il componente, se disponibile.
ms.assetid: fd7a1d34-3013-4419-af92-0a0162c93494
title: Proprietà Installer. ShortcutTarget
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ShortcutTarget
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1c53d43188af9ed8f58ddd54916761e346f1bad1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332166"
---
# <a name="installershortcuttarget-property"></a>Proprietà Installer. ShortcutTarget

La proprietà **ShortcutTarget** dell'oggetto [**Installer**](installer-object.md) esamina un collegamento e ne restituisce il prodotto, il nome della funzionalità e il componente, se disponibile.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Installer.ShortcutTarget
```



## <a name="property-value"></a>Valore proprietà

Percorso completo e nome file per il file.

## <a name="remarks"></a>Commenti

ShortcutTarget restituisce un [**oggetto record**](record-object.md) che contiene tre campi:

-   Field 1 è un GUID per il codice prodotto del collegamento, se disponibile. Questo campo può essere null.
-   Il campo 2 è l'ID funzionalità del collegamento, se disponibile. Questo campo può essere null.
-   Il campo 3 è un GUID per il codice componente, se disponibile. Questo campo può essere null.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)
</dt> <dt>

[**MsiGetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)
</dt> </dl>

 

 




