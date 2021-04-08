---
title: Proprietà Principal. DisplayName
description: Per lo scripting, ottiene o imposta il nome dell'entità.
ms.assetid: 73caf263-f597-4bea-ae89-32f9919d7a70
keywords:
- Proprietà DisplayName Utilità di pianificazione
- Utilità di pianificazione proprietà DisplayName, oggetto Principal
- Utilità di pianificazione oggetto Principal, proprietà DisplayName
topic_type:
- apiref
api_name:
- Principal.DisplayName
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31a76ec9473bccb20ec484259ab8adfe26ad6441
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741874"
---
# <a name="principaldisplayname-property"></a>Proprietà Principal. DisplayName

Per lo scripting, ottiene o imposta il nome dell'entità.

## <a name="syntax"></a>Sintassi


```VB
Principal.DisplayName As String
```



## <a name="property-value"></a>Valore proprietà

Nome dell'entità.

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML per un'attività, il nome visualizzato per un'entità viene specificato nell'elemento [**DisplayName**](taskschedulerschema-displayname-principaltype-element.md) dello schema utilità di pianificazione.

Quando si imposta il valore di questa proprietà, il valore può essere un testo recuperato da un file Resource. dll. Una stringa specializzata viene utilizzata per fare riferimento al testo dal file di risorse. Il formato della stringa è $ (@ \[ dll \] , \[ resourceId \] ) in cui \[ dll \] è il percorso del file con estensione dll che contiene la risorsa e \[ resourceId \] è l'identificatore per il testo della risorsa. Se ad esempio si imposta il valore di questa proprietà su $ (@% SystemRoot% \\ system32 \\ResourceName.dll,-101), la proprietà verrà impostata sul valore del testo della risorsa con un identificatore uguale a-101 nel file% SystemRoot% \\ system32 \\ResourceName.dll.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> <dt>

[**Principale**](principal.md)
</dt> </dl>

 

 





