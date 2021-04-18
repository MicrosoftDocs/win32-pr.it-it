---
description: Il metodo CloseModule dell'oggetto merge chiude il modulo Windows Installer Merge attualmente aperto.
ms.assetid: a11f72cf-4c4e-4650-95f9-549169452622
title: Metodo merge. CloseModule (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.CloseModule
- IMsmMerge.CloseModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 8688ae06cedca1e3b75290f7831f7d3539e3ec21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106323986"
---
# <a name="mergeclosemodule-method"></a>Merge. CloseModule, metodo

Il metodo **CloseModule** dell'oggetto [**merge**](merge-object.md) chiude il modulo Windows Installer Merge attualmente aperto.

## <a name="syntax"></a>Sintassi


```JScript
Merge.CloseModule()
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

La chiusura di un modulo merge non influirà sugli errori che non sono stati recuperati.

### <a name="c"></a>C++

Vedere funzione [**CloseModule**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closemodule) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Mergemod.dll 1,0 o versione successiva<br/>                                                    |
| Intestazione<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
