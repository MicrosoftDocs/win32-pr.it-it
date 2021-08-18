---
description: Il metodo CreateSourceImage dell'oggetto Merge consente al client di estrarre i file da un modulo a un'immagine di origine su disco dopo un'unione, tenendo conto delle modifiche al modulo che potrebbero essere state apportate durante la configurazione del modulo.
ms.assetid: c3e3465a-d5a7-4fcc-b26a-5a8c763c23d9
title: Metodo Merge.CreateSourceImage (Mergemod.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.CreateSourceImage
- IMsmMerge.CreateSourceImage
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 3e50fca7adaeced7f6f2130aeb86cf1ee74db18ae505575c8ce37b1bb85a4010
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926641"
---
# <a name="mergecreatesourceimage-method"></a>Metodo Merge.CreateSourceImage

Il **metodo CreateSourceImage** dell'oggetto [**Merge**](merge-object.md) consente al client di estrarre i file da un modulo a un'immagine di origine su disco dopo un'unione, tenendo conto delle modifiche al modulo che potrebbero essere state apportate durante la configurazione del modulo. L'elenco dei file da estrarre viene ricavato dalla tabella file del modulo durante il processo di unione. L'elenco di file è costituito da ogni file copiato correttamente dalla tabella file del modulo al database di destinazione. Le voci della tabella file che non sono state copiate a causa di conflitti di chiave primaria con le righe esistenti nel database non fanno parte di questo elenco. Al momento della creazione dell'immagine, la directory per ognuno di questi file proviene dal database aperto (post-unione). Il percorso specificato nel *parametro Path* è la radice dell'immagine di origine per l'installazione. *fLongFileNames* determina se i nomi di file lunghi vengono usati sia per i segmenti di percorso che per i nomi di file finali. La funzione ha esito negativo se non è aperto alcun database, non è aperto alcun modulo o non è stato eseguito alcun merge.

## <a name="syntax"></a>Sintassi


```JScript
Merge.CreateSourceImage(
  Path,
  fLongFileNames,
  pFilePaths
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Percorso* 
</dt> <dd>

Percorso della radice dell'immagine di origine per l'installazione.

</dd> <dt>

*fLongFileNames* 
</dt> <dd>

*fLongFileNames* determina se i nomi di file lunghi vengono usati sia per i segmenti di percorso che per i nomi di file finali.

</dd> <dt>

*pFilePaths* 
</dt> <dd>

Si tratta di un elenco di percorsi completi per i file estratti correttamente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Tutti i file nella directory di destinazione con lo stesso nome vengono sovrascritti. Il percorso viene creato se non esiste già.

### <a name="c"></a>C++

Vedere [**La funzione CreateSourceImage.**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-createsourceimage)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Mergemod.dll 2.0 o versione successiva<br/>                                                    |
| Intestazione<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




