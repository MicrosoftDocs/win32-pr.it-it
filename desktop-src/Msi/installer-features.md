---
description: La proprietà features è una proprietà di sola lettura che restituisce un oggetto String enumerando il set di funzionalità pubblicate per il prodotto specificato.
ms.assetid: feb8f09a-fa97-4fee-9082-8f04288af22f
title: Proprietà Installer. Features
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
ms.openlocfilehash: 4f63ce80249fb8bd24d70f92e72c44420a13d798
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324638"
---
# <a name="installerfeatures-property"></a>Proprietà Installer. Features

La proprietà **features** è una proprietà di sola lettura che restituisce un oggetto [**String**](stringlist-object.md) enumerando il set di funzionalità pubblicate per il prodotto specificato.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Installer.Features
```



## <a name="property-value"></a>Valore proprietà

Specifica il codice del prodotto.

## <a name="remarks"></a>Commenti

Per enumerare le funzionalità, un'applicazione esegue l'iterazione dell'oggetto [**String**](stringlist-object.md) con un oggetto per ogni costrutto. Poiché le funzionalità non sono ordinate, qualsiasi nuova funzionalità dispone di un indice arbitrario, ovvero la funzione può restituire le funzionalità in qualsiasi ordine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiEnumFeatures**](/windows/desktop/api/Msi/nf-msi-msienumfeaturesa)
</dt> <dt>

[Funzioni di stato del sistema](installer-function-reference.md)
</dt> </dl>

 

 




