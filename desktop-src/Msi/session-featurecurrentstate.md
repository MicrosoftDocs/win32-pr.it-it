---
description: La proprietà FeatureCurrentState dell'oggetto Session è una proprietà di sola lettura che restituisce lo stato di installazione corrente della funzionalità designata. Per i valori di stato, vedere la proprietà FeatureRequestState.
ms.assetid: c4c325dc-6e7e-4009-8707-952c04574170
title: Proprietà Session. FeatureCurrentState
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
ms.openlocfilehash: 47c834571dd211dd085ed94e9d8c1ff9d5516c9e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329105"
---
# <a name="sessionfeaturecurrentstate-property"></a>Proprietà Session. FeatureCurrentState

La proprietà **FeatureCurrentState** dell'oggetto [**Session**](session-object.md) è una proprietà di sola lettura che restituisce lo stato di installazione corrente della funzionalità designata. Per i valori di stato, vedere la proprietà [**FeatureRequestState**](session-featurerequeststate.md) .

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Session.FeatureCurrentState
```



## <a name="property-value"></a>Valore proprietà

Nome della stringa obbligatoria della funzionalità richiesta e una chiave primaria nella tabella delle [funzionalità](feature-table.md).

## <a name="remarks"></a>Commenti

Se la proprietà ha esito negativo, è possibile ottenere informazioni estese sugli errori usando il metodo [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession è definito come 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Sessione**](session-object.md)
</dt> <dt>

[**Proprietà FeatureRequestState**](session-featurerequeststate.md)
</dt> </dl>

 

 




