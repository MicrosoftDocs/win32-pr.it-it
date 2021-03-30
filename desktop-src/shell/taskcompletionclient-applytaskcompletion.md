---
description: Inizia il completamento dell'attività.
ms.assetid: 75C84DD9-D815-45C2-A28E-EAE437EAFF89
title: 'Metodo TaskCompletionClient:: ApplyTaskCompletion'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TaskCompletionClient.ApplyTaskCompletion
api_type:
- COM
api_location:
- ExecModelClient.dll
ms.openlocfilehash: 950d96ac46c18d741d5cf2337326f116fb79e36a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994965"
---
# <a name="taskcompletionclientapplytaskcompletion-method"></a>Metodo TaskCompletionClient:: ApplyTaskCompletion

Inizia il completamento dell'attività.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ApplyTaskCompletion(
    UINT32   ptcfCategory
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ptcfCategory* 
</dt> <dd>

Valore che indica la categoria dell'attività.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

L'unico valore supportato per *ptcfCategory* è 0x08000000.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                    |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2016\]<br/>                                           |
| DLL<br/>                      | <dl> <dt>ExecModelClient.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TaskCompletionClient**](taskcompletionclient.md)
</dt> </dl>

 

 




