---
description: Il metodo ChiudiDatabase dell'oggetto merge chiude il database Windows Installer attualmente aperto.
ms.assetid: a89fe77a-0099-4c49-b484-c05ee351a66a
title: Metodo merge. ChiudiDatabase (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.CloseDatabase
- IMsmMerge.CloseDatabase
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 5df72b9423ad212264736d16db0ae73ded9afef5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323988"
---
# <a name="mergeclosedatabase-method"></a>Merge. ChiudiDatabase, metodo

Il metodo **ChiudiDatabase** dell'oggetto [**merge**](merge-object.md) chiude il database Windows Installer attualmente aperto.

## <a name="syntax"></a>Sintassi


```JScript
Merge.CloseDatabase(
  bCommit
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*bCommit* 
</dt> <dd>

**True** se le modifiche devono essere salvate; in caso contrario, **false** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

La chiusura di un database Cancella tutte le informazioni sulle dipendenze, ma non influisce sugli errori che non sono stati recuperati.

### <a name="c"></a>C++

Vedere funzione [**ChiudiDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Mergemod.dll 1,0 o versione successiva<br/>                                                    |
| Intestazione<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
