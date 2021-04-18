---
description: Il Metodo OpenLog dell'oggetto merge apre un file di log che riceve i messaggi di stato e di errore. Se il file di log esiste già, il programma di installazione aggiunge nuovi messaggi. Se il file di log non esiste, il programma di installazione crea un file di log.
ms.assetid: 97d01ea3-43b6-4529-9706-97b3b0132d9c
title: Metodo merge. OpenLog (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.OpenLog
- IMsmMerge.OpenLog
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 46dc029c88b44540817e93e1e559829d88b9f62b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333980"
---
# <a name="mergeopenlog-method"></a>Merge. OpenLog, metodo

Il metodo **OpenLog** dell'oggetto [**merge**](merge-object.md) apre un file di log che riceve i messaggi di stato e di errore. Se il file di log esiste già, il programma di installazione aggiunge nuovi messaggi. Se il file di log non esiste, il programma di installazione crea un file di log.

## <a name="syntax"></a>Sintassi


```JScript
Merge.OpenLog(
  Filename
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Filename* 
</dt> <dd>

Nome file completo che punta a un file da aprire o creare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

I client possono inviare i propri messaggi a questo file di log tramite il metodo [**log**](merge-log.md) .

### <a name="c"></a>C++

Vedere funzione [**OpenLog**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openlog) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Mergemod.dll 1,0 o versione successiva<br/>                                                    |
| Intestazione<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
