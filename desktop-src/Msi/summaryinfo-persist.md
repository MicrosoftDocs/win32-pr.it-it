---
description: Il metodo di salvataggio permanente dell'oggetto SummaryInfo formatta e scrive le proprietà archiviate in precedenza nel flusso SummaryInformation standard.
ms.assetid: 77ec1754-73b1-416e-9c9d-72fdbabe16ae
title: SummaryInfo. persevers (metodo)
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
ms.openlocfilehash: e454631e27476e6d18b85908f651d89c2e8063ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329243"
---
# <a name="summaryinfopersist-method"></a>SummaryInfo. persevers (metodo)

Il metodo di **salvataggio permanente** dell'oggetto [**SummaryInfo**](summaryinfo-object.md) formatta e scrive le proprietà archiviate in precedenza nel flusso SummaryInformation standard. Genera un errore se il flusso non può essere scritto correttamente. Questo metodo può essere chiamato solo una volta dopo l'impostazione di tutti i valori delle proprietà. Le proprietà possono essere ancora lette dopo la scrittura del flusso.

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
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISummaryInfo è definito come 000C109B-0000-0000-C000-000000000046<br/>                                                                                                                                                                         |



 

 




