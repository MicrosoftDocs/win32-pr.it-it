---
description: Le variabili di ambiente specificano i percorsi di ricerca per i file, le directory per i file temporanei, le opzioni specifiche dell'applicazione e altre informazioni simili.
ms.assetid: 6180e54e-4bd9-4692-83fd-f3f7f1d8f8d7
title: Variabili di ambiente utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf4f898c7a9135c0421fdd67a7bed1d97655556f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994781"
---
# <a name="user-environment-variables"></a>Variabili di ambiente utente

Le variabili di ambiente specificano i percorsi di ricerca per i file, le directory per i file temporanei, le opzioni specifiche dell'applicazione e altre informazioni simili. Il sistema mantiene un blocco di ambiente per ogni utente e uno per il computer. Il blocco dell'ambiente di sistema rappresenta le variabili di ambiente per tutti gli utenti del computer specifico. Il blocco dell'ambiente di un utente rappresenta le variabili di ambiente gestite dal sistema per quel particolare utente, incluso il set di variabili di ambiente di sistema.

Per impostazione predefinita, ogni processo riceve una copia del blocco di ambiente per il processo padre. Si tratta in genere del blocco dell'ambiente per l'utente che ha eseguito l'accesso. Un processo può specificare blocchi di ambiente diversi per i processi figlio utilizzando la funzione [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) o [**CreateProcessAsUser ha**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) .

Per aggiungere o modificare le variabili di ambiente, l'utente seleziona **sistema** dal **Pannello di controllo**, quindi seleziona la scheda **ambiente** . L'utente può anche aggiungere o modificare le variabili di ambiente al prompt dei comandi usando il comando **set** . Le variabili di ambiente create con il comando **set** si applicano solo alla finestra di comando in cui sono impostate e ai relativi processi figlio. Per ulteriori informazioni, digitare **set/?** al prompt dei comandi.

Per recuperare una copia del blocco di ambiente per un determinato utente, utilizzare la funzione [**CreateEnvironmentBlock**](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock) . Per liberare un blocco di ambiente creato da **CreateEnvironmentBlock**, usare la funzione [**DestroyEnvironmentBlock**](/windows/desktop/api/Userenv/nf-userenv-destroyenvironmentblock) . Queste funzioni fanno riferimento a un puntatore a un blocco di ambiente. Il blocco Environment è una matrice di stringhe Unicode con terminazione null. L'elenco termina con due valori null ( \\ 0 \\ 0).

Per espandere una stringa che contiene le variabili di ambiente tramite il blocco Environment per un utente specificato, utilizzare la funzione [**ExpandEnvironmentStringsForUser**](/windows/desktop/api/Userenv/nf-userenv-expandenvironmentstringsforusera) .

 

 
