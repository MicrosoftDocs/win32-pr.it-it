---
description: Il Metodo Sequence dell'oggetto Session apre una query sulla tabella specificata, ordinando le azioni in base ai numeri nella colonna Sequence.
ms.assetid: cde735b0-0b97-4c4f-adfc-f0321aafb012
title: Metodo Session. Sequence
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Sequence
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 18708b79bdce73b29f46b4d62a15ceb8003d9c9b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333039"
---
# <a name="sessionsequence-method"></a>Metodo Session. Sequence

Il metodo **Sequence** dell'oggetto [**Session**](session-object.md) apre una query sulla tabella specificata, ordinando le azioni in base ai numeri nella colonna Sequence. Per ogni riga recuperata, viene chiamato il metodo [**DoAction**](session-doaction.md) , purché le espressioni di condizione fornite non restituiscono false. Restituisce un msiDoActionStatusEnum di enumerazione, come descritto nel metodo [**DoAction**](session-doaction.md) .

## <a name="syntax"></a>Sintassi


```JScript
Session.Sequence(
  table
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*tabella* 
</dt> <dd>

Nome stringa obbligatorio della tabella da utilizzare per la sequenziazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo in genere viene chiamato internamente dalle azioni di primo livello.

Una sequenza di azione che contiene azioni che aggiornano il sistema, ad esempio le azioni [InstallFiles](installfiles-action.md) e [WriteRegistryValori consente](writeregistryvalues-action.md) , non può essere eseguita chiamando il metodo **Sequence** . L'eccezione a questa regola è rappresentata dal caso in cui il metodo **Sequence** venga chiamato da un'azione personalizzata pianificata nella [tabella InstallExecuteSequence](installexecutesequence-table.md) tra le azioni [InstallInitialize](installinitialize-action.md) e [InstallFinalize](installfinalize-action.md). È possibile chiamare le azioni che non aggiornano il sistema, ad esempio [AppSearch](appsearch-action.md) o [CostInitialize](costinitialize-action.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession è definito come 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




