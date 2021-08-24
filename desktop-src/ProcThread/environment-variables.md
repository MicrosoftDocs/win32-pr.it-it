---
description: 'Ogni processo ha un blocco di ambiente che contiene un set di variabili di ambiente e i relativi valori. Esistono due tipi di variabili di ambiente: variabili di ambiente utente (impostate per ogni utente) e variabili di ambiente di sistema (impostate per tutti gli utenti).'
ms.assetid: 6732b12f-ced1-4769-b947-79da8fd2237a
title: Variabili di ambiente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 647c685aac8ed6df36c0312d7eef49793fd4b2bbfca5576e0377e59da31dd777
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910321"
---
# <a name="environment-variables"></a>Variabili di ambiente

Ogni processo ha un blocco di ambiente che contiene un set di variabili di ambiente e i relativi valori. Esistono due tipi di variabili di ambiente: variabili di ambiente utente (impostate per ogni utente) e variabili di ambiente di sistema (impostate per tutti gli utenti).

Per impostazione predefinita, un processo figlio eredita le variabili di ambiente del processo padre. I programmi avviati dal processore dei comandi ereditano le variabili di ambiente del processore dei comandi. Per specificare un ambiente diverso per un processo figlio, creare un nuovo blocco di ambiente e passarne un puntatore come parametro alla [**funzione CreateProcess.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)

Il processore dei comandi fornisce **il comando set** per visualizzare il blocco di ambiente o per creare nuove variabili di ambiente. È anche possibile visualizzare o modificare  le variabili di ambiente selezionando Sistema dal Pannello di controllo **,** selezionando Impostazioni di sistema avanzate **e** facendo clic su Variabili **di ambiente**.

Ogni blocco di ambiente contiene le variabili di ambiente nel formato seguente:<dl> *Var1* = *Valore1* \\ 0  
*Var2* = *Valore2* \\ 0  
*Var3* = *Valore3* \\ 0  
...  
*VarN* = *ValoreN* \\ 0 \\ 0  
</dl>

Il nome di una variabile di ambiente non può includere un segno di uguale (=).

La [**funzione GetEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-getenvironmentstrings) restituisce un puntatore al blocco di ambiente del processo chiamante. Deve essere considerato come un blocco di sola lettura. non modificarlo direttamente. Usare invece la [**funzione SetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-setenvironmentvariable) per modificare una variabile di ambiente. Al termine del blocco di ambiente ottenuto da **GetEnvironmentStrings,** chiamare la funzione [**FreeEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-freeenvironmentstringsa) per liberare il blocco.

La [**chiamata a SetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-setenvironmentvariable) non ha alcun effetto sulle variabili di ambiente di sistema. Per aggiungere o modificare variabili di ambiente di sistema a livello di codice, aggiungerle alla chiave del Registro di sistema **HKEY \_ LOCAL MACHINE System \_ \\ \\ CurrentControlSet \\ Control Session Manager \\ \\ Environment** , quindi trasmettere un messaggio [**WM \_ SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) con *lParam* impostato sulla stringa "Environment". In questo modo le applicazioni, ad esempio la shell, possono prelevare gli aggiornamenti.

La dimensione massima di una variabile di ambiente definita dall'utente è di 32.767 caratteri. Non esiste alcuna limitazione tecnica alle dimensioni del blocco di ambiente. Esistono tuttavia limiti pratici a seconda del meccanismo usato per accedere al blocco. Ad esempio, un file batch non può impostare una variabile più lunga della lunghezza massima della riga di comando.

**Windows Server 2003 e Windows XP:** La dimensione massima del blocco di ambiente per il processo è di 32.767 caratteri. A partire Windows Vista e Windows Server 2008, non esiste alcuna limitazione tecnica sulle dimensioni del blocco di ambiente.

La [**funzione GetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-getenvironmentvariable) determina se una variabile specificata è definita nell'ambiente del processo chiamante e, in tal caso, qual è il relativo valore.

Per recuperare una copia del blocco di ambiente per un determinato utente, usare la [**funzione CreateEnvironmentBlock.**](/windows/win32/api/userenv/nf-userenv-createenvironmentblock)

Per espandere le stringhe delle variabili di ambiente, usare [**la funzione ExpandEnvironmentStrings.**](/windows/desktop/api/processenv/nf-processenv-expandenvironmentstringsa)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modifica delle variabili di ambiente](changing-environment-variables.md)
</dt> <dt>

[Variabili di ambiente utente](../shell/user-environment-variables.md)
</dt> </dl>

 

 
