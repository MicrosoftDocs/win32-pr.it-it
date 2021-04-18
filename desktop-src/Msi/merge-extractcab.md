---
description: Il metodo ExtractCAB dell'oggetto merge estrae il file con estensione cab incorporato da un modulo e lo salva come file specificato. Il programma di installazione crea questo file se non esiste già e sovrascritto, se esistente.
ms.assetid: a6fe8b69-8f4a-45f7-b7e6-7620a00500bb
title: Metodo merge. ExtractCAB (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ExtractCAB
- IMsmMerge.ExtractCAB
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: d0bdc79fb0087456d035bf732faca384b35b2a9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324918"
---
# <a name="mergeextractcab-method"></a>Merge. ExtractCAB, metodo

Il metodo **ExtractCAB** dell'oggetto [**merge**](merge-object.md) estrae il file con estensione cab incorporato da un modulo e lo salva come file specificato. Il programma di installazione crea questo file se non esiste già e sovrascritto, se esistente.

## <a name="syntax"></a>Sintassi


```JScript
Merge.ExtractCAB(
  FileName
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*FileName* 
</dt> <dd>

Il file di destinazione completo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="c"></a>C++

Vedere funzione [**ExtractCAB**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractcab) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Mergemod.dll 1,0 o versione successiva<br/>                                                    |
| Intestazione<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
