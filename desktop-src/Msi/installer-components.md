---
description: La proprietà Components di sola lettura restituisce un oggetto StringList che enumera il set di componenti installati per tutti i prodotti.
ms.assetid: c84e4329-428a-440a-bd65-097588a86932
title: Installer.Components - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Components
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b8538e594ed02a1bc355ed4cf57db1befb1443e58d7afe2038b16e08eb9e4659
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118632409"
---
# <a name="installercomponents-property"></a>Installer.Components - proprietà

La proprietà **Components** di sola lettura restituisce un [**oggetto StringList**](stringlist-object.md) che enumera il set di componenti installati per tutti i prodotti.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Installer.Components
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

Per enumerare i componenti, un'applicazione può scorrere [**l'oggetto StringList**](stringlist-object.md) usando un costrutto For Each. Poiché i componenti non sono ordinati, tutti i nuovi componenti hanno un indice arbitrario. Ciò significa che la funzione può restituire componenti in qualsiasi ordine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiEnumComponents**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa)
</dt> </dl>

 

 




