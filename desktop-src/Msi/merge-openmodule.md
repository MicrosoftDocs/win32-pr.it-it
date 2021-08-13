---
description: Il metodo OpenModule dell'oggetto Merge apre un modulo unione Windows installer in modalità di sola lettura. Un modulo deve essere aperto prima di poter essere unito a un database di installazione.
ms.assetid: fc976899-2c39-4314-b2fb-417e0dfc53b9
title: Metodo Merge.OpenModule (Mergemod.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.OpenModule
- IMsmMerge.OpenModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 4659fbd2c96d883b04e653fc67c6aa3017f16135405f956bf9b4eb78101bb404
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118628727"
---
# <a name="mergeopenmodule-method"></a>Metodo Merge.OpenModule

Il **metodo OpenModule** dell'oggetto [**Merge**](merge-object.md) apre un Windows di merge del programma di installazione in modalità di sola lettura. Un modulo deve essere aperto prima di poter essere unito a un database di installazione.

## <a name="syntax"></a>Sintassi


```JScript
Merge.OpenModule(
  FileName,
  Language
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*FileName* 
</dt> <dd>

Nome file completo che punta a un modulo unione.

</dd> <dt>

*Lingua* 
</dt> <dd>

Identificatore di lingua valido (LANGID).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questa funzione apre il modulo unione in modalità di sola lettura ed esclude la scrittura di altri programmi nel modulo unione fino a quando non viene chiamato il metodo [**CloseModule.**](merge-closemodule.md)

Il programma di installazione tenta di aprire il modulo nella lingua specificata da *Lingua* o in una lingua più generale. Ad esempio, se *language* è specificato come 1033, un modulo con una lingua predefinita di 1033, 9 o 0 può essere aperto nella lingua predefinita. Il *valore Lingua* 9 apre i moduli con una lingua predefinita pari a 9 o 0. Se la lingua predefinita del modulo non soddisfa i requisiti specificati, viene effettuato un tentativo di trasformare il modulo nella lingua richiesta. In caso di errore, il modulo viene trasformato in linguaggi sempre più generali, fino alla lingua neutra. Se nessuna delle trasformazioni ha esito positivo, l'apertura del modulo non riesce. In questo caso, viene aggiunto un errore all'elenco degli errori di tipo msmErrorLanguageUnsupported. Se si verifica un errore durante la trasformazione del modulo nella lingua desiderata, viene aggiunto un errore all'elenco degli errori di tipo msmErrorLanguageFailed. Per informazioni dettagliate, vedere [**la proprietà Type**](error-type.md) dell'oggetto [**Error.**](error-object.md) L'apertura di un modulo unione cancella tutti gli errori che non sono già stati recuperati.

### <a name="c"></a>C++

Vedere [**Funzione OpenModule.**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openmodule)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Mergemod.dll 1.0 o versione successiva<br/>                                                    |
| Intestazione<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
