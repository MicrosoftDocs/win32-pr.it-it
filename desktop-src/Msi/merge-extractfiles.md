---
description: Il metodo ExtractFiles dell'oggetto Merge estrae il file .cab incorporato da un modulo e quindi scrive tali file nella directory di destinazione.
ms.assetid: 846355d6-32f2-4b04-91dc-acd60445fbd9
title: Metodo Merge.ExtractFiles (Advpub.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ExtractFiles
- IMsmMerge.ExtractFiles
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: e56d6572526e2aecfc12dc5b2bb9a365be6d3c53b6fb1707fe197c056d05c377
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926561"
---
# <a name="mergeextractfiles-method"></a>Metodo Merge.ExtractFiles

Il **metodo ExtractFiles** dell'oggetto [**Merge**](merge-object.md) estrae il file .cab incorporato da un modulo e quindi scrive tali file nella directory di destinazione.

## <a name="syntax"></a>Sintassi


```JScript
Merge.ExtractFiles(
  Path
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Percorso* 
</dt> <dd>

Directory di destinazione completa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Tutti i file nella directory di destinazione con lo stesso nome vengono sovrascritti. Il percorso viene creato se non esiste già.

**ExtractFiles estrae** sempre i file usando nomi di file brevi per il percorso. Per usare nomi di file lunghi per il percorso, usare il [**metodo ExtractFilesEx**](merge-extractfilesex.md).

### <a name="c"></a>C++

Vedere [**Funzione ExtractFiles.**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractfiles)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------|
| Versione<br/> | Mergemod.dll 1.0 o versione successiva<br/>                                                                     |
| Intestazione<br/>  | <dl> <dt>Advpub.h (includere Mergemod.h)</dt> </dl> |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl>                  |



 

 
