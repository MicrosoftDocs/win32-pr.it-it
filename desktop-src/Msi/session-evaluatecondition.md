---
description: Il Metodo EvaluateCondition dell'oggetto Session valuta un'espressione logica che contiene i simboli e i valori. Questo metodo usa la funzione MsiEvaluateCondition.
ms.assetid: 629f7efd-80fe-4a0e-95cc-b62d6258ae0a
title: Session. EvaluateCondition, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.EvaluateCondition
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e6eb207d826b641e9295e4a3fa4fcda16e0b2769
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329107"
---
# <a name="sessionevaluatecondition-method"></a>Session. EvaluateCondition, metodo

Il metodo **EvaluateCondition** dell'oggetto [**Session**](session-object.md) valuta un'espressione logica che contiene i simboli e i valori. Questo metodo usa la funzione [**MsiEvaluateCondition**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona) .

## <a name="syntax"></a>Sintassi


```JScript
Session.EvaluateCondition(
  condition
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*condizione* 
</dt> <dd>

Stringa obbligatoria che contiene l'espressione logica. Per altre informazioni, vedere [sintassi dell'istruzione condizionale](conditional-statement-syntax.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un intero che indica la valutazione della condizione.



| Costante                  | Valore | Descrizione                               |
|---------------------------|-------|-------------------------------------------|
| msiEvaluateConditionFalse | 0     | La condizione restituisce false.         |
| msiEvaluateConditionTrue  | 1     | La condizione restituisce true.          |
| msiEvaluateConditionNone  | 2     | Non è stata specificata un'espressione condizionale. |
| msiEvaluateConditionError | 3     | La condizione contiene un errore di sintassi.    |



 

## <a name="remarks"></a>Commenti

È possibile utilizzare le espressioni condizionali per confrontare gli Stati di funzionalità e componenti. La tabella seguente illustra gli Stati di funzionalità e componenti usati dal metodo EvaluateCondition.



| State                 | Valore | Descrizione                                              |
|-----------------------|-------|----------------------------------------------------------|
| Null                  | Null  | Nessuna azione eseguita sulla funzionalità o sul componente.                 |
| msiInstallStateAbsent | 2     | La funzionalità o il componente non è presente.                     |
| msiInstallStateLocal  | 3     | La funzionalità o il componente è installato nel computer locale. |
| msiInstallStateSource | 4     | La funzionalità o il componente è installato per l'esecuzione dall'origine.    |



 

> [!Note]  
> Gli Stati non vengono impostati fino a quando non viene chiamato il metodo [**SetInstallLevel**](session-setinstalllevel.md) , direttamente o dall' [azione CostFinalize secondo](costfinalize-action.md). Pertanto, il controllo dello stato è utile solo nell'espressione condizionale in una tabella della sequenza di azione.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession è definito come 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi dell'istruzione condizionale](conditional-statement-syntax.md)
</dt> </dl>

 

 




