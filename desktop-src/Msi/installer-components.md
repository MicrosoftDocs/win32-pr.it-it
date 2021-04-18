---
description: La proprietà componenti di sola lettura restituisce un oggetto String enumerando il set di componenti installati per tutti i prodotti.
ms.assetid: c84e4329-428a-440a-bd65-097588a86932
title: Proprietà Installer. Components
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
ms.openlocfilehash: e6767be5182b15836c071bf8b00ed8441f6031dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330498"
---
# <a name="installercomponents-property"></a>Proprietà Installer. Components

La proprietà **componenti** di sola lettura restituisce un oggetto [**String**](stringlist-object.md) enumerando il set di componenti installati per tutti i prodotti.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Installer.Components
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

Per enumerare i componenti, un'applicazione è in grado di scorrere l'oggetto [**String**](stringlist-object.md) con un oggetto per ogni costrutto. Poiché i componenti non sono ordinati, eventuali nuovi componenti hanno un indice arbitrario. Ciò significa che la funzione può restituire componenti in qualsiasi ordine.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiEnumComponents**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsa)
</dt> </dl>

 

 




