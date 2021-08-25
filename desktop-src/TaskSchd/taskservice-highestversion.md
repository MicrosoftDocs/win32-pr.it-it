---
title: TaskService.HighestVersion - proprietà
description: Per lo scripting, indica la versione più recente Utilità di pianificazione che un computer supporta.
ms.assetid: b4e55e46-6f33-4224-811b-06bf218dd1ac
keywords:
- Proprietà HighestVersion Utilità di pianificazione
- Proprietà HighestVersion Utilità di pianificazione, oggetto TaskService
- Oggetto TaskService Utilità di pianificazione, proprietà HighestVersion
topic_type:
- apiref
api_name:
- TaskService.HighestVersion
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e27618490fcf404936532d272402bebc03d94eb72ba8156e897f344b708d90ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959491"
---
# <a name="taskservicehighestversion-property"></a>TaskService.HighestVersion - proprietà

Per lo scripting, indica la versione più recente Utilità di pianificazione che un computer supporta.

## <a name="syntax"></a>Sintassi


```VB
TaskService.HighestVersion As Integer
```



## <a name="property-value"></a>Valore proprietà

La versione più recente di Utilità di pianificazione supportata da un computer. La versione più recente è un valore suddiviso in MajorVersion/MinorVersion sul limite a 16 bit. Il Utilità di pianificazione restituisce 1 per la versione principale e 2 per la versione secondaria. Usare la [funzione CLng](/previous-versions//ck4c5842(v=vs.85)) per ottenere il valore intero della proprietà .

## <a name="examples"></a>Esempio

Il codice seguente illustra come usare la [funzione CLng](/previous-versions//ck4c5842(v=vs.85)) per ottenere il valore della **proprietà HighestVersion.**


```VB
wscript.echo service.HighestVersion
Test = clng( service.HighestVersion )
If Test <> 65538  Then
    wscript.echo "Fail"

Else
    wscript.echo "Pass"
End If
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

