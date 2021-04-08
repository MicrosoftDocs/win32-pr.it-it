---
title: Proprietà TaskService. HighestVersion
description: Per gli script, indica la versione più recente di Utilità di pianificazione supportata da un computer.
ms.assetid: b4e55e46-6f33-4224-811b-06bf218dd1ac
keywords:
- Utilità di pianificazione proprietà HighestVersion
- Utilità di pianificazione proprietà HighestVersion, oggetto TaskService
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
ms.openlocfilehash: 9b4e381326ab901fcaf8657975ce3f8401facd44
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743735"
---
# <a name="taskservicehighestversion-property"></a>Proprietà TaskService. HighestVersion

Per gli script, indica la versione più recente di Utilità di pianificazione supportata da un computer.

## <a name="syntax"></a>Sintassi


```VB
TaskService.HighestVersion As Integer
```



## <a name="property-value"></a>Valore proprietà

La versione più recente di Utilità di pianificazione supportata da un computer. La versione più recente è un valore suddiviso in MajorVersion/MinorVersion sul limite a 16 bit. Il servizio Utilità di pianificazione restituisce 1 per la versione principale e 2 per la versione secondaria. Usare la funzione [CLng](/previous-versions//ck4c5842(v=vs.85)) per ottenere il valore intero della proprietà.

## <a name="examples"></a>Esempio

Nel codice seguente viene illustrato come utilizzare la funzione [CLng](/previous-versions//ck4c5842(v=vs.85)) per ottenere il valore della proprietà **HighestVersion** .


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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

