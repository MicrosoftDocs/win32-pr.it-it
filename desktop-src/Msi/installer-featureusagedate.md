---
description: La proprietà FeatureUsageDate è una proprietà di sola lettura che restituisce la data dell'ultima utilizzo della funzionalità specificata.
ms.assetid: 444e54b2-94e7-44ea-8d7b-eeac984e3715
title: Installer.FeatureUsageDate - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.FeatureUsageDate
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 15c628b95f6dab2d671e660c9783e071e1e4385c165363fdf9ad39abd571510e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118631068"
---
# <a name="installerfeatureusagedate-property"></a>Installer.FeatureUsageDate - proprietà

La **proprietà FeatureUsageDate** è una proprietà di sola lettura che restituisce la data dell'ultima utilizzo della funzionalità specificata.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Installer.FeatureUsageDate
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

L'uso [**dei metodi UseFeature**](installer-usefeature.md), [**ProvideComponent**](installer-providecomponent.md) o [**ProvideQualifiedComponent**](installer-providequalifiedcomponent.md) o dei relativi equivalenti api nella funzionalità specificata imposta questa proprietà.

La data è nel formato di data MS-DOS, come illustrato nella tabella seguente.



| BITS | Contenuto                                            |
|------|-----------------------------------------------------|
| 0-4  | Giorno del mese (1-31)                             |
| 5-8  | Mese (1 = gennaio, 2 = febbraio e così via)        |
| 9-15 | Offset dell'anno rispetto al 1980 (aggiunta del 1980 per ottenere l'anno effettivo) |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiGetFeatureUsage**](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea)
</dt> </dl>

 

 




