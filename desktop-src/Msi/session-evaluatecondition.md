---
description: Il metodo EvaluateCondition dell'oggetto Session valuta un'espressione logica che contiene simboli e valori. Questo metodo usa la funzione MsiEvaluateCondition.
ms.assetid: 629f7efd-80fe-4a0e-95cc-b62d6258ae0a
title: Metodo Session.EvaluateCondition
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
ms.openlocfilehash: fa5807314092c6245c23a329deb44a644ed54b22640292a06e08a9944f54e4dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629331"
---
# <a name="sessionevaluatecondition-method"></a>Metodo Session.EvaluateCondition

Il **metodo EvaluateCondition** dell'oggetto [**Session**](session-object.md) valuta un'espressione logica che contiene simboli e valori. Questo metodo usa la [**funzione MsiEvaluateCondition.**](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona)

## <a name="syntax"></a>Sintassi


```JScript
Session.EvaluateCondition(
  condition
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Condizione* 
</dt> <dd>

Stringa obbligatoria che contiene l'espressione logica. Per altre informazioni, vedere [Sintassi di istruzioni condizionali](conditional-statement-syntax.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce un numero intero che indica la valutazione della condizione.



| Costante                  | Valore | Descrizione                               |
|---------------------------|-------|-------------------------------------------|
| msiEvaluateConditionFalse | 0     | La condizione restituisce false.         |
| msiEvaluateConditionTrue  | 1     | La condizione restituisce true.          |
| msiEvaluateConditionNone  | 2     | Non viene fornita un'espressione condizionale. |
| msiEvaluateConditionError | 3     | La condizione contiene un errore di sintassi.    |



 

## <a name="remarks"></a>Commenti

Le espressioni condizionali possono essere usate per confrontare gli stati delle funzionalità e dei componenti. La tabella seguente illustra gli stati della funzionalità e del componente utilizzati dal metodo EvaluateCondition.



| State                 | Valore | Descrizione                                              |
|-----------------------|-------|----------------------------------------------------------|
| Null                  | Null  | Nessuna azione eseguita sulla funzionalità o sul componente.                 |
| msiInstallStateAbsent | 2     | La funzionalità o il componente non è presente.                     |
| msiInstallStateLocal  | 3     | La funzionalità o il componente viene installato nel computer locale. |
| msiInstallStateSource | 4     | La funzionalità o il componente viene installato per l'esecuzione dall'origine.    |



 

> [!Note]  
> Gli stati non vengono impostati fino a quando non viene chiamato il [**metodo SetInstallLevel,**](session-setinstalllevel.md) direttamente o tramite [l'azione CostFinalize](costfinalize-action.md). Pertanto, il controllo dello stato è utile solo in un'espressione condizionale in una tabella della sequenza di azioni.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID ISession è definito \_ come 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Sintassi di istruzioni condizionali](conditional-statement-syntax.md)
</dt> </dl>

 

 




