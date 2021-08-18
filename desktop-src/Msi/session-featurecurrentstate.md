---
description: La proprietà FeatureCurrentState dell'oggetto Session è una proprietà di sola lettura che restituisce lo stato corrente installato della funzionalità designata. Per i valori di stato, vedere la proprietà FeatureRequestState.
ms.assetid: c4c325dc-6e7e-4009-8707-952c04574170
title: Session.FeatureCurrentState - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureCurrentState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3738a33d2c7a855abe6cc60139286b3e9c4d586bc6c2d9d436390fc5e52f4fd1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629231"
---
# <a name="sessionfeaturecurrentstate-property"></a>Session.FeatureCurrentState - proprietà

La **proprietà FeatureCurrentState** dell'oggetto [**Session**](session-object.md) è una proprietà di sola lettura che restituisce lo stato corrente installato della funzionalità designata. Per i valori di stato, vedere la [**proprietà FeatureRequestState.**](session-featurerequeststate.md)

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Session.FeatureCurrentState
```



## <a name="property-value"></a>Valore proprietà

Nome stringa obbligatorio della funzionalità richiesta e una chiave primaria nella [tabella funzionalità](feature-table.md).

## <a name="remarks"></a>Commenti

Se la proprietà ha esito negativo, è possibile ottenere informazioni estese sull'errore usando il [**metodo LastErrorRecord.**](installer-lasterrorrecord.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID ISession è definito \_ come 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Sessione**](session-object.md)
</dt> <dt>

[**Proprietà FeatureRequestState**](session-featurerequeststate.md)
</dt> </dl>

 

 




