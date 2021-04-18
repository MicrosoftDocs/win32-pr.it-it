---
description: Il metodo commit dell'oggetto di database finalizza il form persistente del database.
ms.assetid: 39253ccd-08f1-4a6f-87cb-3678ae5221a4
title: Metodo database. commit
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.Commit
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d62c998a70e0a4a036695be10b2bf1d983044241
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331612"
---
# <a name="databasecommit-method"></a>Metodo database. commit

Il metodo **commit** dell'oggetto di [**database**](database-object.md) finalizza il form persistente del database. Tutti i dati persistenti vengono scritti nel database scrivibile e non vengono scritte colonne o righe temporanee. Questo metodo non ha alcun effetto su un database aperto in sola lettura. Questo metodo può essere chiamato più volte per salvare lo stato corrente delle tabelle caricate in memoria. Quando il database viene chiuso, viene eseguito il rollback di tutte le modifiche apportate successivamente all'ultimo **commit** . Questo metodo viene in genere chiamato prima dell'arresto quando tutte le modifiche al database sono state finalizzate.

## <a name="syntax"></a>Sintassi


```JScript
Database.Commit()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se il metodo ha esito negativo, è possibile ottenere informazioni estese sull'errore usando il metodo [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iDatabase è definito come 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




