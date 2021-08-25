---
title: Uso delle informazioni sulla versione
description: In questo argomento viene illustrato come utilizzare le funzioni di informazioni sulla versione.
ms.assetid: 447b57c9-9e94-4a28-897e-f7b87d9cb25a
keywords:
- risorse, informazioni sulla versione
- informazioni sulla versione
- informazioni sul file di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0447bc1dfc3b2d5d5006bb5ff9ca3e9fa8f3d488e9b5621acb932c843fc3630f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846991"
---
# <a name="using-version-information"></a>Uso delle informazioni sulla versione

Un programma di installazione in genere ha gli obiettivi seguenti:

-   Per inserire i file nel percorso corretto.
-   Per notificare all'utente se il programma di installazione sta sostituendo un file esistente con una versione notevolmente diversa, ad esempio sostituendo un file in lingua tedesca con un file in lingua inglese o sostituendo un file più recente con un file meno recente.

Quando si scrive il programma di installazione, è necessario disporre delle informazioni seguenti per ogni file:

-   Nome e percorso del file (detto file di origine).
-   Nome del file equivalente sul disco rigido dell'utente (detto file di destinazione). Questo nome corrisponde in genere al nome del file nel disco di installazione.
-   Stato di condivisione del file, ovvero se il file è privato per l'applicazione in fase di installazione o può essere condiviso da più applicazioni.

Il programma di installazione può usare [**la funzione VerFindFile**](/windows/desktop/api/Winver/nf-winver-verfindfilea) per determinare dove copiare il file sul disco. Questa funzione può essere usata anche per specificare se il file è privato per l'applicazione o può essere condiviso. Se si verifica un problema durante la ricerca del file, **VerFindFile** restituisce un valore di errore. Ad esempio, se il sistema usa il file di destinazione, **VerFindFile** restituisce **VFF \_ FILEINUSE**. Il programma di installazione deve notificare all'utente il problema e rispondere alla decisione dell'utente di continuare o terminare l'installazione.

La [**funzione VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) copia il file di origine in un file temporaneo nella directory specificata da [**VerFindFile**](/windows/desktop/api/Winver/nf-winver-verfindfilea). Se necessario, **VerInstallFile** espande il file usando le funzioni nella libreria di decompressione dei dati.

[**VerInstallFile confronta**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) le informazioni sulla versione del file temporaneo con quello del file di destinazione. Se i due valori sono diversi, **VerInstallFile** restituisce uno o più valori di errore. Ad esempio, restituisce **VIF \_ SRCOLD** se il file temporaneo è meno recente del file di destinazione e **VIF \_ DIFFLANG** se i file hanno identificatori di lingua o valori della tabella codici diversi. Il programma di installazione deve notificare all'utente il problema e rispondere alla decisione dell'utente di continuare o terminare l'installazione.

Alcuni [**errori VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) sono recuperabili. Ciò significa che il programma di installazione può chiamare nuovamente **VerInstallFile,** specificando l'opzione **VIFF \_ FORCEINSTALL,** per installare il file indipendentemente dal conflitto di versione. Se **VerInstallFile restituisce** **VIF \_ TEMPFILE e** l'utente sceglie di non forzare l'installazione, il programma di installazione deve eliminare il file temporaneo.

[**VerInstallFile potrebbe**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) riscontrare un errore irreversibile durante il tentativo di forzare l'installazione, anche se l'errore non esisteva in precedenza. Ad esempio, il file potrebbe essere bloccato da un altro utente prima che il programma di installazione tenta di forzare l'installazione. Se un programma di installazione tenta di forzare l'installazione dopo un errore non ripristinabile, **VerInstallFile ha** esito negativo. Il programma di installazione deve contenere routine per il ripristino da questo tipo di errore.

La soluzione consigliata consiste nel visualizzare una finestra di dialogo con i pulsanti **Installa**, **Ignora** e **Installa tutto**. Un'altra soluzione è una finestra di dialogo con i pulsanti **Sì**, Sì **a tutti**, **Ignora** e **Annulla**. Il **pulsante Installa tutto** dovrebbe impedire al programma di installazione di richiedere all'utente errori simili includendo l'opzione **VIFF \_ FORCEINSTALL** in tutti gli utilizzi successivi di [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea). Per gli errori irreversibili, i **pulsanti Installa** e **Installa** tutto devono essere disabilitati.

Per visualizzare un messaggio di errore utile all'utente, il programma di installazione deve in genere recuperare informazioni dalle risorse della versione dei file in conflitto. A questo scopo, il programma di installazione può usare quattro funzioni:

-   [**GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea)
-   [**GetFileVersionInfo**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoa)
-   [**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea)
-   [**VerLanguageName**](/windows/desktop/api/Winver/nf-winver-verlanguagenamea)

[**GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea) restituisce le dimensioni delle informazioni sulla versione. [**GetFileVersionInfo usa**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoa) le informazioni recuperate **da GetFileVersionInfoSize** per recuperare una struttura che contiene le informazioni sulla versione. [**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea) recupera un membro specifico da tale struttura.

Ad esempio, se [**VerInstallFile**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) restituisce l'errore **VIF \_ DIFFTYPE,** il programma di installazione deve usare le funzioni [**GetFileVersionInfoSize**](/windows/desktop/api/Winver/nf-winver-getfileversioninfosizea), [**GetFileVersionInfo**](/windows/desktop/api/Winver/nf-winver-getfileversioninfoa)e [**VerQueryValue**](/windows/desktop/api/Winver/nf-winver-verqueryvaluea) nei file temporanei e di destinazione per ottenere il tipo generale di ogni file. Se le lingue dei file sono in conflitto, il programma di installazione deve usare anche [**VerLanguageName**](/windows/desktop/api/Winver/nf-winver-verlanguagenamea) per convertire l'identificatore della lingua binaria in una rappresentazione testuale della lingua. Ad esempio, 0x040C converte nella stringa "Francese.")

Se [**VerInstallFile restituisce**](/windows/desktop/api/Winver/nf-winver-verinstallfilea) un errore di file, ad esempio **VIF \_ ACCESSVIOLATION,** il programma di installazione deve usare la [**funzione GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) per recuperare il valore di errore più recente. Il programma deve tradurre questo valore in un messaggio informativo da visualizzare all'utente. Il programma non deve cedere il controllo tra le chiamate **a VerInstallFile** **e GetLastError.**

 

 