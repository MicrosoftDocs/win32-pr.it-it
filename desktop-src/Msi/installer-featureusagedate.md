---
description: La proprietà FeatureUsageDate è una proprietà di sola lettura che restituisce la data dell'ultima utilizzo della funzionalità specificata.
ms.assetid: 444e54b2-94e7-44ea-8d7b-eeac984e3715
title: Proprietà Installer. FeatureUsageDate
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
ms.openlocfilehash: b393f9a24b9d1ebeb82de86d26483f703d7854c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324630"
---
# <a name="installerfeatureusagedate-property"></a>Proprietà Installer. FeatureUsageDate

La proprietà **FeatureUsageDate** è una proprietà di sola lettura che restituisce la data dell'ultima utilizzo della funzionalità specificata.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Installer.FeatureUsageDate
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

L'uso dei metodi [**UseFeature**](installer-usefeature.md), [**ProvideComponent**](installer-providecomponent.md) o [**ProvideQualifiedComponent**](installer-providequalifiedcomponent.md) o i relativi equivalenti API nella funzionalità specificata consente di impostare questa proprietà.

La data è nel formato di data MS-DOS, come illustrato nella tabella seguente.



| BITS | Contenuto                                            |
|------|-----------------------------------------------------|
| 0-4  | Giorno del mese (1-31)                             |
| 5-8  | Month (1 = gennaio, 2 = febbraio e così via)        |
| 9-15 | Offset anno da 1980 (aggiungere 1980 per ottenere l'anno effettivo) |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiGetFeatureUsage**](/windows/desktop/api/Msi/nf-msi-msigetfeatureusagea)
</dt> </dl>

 

 




