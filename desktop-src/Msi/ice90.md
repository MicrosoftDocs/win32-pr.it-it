---
description: ICE90 Invia un avviso se rileva che la directory di un collegamento è stata specificata come proprietà pubblica.
ms.assetid: 47565d9b-c3c2-4a5c-8f91-2b3912a63b47
title: ICE90
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7b4063d06aa5a0a8688e2a411040d4b64f58f75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880869"
---
# <a name="ice90"></a>ICE90

ICE90 Invia un avviso se rileva che la directory di un collegamento è stata specificata come proprietà pubblica. I nomi delle [proprietà pubbliche](public-properties.md) sono scritti in lettere maiuscole. Un collegamento specificato da una proprietà pubblica potrebbe non funzionare se il valore della proprietà [**ALLUSERS**](allusers.md) cambia.

Questa azione personalizzata ICE convalida la tabella dei collegamenti e usa la tabella di directory. Se la tabella di directory non è presente, restituisce senza convalidare la tabella dei collegamenti e non invia alcun errore o avviso.

## <a name="result"></a>Risultato

ICE90 invia il seguente avviso.



| Errore ICE90                                                                                                                                                                                                                    | Descrizione                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| Il collegamento ' \[ 1 \] ' contiene una directory che è una proprietà pubblica (tutti i limiti) ed è sotto la directory del profilo utente. Ciò comporta un problema se il valore della proprietà [**ALLUSERS**](allusers.md) cambia nella sequenza dell'interfaccia utente. | La directory di un collegamento è stata specificata come proprietà pubblica. |



 

## <a name="example"></a>Esempio

ICE90 segnala l'avviso seguente per l'esempio:

``` syntax
The shortcut 'Shortcut1' has a directory that is a public property (ALL CAPS) 
and is under user profile directory. This results in a problem if the value 
of the ALLUSERS property changes in the UI sequence.
```

In questo esempio, MYDIR è in un profilo utente. ICE90 Invia un avviso perché il percorso della directory di destinazione è specificato da una proprietà pubblica, MYDIR. Un utente può modificare la proprietà MYDIR o [**ALLUSERS**](allusers.md) . Se **ALLUSERS** è impostato per il [contesto di installazione](installation-context.md)per computer e mydir è sotto un profilo utenti, il file di collegamento in mydir viene copiato nel profilo "tutti gli utenti" e non in un profilo utente specifico. Se **ALLUSERS** è impostato per il contesto di installazione per utente, il file di collegamento in mydir viene copiato nel profilo di un utente specifico e non è disponibile per altri utenti.

[Tabella collegamenti](shortcut-table.md) (parziale)



| Tasto di scelta rapida  | Directory\_ |
|-----------|-------------|
| Shortcut1 | MYDIR       |



 

[Tabella directory](directory-table.md) (parziale)



| Directory | \_Padre directory |
|-----------|-------------------|
| MYDIR     | ProgramMenuFolder |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



