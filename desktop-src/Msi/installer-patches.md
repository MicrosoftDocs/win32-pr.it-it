---
description: La proprietà patch di sola lettura dell'oggetto Installer restituisce un oggetto String che contiene tutte le patch applicate al prodotto.
ms.assetid: a8d46073-399b-480e-b4b0-a7a2f832e160
title: Proprietà Installer. Patches
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
ms.openlocfilehash: fd94c5853b3e455cf4d814dfb3c4078705ac727b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332176"
---
# <a name="installerpatches-property"></a>Proprietà Installer. Patches

La proprietà **patch** di sola lettura dell'oggetto [**Installer**](installer-object.md) restituisce un oggetto [**String**](stringlist-object.md) che contiene tutte le patch applicate al prodotto.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Installer.Patches
```



## <a name="property-value"></a>Valore proprietà

Specifica il codice del prodotto.

## <a name="remarks"></a>Commenti

Per enumerare le patch, un'applicazione esegue l'iterazione dell'oggetto [**String**](stringlist-object.md) con un oggetto per ogni costrutto. Poiché le patch non sono ordinate, tutte le nuove patch hanno un indice arbitrario. Ciò significa che la funzione può restituire le patch in qualsiasi ordine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiEnumPatches**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
</dt> </dl>

 

 




