---
title: Utilizzo delle informazioni sulla versione
description: In questo argomento viene illustrato come utilizzare le funzioni di informazioni sulla versione.
ms.assetid: 447b57c9-9e94-4a28-897e-f7b87d9cb25a
keywords:
- risorse, informazioni sulla versione
- informazioni sulla versione
- informazioni sul file di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a8785275f5aac69218989250d1c0f83e0a1ff9f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725455"
---
# <a name="using-version-information"></a>Utilizzo delle informazioni sulla versione

Un programma di installazione ha in genere gli obiettivi seguenti:

-   Per inserire i file nel percorso corretto.
-   Per notificare all'utente se il programma di installazione sostituisce un file esistente con una versione significativamente diversa, ad esempio sostituendo un file in lingua tedesca con un file in lingua inglese o sostituendo un file più recente con un file precedente.

Quando si scrive il programma di installazione, è necessario disporre delle seguenti informazioni per ogni file:

-   Nome e percorso del file (denominato file di origine).
-   Nome del file equivalente sul disco rigido dell'utente (denominato file di destinazione). Questo nome corrisponde in genere al nome del file nel disco di installazione.
-   Lo stato di condivisione del file, vale a dire se il file è privato per l'applicazione in fase di installazione o può essere condiviso da più applicazioni.

Il programma di installazione può utilizzare la funzione [**VerFindFile**](/windows/desktop/api/Winver/nf-winver-verfindfilea) per determinare la posizione in cui copiare il file sul disco. Questa funzione può essere utilizzata anche per specificare se il file è privato o può essere condiviso. Se si verifica un problema durante la ricerca del file, **VerFindFile** restituisce un valore di errore. Ad esempio, se il sistema usa il file di destinazione, **VerFindFile** restituisce **VFF \_ FILEINUSE**. Il programma di installazione deve notificare all'utente il problema e rispondere alla decisione dell'utente di continuare o di terminare l'installazione.

La funzione [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) copia il file di origine in un file temporaneo nella directory specificata da [**VerFindFile**](/windows/desktop/api/Winver/nf-winver-verfindfilea). Se necessario, **VerInstallFile** espande il file usando le funzioni nella libreria di decompressione dei dati.

[**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) Confronta le informazioni sulla versione del file temporaneo con quelle del file di destinazione. Se i due valori sono diversi, **VerInstallFile** restituisce uno o più valori di errore. Ad esempio, restituisce **VIF \_ SRCOLD** se il file temporaneo è antecedente al file di destinazione e **VIF \_ DIFFLANG** se i file hanno identificatori di lingua o valori della tabella codici diversi. Il programma di installazione deve notificare all'utente il problema e rispondere alla decisione dell'utente di continuare o di terminare l'installazione.

Alcuni errori di [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) sono recuperabili. In altre termini, il programma di installazione può chiamare nuovamente **VerInstallFile** , specificando l'opzione **VIFF \_ FORCEINSTALL** , per installare il file indipendentemente dal conflitto di versione. Se **VerInstallFile** restituisce **VIF \_ tempfile** e l'utente sceglie di non forzare l'installazione, il programma di installazione deve eliminare il file temporaneo.

[**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) potrebbe verificarsi un errore irreversibile durante il tentativo di forzare l'installazione, anche se l'errore non esisteva in precedenza. Ad esempio, il file potrebbe essere bloccato da un altro utente prima che il programma di installazione abbia tentato di forzare l'installazione. Se un programma di installazione tenta di forzare l'installazione dopo un errore irreversibile, **VerInstallFile** non riesce. Il programma di installazione deve contenere routine per il ripristino da questo tipo di errore.

La soluzione consigliata consiste nel visualizzare una finestra di dialogo con i pulsanti **Installa**, **Ignora** e **installa tutto**. Un'altra soluzione è una finestra di dialogo con i pulsanti **Sì**, **Sì**, **Ignora** e **Annulla**. Il pulsante **installa tutto** dovrebbe impedire al programma di installazione di richiedere all'utente errori simili, includendo l'opzione **VIFF \_ FORCEINSTALL** in tutti gli utilizzi successivi di [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea). Per gli errori irreversibili, i pulsanti **Installa** e **installa tutti** devono essere disabilitati.

Per visualizzare un messaggio di errore utile all'utente, il programma di installazione di solito deve recuperare le informazioni dalle risorse di versione dei file in conflitto. Sono disponibili quattro funzioni che il programma di installazione può utilizzare a questo scopo:

-   [**Impossibile eseguire GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea)
-   [**GetFileVersionInfo**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoa)
-   [**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea)
-   [**VerLanguageName**](/windows/desktop/api/Winver/nf-winver-verlanguagenamea)

[**Impossibile eseguire GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea) restituisce le dimensioni delle informazioni sulla versione. [**GetFileVersionInfo**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoa) usa le informazioni recuperate da **Impossibile eseguire GetFileVersionInfoSize** per recuperare una struttura che contiene le informazioni sulla versione. [**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea) recupera un membro specifico da tale struttura.

Se, ad esempio, [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) restituisce l'errore **VIF \_ elemento DiffType** , il programma di installazione deve utilizzare le funzioni [**Impossibile eseguire GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea), [**GetFileVersionInfo**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoa)e [**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea) sui file temporanei e di destinazione per ottenere il tipo generale di ogni file. Se le lingue dei file sono in conflitto, anche il programma di installazione deve usare [**VerLanguageName**](/windows/desktop/api/Winver/nf-winver-verlanguagenamea) per convertire l'identificatore di lingua binario in una rappresentazione testuale della lingua. Ad esempio, 0x040C viene convertito nella stringa "French".

Se [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) restituisce un errore di file, ad esempio **VIF \_ ACCESSVIOLATION**, il programma di installazione deve usare la funzione [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) per recuperare il valore di errore più recente. Il programma deve tradurre questo valore in un messaggio informativo da visualizzare all'utente. Il programma non deve restituire il controllo tra le chiamate a **VerInstallFile** e **GetLastError**.

 

 