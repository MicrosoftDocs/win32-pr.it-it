---
description: La proprietà FeatureCost dell'oggetto Session restituisce la quantità totale di spazio su disco, in unità di 512 byte, richiesta dalla funzionalità specificata e dalle relative funzionalità padre (fino alla radice della tabella delle funzionalità).
ms.assetid: 5df9912a-2722-41c8-991b-256a009e85df
title: Proprietà Session. FeatureCost
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureCost
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 25c93ce0b3b4efa91a827217d221546e8bab5744
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329106"
---
# <a name="sessionfeaturecost-property"></a>Proprietà Session. FeatureCost

La proprietà **FeatureCost** dell'oggetto [**Session**](session-object.md) restituisce la quantità totale di spazio su disco, in unità di 512 byte, richiesta dalla funzionalità specificata e dalle relative funzionalità padre (fino alla radice della tabella delle funzionalità). Per ogni funzionalità, il costo totale è costituito dai costi del disco attribuiti a ogni componente collegato alla funzionalità.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Session.FeatureCost
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

Se la proprietà ha esito negativo, è possibile ottenere informazioni estese sugli errori usando il metodo [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession è definito come 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




