---
description: La proprietà ShortcutTarget dell'oggetto Installer esamina un collegamento e restituisce il prodotto, il nome della funzionalità e il componente, se disponibile.
ms.assetid: fd7a1d34-3013-4419-af92-0a0162c93494
title: Proprietà Installer.ShortcutTarget
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
ms.openlocfilehash: b54e334314c0bfd0fb721b175d0a14894d8a509ea02ff36e324903bb1fdbffaf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894001"
---
# <a name="installershortcuttarget-property"></a>Proprietà Installer.ShortcutTarget

La **proprietà ShortcutTarget** dell'oggetto [**Installer**](installer-object.md) esamina un collegamento e restituisce il prodotto, il nome della funzionalità e il componente, se disponibile.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Installer.ShortcutTarget
```



## <a name="property-value"></a>Valore proprietà

Percorso completo e nome del file.

## <a name="remarks"></a>Commenti

ShortcutTarget restituisce un [**oggetto Record**](record-object.md) che contiene tre campi:

-   Il campo 1 è un GUID per il codice prodotto del collegamento, se disponibile. Questo campo può essere Null.
-   Il campo 2 è l'ID funzionalità del collegamento, se disponibile. Questo campo può essere Null.
-   Il campo 3 è un GUID per il codice del componente, se disponibile. Questo campo può essere Null.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IInstaller è definito come \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiGetFeatureState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)
</dt> <dt>

[**MsiGetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)
</dt> </dl>

 

 




