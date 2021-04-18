---
description: Il metodo FeatureInfo dell'oggetto Session restituisce un oggetto FeatureInfo che contiene informazioni descrittive per la funzionalità specificata.
ms.assetid: f5391fd4-984e-44cc-8b6c-fd97834e0674
title: Session. FeatureInfo, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 6cb2acd17dd7d07024e0b490beb6d13ad2bafd6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330777"
---
# <a name="sessionfeatureinfo-method"></a>Session. FeatureInfo, metodo

Il metodo **FeatureInfo** dell'oggetto [**Session**](session-object.md) restituisce un oggetto **FeatureInfo** che contiene informazioni descrittive per la funzionalità specificata.

## <a name="syntax"></a>Sintassi


```JScript
Session.FeatureInfo(
  Feature
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Funzionalità* 
</dt> <dd>

Identifica la funzionalità di interesse.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession è definito come 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiGetFeatureInfo**](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa)
</dt> </dl>

 

 




