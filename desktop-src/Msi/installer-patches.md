---
description: La proprietà Patches di sola lettura dell'oggetto Installer restituisce un oggetto StringList che contiene tutte le patch applicate al prodotto.
ms.assetid: a8d46073-399b-480e-b4b0-a7a2f832e160
title: Installer.Patches - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Patches
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 33576b92924493a99c058196639faa34f5b42e388b9e30b6e300c17444ddeeff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119430781"
---
# <a name="installerpatches-property"></a>Installer.Patches - proprietà

La proprietà **Patches di sola lettura** dell'oggetto [**Installer**](installer-object.md) restituisce un [**oggetto StringList**](stringlist-object.md) che contiene tutte le patch applicate al prodotto.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Installer.Patches
```



## <a name="property-value"></a>Valore proprietà

Specifica il codice prodotto.

## <a name="remarks"></a>Commenti

Per enumerare le patch, un'applicazione scorre [**l'oggetto StringList**](stringlist-object.md) usando un costrutto For Each. Poiché le patch non sono ordinate, le nuove patch hanno un indice arbitrario. Ciò significa che la funzione può restituire patch in qualsiasi ordine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiEnumPatches**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
</dt> </dl>

 

 




