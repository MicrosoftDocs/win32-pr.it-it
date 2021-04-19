---
description: Controlla il modo in cui WMI crea o aggiorna le classi a seconda dei flag specificati.
ms.assetid: ec535662-be14-44dc-ba0f-f9d2cbf630ea
ms.tgt_platform: multiple
title: pragma classFlags
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pragma
api_type:
- NA
api_location: ''
ms.openlocfilehash: 422185e3b1549d28e6d7004e2032675148d2408e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308841"
---
# <a name="pragma-classflags"></a>pragma classFlags

Il comando per il preprocessore **pragma classFlags** controlla il modo in cui WMI crea o aggiorna le classi a seconda dei flag specificati.

Di seguito viene descritta la sintassi per questo comando:


```mof
#pragma classflags ("[flag1], [flag2]")
```



Il *\[ flag \]* deve essere uno o più degli argomenti seguenti. È possibile combinare eventuali flag che non si contraddicono tra loro.



| Flag        | Descrizione                                                                                                                                                                                                                                                                                                                                                     |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| createonly  | Indica al compilatore di non apportare modifiche alle classi esistenti e di terminare una compilazione se una classe specificata nel file MOF esiste già in WMI.                                                                                                                                                                                                        |
| ForceUpdate | Forza gli aggiornamenti delle classi quando esistono classi figlio in conflitto. Se, ad esempio, si definisce un qualificatore di classe in una classe figlio e la classe di base tenta di aggiungere lo stesso qualificatore, l'utilizzo di questo flag causa la risoluzione del conflitto da parte del compilatore eliminando il qualificatore in conflitto nella classe figlio. Se la classe figlio dispone di istanze, l'aggiornamento avrà esito negativo. |
| safeupdate  | Consente al compilatore di aggiornare le classi anche se esistono classi figlio, se la modifica non provoca conflitti con le classi figlio. Questo flag, ad esempio, consente di aggiungere una nuova proprietà a una classe di base senza dover aggiungere anche la proprietà a una classe figlio preesistente. Se le classi figlio hanno istanze, l'aggiornamento avrà esito negativo.                           |
| UpdateOnly  | Indica al compilatore di non creare nuove classi e fa in modo che il compilatore interrompa la compilazione se non esiste una classe specificata nel file MOF.                                                                                                                                                                                                  |



 

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato come utilizzare questo comando con i flag UpdateOnly e ForceUpdate.


```mof
#pragma classflags ("updateonly", "forceupdate")
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>       |
| Server minimo supportato<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Comandi del preprocessore](preprocessor-commands.md)
</dt> </dl>

 

 




