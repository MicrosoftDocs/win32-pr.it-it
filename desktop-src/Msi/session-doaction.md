---
description: Il metodo DoAction dell'oggetto Session esegue la funzione Action corrispondente al nome fornito.
ms.assetid: 6cff1cf1-1c8f-4c43-a687-e927e8573e55
title: Metodo Session. DoAction (fotoacquire. h)
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
ms.openlocfilehash: 3084cfd51e7efbcfbfbc3cbcf2c9be21d8373d21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329108"
---
# <a name="sessiondoaction-method"></a>Session. DoAction, metodo

Il metodo **DoAction** dell'oggetto [**Session**](session-object.md) esegue la funzione Action corrispondente al nome fornito. Se viene fornito un nome di azione null, il motore utilizzerà il valore in maiuscolo della [proprietà Action](action.md) come azione da eseguire. Se non viene definito alcun valore della proprietà, viene eseguita l'azione predefinita, attualmente definita come INSTALL. Questo metodo restituisce un'enumerazione Integer.

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

Nome stringa obbligatorio dell'azione da eseguire. Distinzione tra maiuscole e minuscole.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Le azioni che aggiornano il sistema, ad esempio le azioni [InstallFiles](installfiles-action.md) e [WriteRegistryValori consente](writeregistryvalues-action.md) , non possono essere eseguite chiamando il metodo **DoAction** . L'eccezione a questa regola è rappresentata dal caso in cui il metodo **DoAction** viene chiamato da un'azione personalizzata pianificata nella [tabella InstallExecuteSequence](installexecutesequence-table.md) tra le azioni [InstallInitialize](installinitialize-action.md) e [InstallFinalize](installfinalize-action.md). È possibile chiamare le azioni che non aggiornano il sistema, ad esempio [AppSearch](appsearch-action.md) o [CostInitialize](costinitialize-action.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| Intestazione<br/>  | <dl> <dt>Fotoacquisisci. h</dt> </dl>                                                                                                                                                               |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession è definito come 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




