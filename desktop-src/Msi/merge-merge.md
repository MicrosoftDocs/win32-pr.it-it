---
description: Il metodo Merge dell'oggetto merge esegue un'Unione del database corrente e del modulo corrente.
ms.assetid: 4b580b1f-5071-42f1-8022-a152817f9fdc
title: Metodo merge. Merge (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Merge
- IMsmMerge.Merge
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: f33a0ba8218ae38d8fb31cefb6910f5b2c16484d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332261"
---
# <a name="mergemerge-method"></a>Merge. Merge (metodo)

Il metodo **merge** dell'oggetto [**merge**](merge-object.md) esegue un'Unione del database corrente e del modulo corrente. Il merge collega i componenti del modulo alla funzionalità identificata dalla *funzionalità*. La radice dell'albero di directory del modulo viene reindirizzata alla posizione specificata da *RedirectDir*.

Il metodo **merge** può essere chiamato una sola volta per unire una determinata combinazione di file con estensione msi e MSM.

## <a name="syntax"></a>Sintassi


```JScript
Merge.Merge(
  Feature,
  RedirectDir
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

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Una volta completata l'Unione, i componenti del modulo vengono collegati alla funzionalità identificata dalla *funzionalità*. Questa funzionalità non è stata creata e deve essere una funzionalità esistente. Si noti che il metodo **merge** ottiene tutti i riferimenti alle funzionalità nel modulo e sostituisce il riferimento alla funzionalità per tutte le occorrenze del GUID null nel database del modulo. Per altre informazioni, vedere [riferimento alle funzionalità nei moduli merge](referencing-features-in-merge-modules.md).

Il modulo può essere collegato a funzionalità aggiuntive usando il metodo [**Connect**](merge-connect.md) . Si noti che la chiamata al metodo **Connect** crea solo associazioni di componenti di funzionalità. Non modifica le righe che sono già state unite nel database.

Le modifiche apportate al database vengono salvate solo se viene chiamato il metodo [**ChiudiDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase) con *BCommit* impostato su **true**.

Se si verificano conflitti di merge, incluse le esclusioni, vengono inseriti nell'enumeratore Error per il recupero successivo, ma non determina l'esito negativo dell'operazione di merge. Gli errori possono essere recuperati tramite la proprietà [**Errors**](error-object.md) . Gli errori e i messaggi informativi vengono inseriti nel file di log corrente.

### <a name="c"></a>C++

Vedere funzione [**merge**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Mergemod.dll 1,0 o versione successiva<br/>                                                    |
| Intestazione<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
