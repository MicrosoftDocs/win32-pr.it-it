---
description: Il metodo MergeEx dell'oggetto merge è equivalente alla funzione Merge, ad eccezione del fatto che accetta un argomento aggiuntivo.
ms.assetid: 83b6d62b-d176-42ac-b513-d1c2e562965c
title: Metodo merge. MergeEx (Mergemod. h)
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
ms.openlocfilehash: 12accfcbc87877300b803ae90d8c924802410e9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326374"
---
# <a name="mergemergeex-method"></a>Merge. MergeEx, metodo

Il metodo **MergeEx** dell'oggetto [**merge**](merge-object.md) è equivalente alla funzione [**merge**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) , ad eccezione del fatto che accetta un argomento aggiuntivo. L'argomento *pConfiguration* è un'interfaccia implementata dal client. L'argomento può essere null. La presenza di questo argomento indica che il client è in grado di supportare la funzionalità di configurazione, ma non obbliga il client a fornire i dati di configurazione per un elemento configurabile specifico.

Il metodo [**merge**](merge-merge.md) esegue un'Unione del database corrente e del modulo corrente. Il merge collega i componenti del modulo alla funzionalità identificata dalla *funzionalità*. La radice dell'albero di directory del modulo viene reindirizzata alla posizione specificata da *RedirectDir*.

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

Chiave di una voce nella tabella di [directory](directory-table.md) del database. Questo parametro può essere null o una stringa vuota.

</dd> <dt>

*pConfiguration* 
</dt> <dd>

L'argomento *pConfiguration* è un'interfaccia implementata dal client. L'argomento può essere null. La presenza di questo argomento indica che il client è in grado di supportare la funzionalità di configurazione, ma non obbliga il client a fornire i dati di configurazione per un elemento configurabile specifico.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Una volta completata l'Unione, i componenti del modulo vengono collegati alla funzionalità identificata dalla *funzionalità*. Questa funzionalità non è stata creata e deve essere una funzionalità esistente. Il modulo può essere collegato a funzionalità aggiuntive usando il metodo [**Connect**](merge-connect.md) .

Le modifiche apportate al database vengono salvate solo se viene chiamato il metodo [**ChiudiDatabase**](merge-closedatabase.md) con *BCommit* impostato su **true**.

Se si verificano conflitti di merge, incluse le esclusioni, vengono inseriti nell'enumeratore Error per il recupero successivo, ma non determina l'esito negativo dell'operazione di merge. Gli errori possono essere recuperati tramite la proprietà [**Errors**](merge-errors.md) . Gli errori e i messaggi informativi vengono inseriti nel file di log corrente.

Quando l'Unione non riesce a causa di una configurazione errata del modulo, la funzione [**MergeEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex) restituisce E ha \_ esito negativo. Sono inclusi gli errori msmErrorType seguenti: **msmErrorBadNullSubstitution**, **msmErrorBadSubstitutionType**, **msmErrorBadNullResponse**, **msmErrorMissingConfigItem** e **msmErrorDataRequestFailed**. Questi errori comportano l'arresto immediato dell'Unione quando viene rilevato l'errore. L'oggetto Error viene ancora aggiunto all'enumeratore quando **MergeEx** restituisce E ha \_ esito negativo. Per ulteriori informazioni sugli errori msmErrorType, vedere [**get \_ Type function (Error Object)**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_type). Tutti gli altri errori provocano la restituzione di false da parte di **MergeEx** \_ e la continuazione del merge.

### <a name="c"></a>C++

Vedere funzione [**MergeEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Mergemod.dll 2,0 o versione successiva<br/>                                                    |
| Intestazione<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
