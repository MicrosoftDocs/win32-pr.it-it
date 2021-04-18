---
description: Il metodo ApriModulo dell'oggetto merge apre un modulo Windows Installer Merge in modalità di sola lettura. Prima di poter eseguire il merge di un modulo con un database di installazione, è necessario aprirlo.
ms.assetid: fc976899-2c39-4314-b2fb-417e0dfc53b9
title: Metodo merge. ApriModulo (Mergemod. h)
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
ms.openlocfilehash: 9d83a9331c91817f70c49ecf74c7171c5e627be6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333976"
---
# <a name="mergeopenmodule-method"></a>Merge. ApriModulo, metodo

Il metodo **ApriModulo** dell'oggetto [**merge**](merge-object.md) apre un modulo Windows Installer Merge in modalità di sola lettura. Prima di poter eseguire il merge di un modulo con un database di installazione, è necessario aprirlo.

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

Nome file completo che punta a un modulo merge.

</dd> <dt>

*Lingua* 
</dt> <dd>

Identificatore di lingua valido (LANGID).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questa funzione apre il modulo merge in modalità di sola lettura ed esclude altri programmi da scrivere nel modulo merge fino a quando non viene chiamato il metodo [**CloseModule**](merge-closemodule.md) .

Il programma di installazione tenta di aprire il modulo nella lingua specificata dalla *lingua* o in una lingua più generale. Se, ad esempio, il *linguaggio* viene specificato come 1033, nella lingua predefinita è possibile aprire un modulo con la lingua predefinita 1033, 9 o 0. Un valore di *lingua* 9 apre i moduli con la lingua predefinita 9 o 0. Se la lingua predefinita del modulo non soddisfa i requisiti specificati, viene effettuato un tentativo di trasformare il modulo nella lingua richiesta. Se l'operazione ha esito negativo, il modulo viene trasformato in linguaggi sempre più generali, fino alla lingua neutra. Se nessuna delle trasformazioni ha esito positivo, non è possibile aprire il modulo. In questo caso, viene aggiunto un errore all'elenco errori di tipo msmErrorLanguageUnsupported. Se si verifica un errore durante la trasformazione del modulo nella lingua desiderata, viene aggiunto un errore all'elenco errori di tipo msmErrorLanguageFailed. Per informazioni dettagliate, vedere la proprietà [**Type**](error-type.md) dell'oggetto [**Error**](error-object.md) . L'apertura di un modulo merge Cancella tutti gli errori che non sono stati ancora recuperati.

### <a name="c"></a>C++

Vedere funzione [**ApriModulo**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openmodule) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Mergemod.dll 1,0 o versione successiva<br/>                                                    |
| Intestazione<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
