---
description: Il metodo ExtractFilesEx dell'oggetto merge estrae il file con estensione cab incorporato da un modulo e quindi scrive tali file nella directory di destinazione.
ms.assetid: 8b063052-4f92-466a-9c52-bda26ed13d5c
title: Metodo merge. ExtractFilesEx (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ExtractFilesEx
- IMsmMerge.ExtractFilesEx
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: be6aa1001be0d3ecd6cbb9c4cd1d8c04b4649f10
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332940"
---
# <a name="mergeextractfilesex-method"></a>Merge. ExtractFilesEx, metodo

Il metodo **ExtractFilesEx** dell'oggetto [**merge**](merge-object.md) estrae il file con estensione cab incorporato da un modulo e quindi scrive tali file nella directory di destinazione.

## <a name="syntax"></a>Sintassi


```JScript
Merge.ExtractFilesEx(
  Path,
  fLongFileNames,
  pFilePaths
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Percorso* 
</dt> <dd>

Directory di destinazione completo.

</dd> <dt>

*fLongFileNames* 
</dt> <dd>

Impostare questa impostazione per specificare l'utilizzo di nomi di file lunghi per i segmenti di percorso e i nomi file finali.

</dd> <dt>

*pFilePaths* 
</dt> <dd>

Si tratta di un elenco di percorsi completi per i file estratti correttamente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Tutti i file nella directory di destinazione con lo stesso nome verranno sovrascritti. Il percorso viene creato se non esiste già.

### <a name="c"></a>C++

Vedere funzione [**ExtractFilesEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-extractfilesex) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Mergemod.dll 2,0 o versione successiva<br/>                                                    |
| Intestazione<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




