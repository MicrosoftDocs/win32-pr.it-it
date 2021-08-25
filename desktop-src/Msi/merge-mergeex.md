---
description: Il metodo MergeEx dell'oggetto Merge equivale alla funzione Merge, con la differenza che accetta un argomento aggiuntivo.
ms.assetid: 83b6d62b-d176-42ac-b513-d1c2e562965c
title: Metodo Merge.MergeEx (Mergemod.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.MergeEx
- IMsmMerge.MergeEx
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 7e683597d78e568e6bfec9b59241fe45f922c5346ef83f427598ad0a7c59dcac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926531"
---
# <a name="mergemergeex-method"></a>Metodo Merge.MergeEx

Il **metodo MergeEx** dell'oggetto [**Merge**](merge-object.md) equivale alla [**funzione Merge,**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) con la differenza che accetta un argomento aggiuntivo. *L'argomento pConfiguration* è un'interfaccia implementata dal client. L'argomento può essere Null. La presenza di questo argomento indica che il client è in grado di supportare la funzionalità di configurazione, ma non obbliga il client a fornire dati di configurazione per qualsiasi elemento configurabile specifico.

Il [**metodo Merge**](merge-merge.md) esegue un'unione del database corrente e del modulo corrente. L'unione collega i componenti del modulo alla funzionalità identificata dalla *funzionalità*. La radice dell'albero delle directory del modulo viene reindirizzata al percorso specificato da *RedirectDir.*

## <a name="syntax"></a>Sintassi


```JScript
Merge.MergeEx(
  Feature,
  RedirectDir,
  pConfiguration
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Funzionalità* 
</dt> <dd>

Nome di una funzionalità nel database.

</dd> <dt>

*RedirectDir* 
</dt> <dd>

Chiave di una voce nella [tabella Directory](directory-table.md) del database. Questo parametro può essere Null o una stringa vuota.

</dd> <dt>

*pConfiguration* 
</dt> <dd>

*L'argomento pConfiguration* è un'interfaccia implementata dal client. L'argomento può essere Null. La presenza di questo argomento indica che il client è in grado di supportare la funzionalità di configurazione, ma non obbliga il client a fornire dati di configurazione per qualsiasi elemento configurabile specifico.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Al termine dell'unione, i componenti del modulo vengono collegati alla funzionalità identificata dalla *funzionalità*. Questa funzionalità non viene creata e deve essere una funzionalità esistente. Il modulo può essere collegato a funzionalità aggiuntive usando il [**Connessione**](merge-connect.md) metodo .

Le modifiche apportate al database vengono salvate se e solo se il [**metodo CloseDatabase**](merge-closedatabase.md) viene chiamato con *bCommit* impostato su **TRUE.**

Se si verificano conflitti di merge, incluse le esclusioni, vengono inseriti nell'enumeratore degli errori per un successivo recupero, ma non causano l'esito negativo del merge. Gli errori possono essere recuperati tramite la [**proprietà**](merge-errors.md) Errors. Gli errori e i messaggi informativi vengono inviati al file di log corrente.

Quando l'unione ha esito negativo a causa di una configurazione del modulo non corretta, la [**funzione MergeEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex) restituisce E \_ FAIL. Sono inclusi questi errori msmErrorType: **msmErrorBadNullSubstitution**, **msmErrorBadSubstitutionType**, **msmErrorBadNullResponse**, **msmErrorMissingConfigItem** e **msmErrorDataRequestFailed**. Questi errori causano l'arresto immediato dell'unione quando viene rilevato l'errore. L'oggetto errore viene ancora aggiunto all'enumeratore quando **MergeEx** restituisce E \_ FAIL. Per altre informazioni sugli errori msmErrorType, vedere [**Get \_ Type Function (Error Object)**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_type). Tutti gli altri errori **causano la restituzione** di S FALSE da parte di MergeEx \_ e la continuazione dell'unione.

### <a name="c"></a>C++

Vedere [**La funzione MergeEx.**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Mergemod.dll 2.0 o versione successiva<br/>                                                    |
| Intestazione<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
