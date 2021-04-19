---
description: La proprietà ComponentQualifiers è una proprietà di sola lettura che restituisce un oggetto String enumerando il set di qualificatori registrati per il componente specificato.
ms.assetid: 49b16c9a-ce84-42ff-af1d-f4ecf7dbe23a
title: Proprietà Installer. ComponentQualifiers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentQualifiers
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 0e6f58850974eaa2021578f0d56015ea0ef6d9e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329024"
---
# <a name="installercomponentqualifiers-property"></a>Proprietà Installer. ComponentQualifiers

La proprietà **ComponentQualifiers** è una proprietà di sola lettura che restituisce un oggetto [**String**](stringlist-object.md) enumerando il set di qualificatori registrati per il componente specificato.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Installer.ComponentQualifiers
```



## <a name="property-value"></a>Valore proprietà

GUID di stringa che rappresenta la categoria di [componenti](publishcomponent-table.md).

## <a name="remarks"></a>Commenti

Per enumerare i qualificatori, l'applicazione esegue l'iterazione dell'oggetto [**String**](stringlist-object.md) con un oggetto per ogni costrutto. Poiché i qualificatori non sono ordinati, qualsiasi nuovo qualificatore dispone di un indice arbitrario, ovvero la funzione può restituire qualificatori in qualsiasi ordine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)
</dt> </dl>

 

 




