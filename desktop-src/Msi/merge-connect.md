---
description: Il metodo Connect dell'oggetto merge connette un modulo a una funzionalità aggiuntiva. Il modulo deve essere già stato Unito nel database o verrà unito al database. La funzionalità deve esistere prima di chiamare questa funzione.
ms.assetid: 1c1ef664-792c-4cdc-b468-1ffe0b7810a5
title: Metodo merge. Connect (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Connect
- IMsmMerge.Connect
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: da66f7dfe4203e80d4778ae9b39c665a66164384
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327322"
---
# <a name="mergeconnect-method"></a>Merge. Connect (metodo)

Il metodo **Connect** dell'oggetto [**merge**](merge-object.md) connette un modulo a una funzionalità aggiuntiva. Il modulo deve essere già stato Unito nel database o verrà unito al database. La funzionalità deve esistere prima di chiamare questa funzione.

Le modifiche apportate al database non vengono salvate su disco a meno che non venga chiamato il metodo [**ChiudiDatabase**](merge-closedatabase.md) con *BCommit* impostato su **true**.

## <a name="syntax"></a>Sintassi


```JScript
Merge.Connect(
  Feature
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Funzionalità* 
</dt> <dd>

Nome di una funzionalità già esistente nel database.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Gli errori possono essere recuperati tramite la proprietà [**Errors**](merge-errors.md) . Gli errori e i messaggi informativi vengono inseriti nel file di log corrente.

### <a name="c"></a>C++

Vedere funzione [**Connect**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-connect) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Mergemod.dll 1,0 o versione successiva<br/>                                                    |
| Intestazione<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
