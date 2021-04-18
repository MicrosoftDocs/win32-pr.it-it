---
description: 'Ogni processo dispone di un blocco di ambiente che contiene un set di variabili di ambiente e i relativi valori. Esistono due tipi di variabili di ambiente: le variabili di ambiente utente (impostate per ogni utente) e le variabili di ambiente di sistema (impostate per Everyone).'
ms.assetid: 6732b12f-ced1-4769-b947-79da8fd2237a
title: Variabili di ambiente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f50226d12286d01c77025d1cc38e33e2778392a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311989"
---
# <a name="environment-variables"></a>Variabili di ambiente

Ogni processo dispone di un blocco di ambiente che contiene un set di variabili di ambiente e i relativi valori. Esistono due tipi di variabili di ambiente: le variabili di ambiente utente (impostate per ogni utente) e le variabili di ambiente di sistema (impostate per Everyone).

Per impostazione predefinita, un processo figlio eredita le variabili di ambiente del processo padre. I programmi avviati dal processore dei comandi ereditano le variabili di ambiente del processore dei comandi. Per specificare un ambiente diverso per un processo figlio, creare un nuovo blocco di ambiente e passarvi un puntatore come parametro alla funzione [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) .

Il processore dei comandi fornisce il comando **set** per visualizzare il relativo blocco di ambiente o per creare nuove variabili di ambiente. È anche possibile visualizzare o modificare le variabili di ambiente selezionando **sistema** dal **Pannello di controllo**, selezionando **impostazioni di sistema avanzate** e facendo clic su **variabili di ambiente**.

Ogni blocco di ambiente contiene le variabili di ambiente nel formato seguente:<dl> *Var1* = *Value1* \\ 0  
*Var2* = *Value2* \\ 0  
*Var3* = *Valore3* \\ 0  
...  
*VarN* = *Valore di* \\ 0 \\ 0  
</dl>

Il nome di una variabile di ambiente non può includere un segno di uguale (=).

La funzione [**GetEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-getenvironmentstrings) restituisce un puntatore al blocco dell'ambiente del processo chiamante. Questa operazione deve essere considerata come un blocco di sola lettura. non modificarla direttamente. Usare invece la funzione [**nell'SetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-setenvironmentvariable) per modificare una variabile di ambiente. Una volta terminato il blocco dell'ambiente ottenuto da **GetEnvironmentStrings**, chiamare la funzione [**FreeEnvironmentStrings**](/windows/win32/api/processenv/nf-processenv-freeenvironmentstringsa) per liberare il blocco.

La chiamata a [**nell'SetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-setenvironmentvariable) non ha alcun effetto sulle variabili di ambiente di sistema. Per aggiungere o modificare a livello di codice le variabili di ambiente di sistema, aggiungerle alla chiave del registro di **\_ sistema HKEY LOCAL \_ Machine \\ System \\ CurrentControlSet \\ Control \\ Session Manager \\ Environment** , quindi trasmettere un messaggio [**WM \_ SETTINGCHANGE**](/windows/desktop/winmsg/wm-settingchange) con *lParam* impostato sulla stringa "Environment". Questo consente alle applicazioni, ad esempio la shell, di prelevare gli aggiornamenti.

La dimensione massima di una variabile di ambiente definita dall'utente è 32.767 caratteri. Non esiste alcuna limitazione tecnica sulle dimensioni del blocco dell'ambiente. Tuttavia, esistono limiti pratici a seconda del meccanismo utilizzato per accedere al blocco. Un file batch, ad esempio, non può impostare una variabile che supera la lunghezza massima consentita per la riga di comando.

**Windows Server 2003 e Windows XP:** La dimensione massima del blocco di ambiente per il processo è di 32.767 caratteri. A partire da Windows Vista e Windows Server 2008, non esiste alcuna limitazione tecnica sulle dimensioni del blocco dell'ambiente.

La funzione [**GetEnvironmentVariable**](/windows/desktop/api/WinBase/nf-winbase-getenvironmentvariable) determina se una variabile specificata è definita nell'ambiente del processo chiamante e, in caso affermativo, qual è il relativo valore.

Per recuperare una copia del blocco di ambiente per un determinato utente, utilizzare la funzione [**CreateEnvironmentBlock**](/windows/win32/api/userenv/nf-userenv-createenvironmentblock) .

Per espandere le stringhe delle variabili di ambiente, usare la funzione [**ExpandEnvironmentStrings**](/windows/desktop/api/processenv/nf-processenv-expandenvironmentstringsa) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modifica delle variabili di ambiente](changing-environment-variables.md)
</dt> <dt>

[Variabili di ambiente utente](../shell/user-environment-variables.md)
</dt> </dl>

 

 
