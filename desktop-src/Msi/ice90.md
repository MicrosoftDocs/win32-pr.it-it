---
description: ICE90 invia un avviso se rileva che la directory di un collegamento è stata specificata come proprietà pubblica.
ms.assetid: 47565d9b-c3c2-4a5c-8f91-2b3912a63b47
title: ICE90
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fba38ba074bf939431f497e8aab73ec0640d7bbc66fb0998498ce190d99fd92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894951"
---
# <a name="ice90"></a>ICE90

ICE90 invia un avviso se rileva che la directory di un collegamento è stata specificata come proprietà pubblica. I nomi [delle proprietà pubbliche](public-properties.md) sono scritti in lettere maiuscole. Un collegamento specificato da una proprietà pubblica potrebbe non funzionare se il valore della proprietà [**ALLUSERS**](allusers.md) cambia.

Questa azione personalizzata ICE convalida la tabella Shortcut e usa la tabella Directory. Se la tabella Directory non è presente, viene restituita senza convalidare la tabella Collegamento e non vengono pubblicati errori o avvisi.

## <a name="result"></a>Risultato

ICE90 pubblica l'avviso seguente.



| Errore ICE90                                                                                                                                                                                                                    | Descrizione                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| Il collegamento ' 1 ' ha una directory che è una proprietà \[ pubblica (ALL CAPS) e si trova \] nella directory del profilo utente. Ciò comporta un problema se il valore della proprietà [**ALLUSERS**](allusers.md) cambia nella sequenza dell'interfaccia utente. | La directory di un collegamento è stata specificata come proprietà pubblica. |



 

## <a name="example"></a>Esempio

ICE90 segnala l'avviso seguente per l'esempio:

``` syntax
The shortcut 'Shortcut1' has a directory that is a public property (ALL CAPS) 
and is under user profile directory. This results in a problem if the value 
of the ALLUSERS property changes in the UI sequence.
```

In questo esempio MYDIR si trova in un profilo utente. ICE90 invia un avviso perché il percorso della directory di destinazione è specificato da una proprietà pubblica, MYDIR. Un utente può modificare la proprietà MYDIR [**o ALLUSERS.**](allusers.md) Se **ALLUSERS** è impostato per il contesto di installazione per computer [e](installation-context.md)MYDIR si trova in un profilo utente, il file di collegamento in MYDIR viene copiato nel profilo "Tutti gli utenti" e non nel profilo di un utente specifico. Se **ALLUSERS è** impostato per il contesto di installazione per utente, il file di collegamento in MYDIR viene copiato nel profilo di un determinato utente e non è disponibile per altri utenti.

[Tabella dei collegamenti](shortcut-table.md) (parziale)



| Tasto di scelta rapida  | Directory\_ |
|-----------|-------------|
| Collegamento1 | MYDIR       |



 

[Tabella directory](directory-table.md) (parziale)



| Directory | Directory \_ Parent |
|-----------|-------------------|
| MYDIR     | CartellaMenu Programma |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



