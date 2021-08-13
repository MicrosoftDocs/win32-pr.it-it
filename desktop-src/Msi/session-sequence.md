---
description: Il metodo Sequence dell'oggetto Session apre una query sulla tabella specificata, ordinando le azioni in base ai numeri nella colonna Sequenza.
ms.assetid: cde735b0-0b97-4c4f-adfc-f0321aafb012
title: Metodo Session.Sequence
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
ms.openlocfilehash: 59e9bb09e66ad9a7bff51f1ce2e7e15750749d04a4d2f2c92365b78b29b34585
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625119"
---
# <a name="sessionsequence-method"></a>Metodo Session.Sequence

Il **metodo Sequence** [**dell'oggetto Session**](session-object.md) apre una query sulla tabella specificata, ordinando le azioni in base ai numeri nella colonna Sequenza. Per ogni riga recuperata, viene chiamato il metodo [**DoAction,**](session-doaction.md) a condizione che qualsiasi espressione di condizione fornita non restituirà False. Restituisce un'enumerazione msiDoActionStatusEnum, come descritto nel [**metodo DoAction.**](session-doaction.md)

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

Nome stringa obbligatorio della tabella da usare per la sequenziazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo viene in genere chiamato internamente dalle azioni di primo livello.

Una sequenza di azioni contenente azioni che aggiornano il sistema, ad esempio le azioni [InstallFiles](installfiles-action.md) e [WriteRegistryValues,](writeregistryvalues-action.md) non può essere eseguita chiamando il **metodo Sequence.** L'eccezione a questa regola è se il metodo **Sequence** viene chiamato da un'azione personalizzata pianificata nella tabella [InstallExecuteSequence](installexecutesequence-table.md) tra le azioni [InstallInitialize](installinitialize-action.md) e [InstallFinalize](installfinalize-action.md). È possibile chiamare azioni che non aggiornano il sistema, ad esempio [AppSearch](appsearch-action.md) o [CostInitialize.](costinitialize-action.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession è definito come 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




