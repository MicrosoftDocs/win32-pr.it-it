---
description: Il metodo ExtractFiles dell'oggetto merge estrae il file con estensione cab incorporato da un modulo e quindi scrive tali file nella directory di destinazione.
ms.assetid: 846355d6-32f2-4b04-91dc-acd60445fbd9
title: Metodo merge. ExtractFiles (Advpub. h)
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
ms.openlocfilehash: 3869dc37b841d386891eb70940054bd78805bf94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327805"
---
# <a name="mergeextractfiles-method"></a>Merge. ExtractFiles, metodo

Il metodo **ExtractFiles** dell'oggetto [**merge**](merge-object.md) estrae il file con estensione cab incorporato da un modulo e quindi scrive tali file nella directory di destinazione.

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

Directory di destinazione completo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Tutti i file nella directory di destinazione con lo stesso nome verranno sovrascritti. Il percorso viene creato se non esiste già.

**ExtractFiles** estrae sempre i file usando nomi di file brevi per il percorso. Per usare nomi di file lunghi per il percorso, usare il [**Metodo ExtractFilesEx**](merge-extractfilesex.md).

### <a name="c"></a>C++

Vedere funzione [**ExtractFiles**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractfiles) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------------|
| Versione<br/> | Mergemod.dll 1,0 o versione successiva<br/>                                                                     |
| Intestazione<br/>  | <dl> <dt>Advpub. h (include Mergemod. h)</dt> </dl> |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl>                  |



 

 
