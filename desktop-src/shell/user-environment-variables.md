---
description: Le variabili di ambiente specificano i percorsi di ricerca per i file, le directory per i file temporanei, le opzioni specifiche dell'applicazione e altre informazioni simili.
ms.assetid: 6180e54e-4bd9-4692-83fd-f3f7f1d8f8d7
title: Variabili di ambiente utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41bbe37cdbe7dd82268b2166ed625a9baf1d2502df4c26208bca51a89cd782df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857043"
---
# <a name="user-environment-variables"></a>Variabili di ambiente utente

Le variabili di ambiente specificano i percorsi di ricerca per i file, le directory per i file temporanei, le opzioni specifiche dell'applicazione e altre informazioni simili. Il sistema gestisce un blocco di ambiente per ogni utente e uno per il computer. Il blocco dell'ambiente di sistema rappresenta le variabili di ambiente per tutti gli utenti del computer specifico. Il blocco di ambiente di un utente rappresenta le variabili di ambiente che il sistema gestisce per l'utente specifico, incluso il set di variabili di ambiente di sistema.

Per impostazione predefinita, ogni processo riceve una copia del blocco di ambiente per il processo padre. In genere, si tratta del blocco di ambiente per l'utente connesso. Un processo può specificare blocchi di ambiente diversi per i processi figlio usando la [**funzione CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) o [**CreateProcessAsUser.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessasusera)

Per aggiungere o modificare le variabili di ambiente, l'utente seleziona **System** (Sistema) Pannello di controllo **e** quindi la scheda Environment **(Ambiente).** L'utente può anche aggiungere o modificare le variabili di ambiente da un prompt dei comandi usando il **comando set.** Le variabili di ambiente create con **il comando set** si applicano solo alla finestra di comando in cui sono impostate e ai relativi processi figlio. Per altre informazioni, digitare **set /?** al prompt dei comandi.

Per recuperare una copia del blocco di ambiente per un determinato utente, usare la [**funzione CreateEnvironmentBlock.**](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock) Per liberare un blocco di ambiente creato **da CreateEnvironmentBlock,** usare la [**funzione DestroyEnvironmentBlock.**](/windows/desktop/api/Userenv/nf-userenv-destroyenvironmentblock) Queste funzioni fanno riferimento a un puntatore a un blocco di ambiente. Il blocco di ambiente è una matrice di stringhe Unicode con terminazione Null. L'elenco termina con due valori Null ( \\ 0 \\ 0).

Per espandere una stringa che contiene variabili di ambiente usando il blocco di ambiente per un utente specificato, usare la [**funzione ExpandEnvironmentStringsForUser.**](/windows/desktop/api/Userenv/nf-userenv-expandenvironmentstringsforusera)

 

 
