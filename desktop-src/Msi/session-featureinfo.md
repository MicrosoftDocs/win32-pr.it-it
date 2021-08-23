---
description: Il metodo FeatureInfo dell'oggetto Session restituisce un oggetto FeatureInfo contenente informazioni descrittive per la funzionalità specificata.
ms.assetid: f5391fd4-984e-44cc-8b6c-fd97834e0674
title: Metodo Session.FeatureInfo
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
ms.openlocfilehash: b4d6e44a16305d4a46525cfed631068ff0137c642b09b8dc6a9eca169a104548
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625199"
---
# <a name="sessionfeatureinfo-method"></a>Metodo Session.FeatureInfo

Il **metodo FeatureInfo** dell'oggetto [**Session**](session-object.md) restituisce un **oggetto FeatureInfo** contenente informazioni descrittive per la funzionalità specificata.

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
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID ISession è definito \_ come 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiGetFeatureInfo**](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa)
</dt> </dl>

 

 




