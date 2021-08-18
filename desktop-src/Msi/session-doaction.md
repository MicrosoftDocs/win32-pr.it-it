---
description: Il metodo DoAction dell'oggetto Session esegue la funzione di azione corrispondente al nome fornito.
ms.assetid: 6cff1cf1-1c8f-4c43-a687-e927e8573e55
title: Metodo Session.DoAction (Photoacquire.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.DoAction
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5c3f6451ec6ef920e6c6414a9396d2c4eeb2102ffc161e1ed91ce996752cd345
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629391"
---
# <a name="sessiondoaction-method"></a>Metodo Session.DoAction

Il **metodo DoAction** dell'oggetto [**Session**](session-object.md) esegue la funzione di azione corrispondente al nome fornito. Se viene specificato un nome di azione Null, il motore usa il valore maiuscolo della proprietà [ACTION](action.md) come azione da eseguire. Se non viene definito alcun valore di proprietà, viene eseguita l'azione predefinita, attualmente definita come INSTALL. Questo metodo restituisce un'enumerazione integer.

## <a name="syntax"></a>Sintassi


```JScript
Session.DoAction(
  action
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*action* 
</dt> <dd>

Nome stringa obbligatorio dell'azione da eseguire. Sensitive.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Le azioni che aggiornano il sistema, ad esempio [le azioni InstallFiles](installfiles-action.md) e [WriteRegistryValues,](writeregistryvalues-action.md) non possono essere eseguite chiamando il **metodo DoAction.** L'eccezione a questa regola è se il **metodo DoAction** viene chiamato da un'azione personalizzata pianificata nella tabella [InstallExecuteSequence](installexecutesequence-table.md) tra le [azioni InstallInitialize](installinitialize-action.md) e [InstallFinalize](installfinalize-action.md). È possibile chiamare azioni che non aggiornano il sistema, ad esempio [AppSearch](appsearch-action.md) o [CostInitialize.](costinitialize-action.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| Intestazione<br/>  | <dl> <dt>Photoacquire.h</dt> </dl>                                                                                                                                                               |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID ISession è definito \_ come 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




