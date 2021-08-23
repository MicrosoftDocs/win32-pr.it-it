---
description: La proprietà SummaryInformation dell'oggetto Database restituisce un oggetto SummaryInfo che può essere usato per esaminare, aggiornare e aggiungere proprietà al flusso di informazioni di riepilogo.
ms.assetid: 6892a8c0-c99e-4dcb-b6cb-d470ffceab69
title: Proprietà Database.SummaryInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.SummaryInformation
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cf181b35457b8f4be5737bfa31cf284d86ed21f48800dcab6044cef444a5b640
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947578"
---
# <a name="databasesummaryinformation-property"></a>Proprietà Database.SummaryInformation

La **proprietà SummaryInformation** dell'oggetto [**Database**](database-object.md) restituisce un [**oggetto SummaryInfo**](summaryinfo-object.md) che può essere usato per esaminare, aggiornare e aggiungere proprietà al flusso [di informazioni di riepilogo.](summary-information-stream.md)

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Database.SummaryInformation
```



## <a name="property-value"></a>Valore proprietà

Numero massimo di proprietà da aggiungere o modificare. Questo parametro è obbligatorio e viene usato per allocare memoria di lavoro sufficiente durante la generazione del flusso. Non è necessario archiviare questo numero di proprietà. È necessario usare un valore pari a zero se il database viene aperto in sola lettura per impedire l'aggiornamento del flusso.

## <a name="remarks"></a>Commenti

Se viene usato un valore *maxProperties* maggiore di 0 per aprire un flusso di informazioni di riepilogo esistente, è necessario chiamare il metodo [**Persist**](summaryinfo-persist.md) prima di chiudere l'oggetto. In caso negativo, le informazioni sul flusso esistenti andranno perse.

Se la proprietà ha esito negativo, è possibile ottenere informazioni estese sull'errore usando il [**metodo LastErrorRecord.**](installer-lasterrorrecord.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IDatabase è definito come 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




