---
description: Il metodo Merge dell'oggetto Merge esegue un'unione del database corrente e del modulo corrente.
ms.assetid: 4b580b1f-5071-42f1-8022-a152817f9fdc
title: Metodo Merge.Merge (Mergemod.h)
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
ms.openlocfilehash: 43644f8ef19b81331f9f2d88d4dac03d654379d51174a50e994d3642cb86eabc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117804731"
---
# <a name="mergemerge-method"></a>Metodo Merge.Merge

Il **metodo Merge** dell'oggetto [**Merge**](merge-object.md) esegue un'unione del database corrente e del modulo corrente. L'unione collega i componenti del modulo alla funzionalità identificata dalla *funzionalità*. La radice dell'albero di directory del modulo viene reindirizzata al percorso specificato da *RedirectDir.*

Il **metodo Merge** può essere chiamato una sola volta per unire una particolare combinazione di .msi file con estensione msm.

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

Chiave di una voce nella [tabella Directory](directory-table.md) del database. Questo parametro può essere Null o una stringa vuota.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Al termine dell'unione, i componenti del modulo vengono collegati alla funzionalità identificata dalla *funzionalità*. Questa funzionalità non viene creata e deve essere una funzionalità esistente. Si noti che **il metodo Merge** ottiene tutti i riferimenti alle funzionalità nel modulo e sostituisce il riferimento alla funzionalità per tutte le occorrenze del GUID Null nel database del modulo. Per altre informazioni, vedere [Referencing Features in Merge Modules](referencing-features-in-merge-modules.md).

Il modulo può essere collegato a funzionalità aggiuntive usando [**Connessione**](merge-connect.md) metodo . Si noti che la chiamata **Connessione** metodo crea solo associazioni funzionalità-componente. Non modifica le righe che sono già state unite nel database.

Le modifiche apportate al database vengono salvate solo se il [**metodo CloseDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase) viene chiamato con *bCommit* impostato su **TRUE.**

Se si verificano conflitti di merge, incluse le esclusioni, vengono inseriti nell'enumeratore degli errori per un successivo recupero, ma non causano l'esito negativo dell'unione. Gli errori possono essere recuperati tramite la [**proprietà**](error-object.md) Errors. Gli errori e i messaggi informativi vengono inviati al file di log corrente.

### <a name="c"></a>C++

Vedere [**Funzione Merge.**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | Mergemod.dll 1.0 o versione successiva<br/>                                                    |
| Intestazione<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
