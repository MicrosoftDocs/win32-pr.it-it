---
description: Il metodo CreateSourceImage dell'oggetto merge consente al client di estrarre i file da un modulo in un'immagine di origine su disco dopo un'operazione di merge, tenendo conto delle modifiche apportate al modulo che potrebbero essere state apportate durante la configurazione del modulo.
ms.assetid: c3e3465a-d5a7-4fcc-b26a-5a8c763c23d9
title: Metodo merge. CreateSourceImage (Mergemod. h)
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
ms.openlocfilehash: e8d9365a69ff6f33c2989e9102bac7c9c22166aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327807"
---
# <a name="mergecreatesourceimage-method"></a>Merge. CreateSourceImage, metodo

Il metodo **CreateSourceImage** dell'oggetto [**merge**](merge-object.md) consente al client di estrarre i file da un modulo in un'immagine di origine su disco dopo un'operazione di merge, tenendo conto delle modifiche apportate al modulo che potrebbero essere state apportate durante la configurazione del modulo. L'elenco di file da estrarre viene ricavato dalla tabella file del modulo durante il processo di merge. L'elenco dei file è costituito da tutti i file copiati correttamente dalla tabella file del modulo al database di destinazione. Le voci della tabella di file non copiate a causa di conflitti di chiave primaria con le righe esistenti nel database non fanno parte di questo elenco. Al momento della creazione dell'immagine, la directory per ognuno di questi file deriva dal database aperto (post-merge). Il percorso specificato nel parametro *path* è la radice dell'immagine di origine per l'installazione. *fLongFileNames* determina se i nomi di file lunghi vengono usati sia per i segmenti di percorso che per i nomi di file finali. La funzione ha esito negativo se non è aperto alcun database, non è aperto alcun modulo oppure non è stata eseguita alcuna operazione di merge.

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

Tutti i file nella directory di destinazione con lo stesso nome verranno sovrascritti. Il percorso viene creato se non esiste già.

### <a name="c"></a>C++

Vedere funzione [**CreateSourceImage**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-createsourceimage) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Mergemod.dll 2,0 o versione successiva<br/>                                                    |
| Intestazione<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




