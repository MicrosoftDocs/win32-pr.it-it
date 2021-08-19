---
description: Il metodo CloseDatabase dell'oggetto Merge chiude il database Windows Installer.
ms.assetid: a89fe77a-0099-4c49-b484-c05ee351a66a
title: Metodo Merge.CloseDatabase (Mergemod.h)
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
ms.openlocfilehash: 3f3b250cbaebd565f14ef7f10cd8180e497f20347d00a7e96a74298d3e5dc770
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119013029"
---
# <a name="mergeclosedatabase-method"></a>Metodo Merge.CloseDatabase

Il **metodo CloseDatabase** dell'oggetto [**Merge**](merge-object.md) chiude il database Windows Installer.

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

**TRUE se** le modifiche devono essere salvate, **FALSE in caso contrario.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

La chiusura di un database cancella tutte le informazioni sulle dipendenze, ma non influisce sugli errori che non sono stati recuperati.

### <a name="c"></a>C++

Vedere [**Funzione CloseDatabase.**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Mergemod.dll 1.0 o versione successiva<br/>                                                    |
| Intestazione<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
