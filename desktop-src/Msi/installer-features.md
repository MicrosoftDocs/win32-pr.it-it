---
description: La proprietà Features è una proprietà di sola lettura che restituisce un oggetto StringList che enumera il set di funzionalità pubblicate per il prodotto specificato.
ms.assetid: feb8f09a-fa97-4fee-9082-8f04288af22f
title: Installer.Features - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.Features
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e31dfe2c487a151280a10c4fa7222c005f94c0eeb4ac4f3f5145d67ab600fe9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118631473"
---
# <a name="installerfeatures-property"></a>Installer.Features - proprietà

La **proprietà Features** è una proprietà di sola lettura che restituisce un oggetto [**StringList**](stringlist-object.md) che enumera il set di funzionalità pubblicate per il prodotto specificato.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Installer.Features
```



## <a name="property-value"></a>Valore proprietà

Specifica il codice prodotto del prodotto.

## <a name="remarks"></a>Commenti

Per enumerare le funzionalità, un'applicazione scorre [**l'oggetto StringList**](stringlist-object.md) usando un costrutto For Each. Poiché le funzionalità non sono ordinate, qualsiasi nuova funzionalità ha un indice arbitrario, vale a dire che la funzione può restituire caratteristiche in qualsiasi ordine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa)
</dt> <dt>

[Funzioni di stato del sistema](installer-function-reference.md)
</dt> </dl>

 

 




