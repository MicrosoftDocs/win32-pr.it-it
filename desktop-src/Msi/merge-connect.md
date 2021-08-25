---
description: Il Connessione dell'oggetto Merge connette un modulo a una funzionalità aggiuntiva. Il modulo deve essere già stato unito nel database o verrà unito al database. La funzionalità deve esistere prima di chiamare questa funzione.
ms.assetid: 1c1ef664-792c-4cdc-b468-1ffe0b7810a5
title: Unione. Connessione metodo (Mergemod.h)
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
ms.openlocfilehash: c28aafaac9f8224ea4f622b2e63f81d9dc458d72e98c6e22c348087794e9e7a5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926671"
---
# <a name="mergeconnect-method"></a>Unione. Connessione metodo

Il **Connessione** metodo dell'oggetto [**Merge**](merge-object.md) connette un modulo a una funzionalità aggiuntiva. Il modulo deve essere già stato unito nel database o verrà unito al database. La funzionalità deve esistere prima di chiamare questa funzione.

Le modifiche apportate al database non vengono salvate su disco a meno che il [**metodo CloseDatabase**](merge-closedatabase.md) non venga chiamato con *bCommit* impostato su **TRUE.**

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

Gli errori possono essere recuperati tramite la [**proprietà**](merge-errors.md) Errors. Gli errori e i messaggi informativi vengono inviati al file di log corrente.

### <a name="c"></a>C++

Vedere [**Connessione**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-connect) funzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Mergemod.dll 1.0 o versione successiva<br/>                                                    |
| Intestazione<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
