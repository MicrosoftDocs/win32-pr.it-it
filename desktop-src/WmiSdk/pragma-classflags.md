---
description: Controlla il modo in cui WMI crea o aggiorna le classi a seconda dei flag specificati.
ms.assetid: ec535662-be14-44dc-ba0f-f9d2cbf630ea
ms.tgt_platform: multiple
title: pragma classflags
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
ms.openlocfilehash: 6fd2b8ec75bd0521ce31af1ee7ce9dba2d9498890f9b5ddc768463f733322cda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996321"
---
# <a name="pragma-classflags"></a>pragma classflags

Il comando del preprocessore **pragma classflags** controlla il modo in cui WMI crea o aggiorna le classi a seconda dei flag specificati.

Di seguito viene descritta la sintassi per questo comando:


```mof
#pragma classflags ("[flag1], [flag2]")
```



*\[ Il \] flag* deve essere uno o più degli argomenti seguenti. È possibile combinare tutti i flag che non si contraddicono tra loro.



| Flag        | Descrizione                                                                                                                                                                                                                                                                                                                                                     |
|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| createonly  | Indica al compilatore di non apportare modifiche alle classi esistenti e termina una compilazione se una classe specificata nel file MOF esiste già in WMI.                                                                                                                                                                                                        |
| Forceupdate | Forza gli aggiornamenti delle classi in caso di classi figlio in conflitto. Ad esempio, se si definisce un qualificatore di classe in una classe figlio e la classe base tenta di aggiungere lo stesso qualificatore, l'uso di questo flag fa sì che il compilatore risolva il conflitto eliminando il qualificatore in conflitto nella classe figlio. Se la classe figlio dispone di istanze, l'aggiornamento ha esito negativo. |
| safeupdate  | Consente al compilatore di aggiornare le classi anche se esistono classi figlio, se la modifica non causa conflitti con le classi figlio. Ad esempio, questo flag consente di aggiungere una nuova proprietà a una classe di base senza dover aggiungere la proprietà a qualsiasi classe figlio preesiste. Se le classi figlio hanno istanze, l'aggiornamento non riesce.                           |
| updateonly  | Indica al compilatore di non creare nuove classi e fa in modo che termini la compilazione se non esiste una classe specificata nel file MOF.                                                                                                                                                                                                  |



 

## <a name="examples"></a>Esempio

L'esempio seguente illustra come usare questo comando con i flag updateonly e forceupdate.


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

[Comandi per il preprocessore](preprocessor-commands.md)
</dt> </dl>

 

 




