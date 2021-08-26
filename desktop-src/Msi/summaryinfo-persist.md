---
description: Il metodo Persist dell'oggetto SummaryInfo formatta e scrive le proprietà archiviate in precedenza nel flusso SummaryInformation standard.
ms.assetid: 77ec1754-73b1-416e-9c9d-72fdbabe16ae
title: Metodo SummaryInfo.Persist
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SummaryInfo.Persist
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 35916dccc3b131d49176b4ecc1a31fedf40c7c5eafeb4c107b30de08db21dc81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039601"
---
# <a name="summaryinfopersist-method"></a>Metodo SummaryInfo.Persist

Il **metodo Persist** dell'oggetto [**SummaryInfo**](summaryinfo-object.md) formatta e scrive le proprietà archiviate in precedenza nel flusso SummaryInformation standard. Genera un errore se il flusso non può essere scritto correttamente. Questo metodo può essere chiamato una sola volta dopo l'impostazione di tutti i valori delle proprietà. Le proprietà possono comunque essere lette dopo la scrittura del flusso.

## <a name="syntax"></a>Sintassi


```JScript
SummaryInfo.Persist()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISummaryInfo è definito come 000C109B-0000-0000-C000-000000000046<br/>                                                                                                                                                                         |



 

 




