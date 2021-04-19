---
description: La proprietà SummaryInformation dell'oggetto di database restituisce un oggetto SummaryInfo che può essere utilizzato per esaminare, aggiornare e aggiungere proprietà al flusso di informazioni di riepilogo.
ms.assetid: 6892a8c0-c99e-4dcb-b6cb-d470ffceab69
title: Proprietà database. SummaryInformation
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
ms.openlocfilehash: 524c4fa2fe5014436f122f0a5460aced820e30ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333055"
---
# <a name="databasesummaryinformation-property"></a>Proprietà database. SummaryInformation

La proprietà **SummaryInformation** dell'oggetto di [**database**](database-object.md) restituisce un oggetto [**SummaryInfo**](summaryinfo-object.md) che può essere utilizzato per esaminare, aggiornare e aggiungere proprietà al flusso di [informazioni di riepilogo](summary-information-stream.md).

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Database.SummaryInformation
```



## <a name="property-value"></a>Valore proprietà

Numero massimo di proprietà da aggiungere o modificare. Questo parametro è obbligatorio e viene utilizzato per allocare memoria di lavoro sufficiente durante la generazione del flusso. Non è necessario archiviare questo numero di proprietà. Se il database è aperto in sola lettura per impedire l'aggiornamento del flusso, è necessario utilizzare un valore pari a zero.

## <a name="remarks"></a>Commenti

Se viene usato un valore di *maxProperties* maggiore di 0 per aprire un flusso di informazioni di riepilogo esistente, è necessario chiamare il metodo di [**salvataggio permanente**](summaryinfo-persist.md) prima di chiudere l'oggetto. In caso contrario, le informazioni sul flusso esistenti andranno perse.

Se la proprietà ha esito negativo, è possibile ottenere informazioni estese sugli errori usando il metodo [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iDatabase è definito come 000C109D-0000-0000-C000-000000000046<br/>                                                                                                                                                                            |



 

 




