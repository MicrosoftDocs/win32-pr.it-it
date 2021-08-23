---
description: La proprietà FeatureCost dell'oggetto Session restituisce la quantità totale di spazio su disco (in unità di 512 byte) richiesta dalla funzionalità specificata e dalle relative funzionalità padre (fino alla radice della tabella Feature).
ms.assetid: 5df9912a-2722-41c8-991b-256a009e85df
title: Session.FeatureCost - proprietà
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
ms.openlocfilehash: 617d1695b8b472952f22737ba3f677d9320f9b4214afc3dea5a9cc5010e2b1a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629291"
---
# <a name="sessionfeaturecost-property"></a>Session.FeatureCost - proprietà

La **proprietà FeatureCost** dell'oggetto [**Session**](session-object.md) restituisce la quantità totale di spazio su disco (in unità di 512 byte) richiesta dalla funzionalità specificata e dalle relative funzionalità padre (fino alla radice della tabella Feature). Per ogni funzionalità, il costo totale è costituito da costi del disco attribuiti a ogni componente collegato alla funzionalità.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Session.FeatureCost
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

Se la proprietà ha esito negativo, è possibile ottenere informazioni estese sull'errore usando il [**metodo LastErrorRecord.**](installer-lasterrorrecord.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession è definito come 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




