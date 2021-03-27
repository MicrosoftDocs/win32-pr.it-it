---
description: In questo argomento vengono fornite informazioni sulle considerazioni sulla sicurezza correlate alla shell di Windows.
ms.assetid: eca31652-2659-456d-b082-c84d6fd39094
title: 'Considerazioni sulla sicurezza: shell Microsoft Windows'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16b11a965a36a403b57a3e5229fc758a4ce37252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753047"
---
# <a name="security-considerations-microsoft-windows-shell"></a>Considerazioni sulla sicurezza: shell Microsoft Windows

In questo argomento vengono fornite informazioni sulle considerazioni sulla sicurezza correlate alla shell di Windows. Questo documento non è in grado di fornire tutte le informazioni necessarie sui problemi di sicurezza, bensì di usarlo come punto di partenza e riferimento per questa specifica area tecnologica.

La shell controlla alcuni aspetti importanti del sistema, inclusi diversi che presentano potenziali rischi per la sicurezza se non sono gestiti correttamente. In questo argomento vengono illustrati alcuni dei problemi più comuni e viene illustrato come risolverli nelle applicazioni. Tenere presente che la sicurezza non è limitata agli exploit basati su Internet. Nei sistemi condivisi, inclusi i sistemi accessibili tramite Servizi terminal, è inoltre necessario assicurarsi che gli utenti non possano eseguire alcuna operazione che possa danneggiare altri utenti che condividono il sistema.

-   [Installazione corretta dell'applicazione](#installing-your-application-properly)
-   [Shlwapi](#shlwapi)
-   [Completamento automatico](#autocomplete)
-   [ShellExecute, ShellExecuteEx e funzioni correlate](#shellexecute-shellexecuteex-and-related-functions)
-   [Trasferimento e copia di file](#moving-and-copying-files)
-   [Scrittura di estensioni dello spazio dei nomi sicure](#writing-secure-namespace-extensions)
-   [Avvisi di sicurezza](#security-alerts)
-   [Argomenti correlati](#related-topics)

## <a name="installing-your-application-properly"></a>Installazione corretta dell'applicazione

La maggior parte dei potenziali problemi di sicurezza della shell può essere mitigata installando correttamente l'applicazione.

-   Installare l'applicazione nella cartella programmi. 

    | Sistema operativo                             | Location                                                                                                                                                                                                                                   |
    |----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Windows XP, Windows Server 2003 e versioni precedenti | \_file di programma CSIDL \_                                                                                                                                                                                                                      |
    | Windows Vista e versioni successive                      | FOLDERID \_ ProgramFiles, FOLDERID \_ PROGRAMFILESX86, FOLDERID \_ ProgramFilesX64, FOLDERID ProgramFilesCommon \_ , FOLDERID \_ ProgramFilesCommonX86 o FOLDERID ProgramFilesCommonX64 \_ . Vedere [**KNOWNFOLDERID**](knownfolderid.md) per le specifiche. |

    

     

-   Non archiviare i dati utente nella cartella programmi.

    Utilizzare la cartella dati appropriata per i dati comuni a tutti gli utenti.

    

    | Sistema operativo                             | Location               |
    |----------------------------------------------|------------------------|
    | Windows XP, Windows Server 2003 e versioni precedenti | CSIDL \_ Common \_ AppData |
    | Windows Vista e versioni successive                      | \_ProgramData FOLDERID  |

    

     

    Utilizzare la cartella di dati utente appropriata per i dati appartenenti a un determinato utente.

    

    | Sistema operativo                             | Location                                                   |
    |----------------------------------------------|------------------------------------------------------------|
    | Windows XP, Windows Server 2003 e versioni precedenti | CSIDL \_ AppData, CSIDL \_ Personal e altri utenti.               |
    | Windows Vista e versioni successive                      | FOLDERID \_ RoamingAppData, FOLDERID \_ Documents e altri. |

    

     

-   Se è necessario eseguire l'installazione in un percorso diverso dalla cartella programmi, assicurarsi di impostare correttamente gli elenchi di controllo di accesso (ACL) in modo che gli utenti non abbiano accesso a parti non appropriate del file system. Qualsiasi dato specifico di un determinato utente deve disporre di un ACL che impedisce ad altri utenti di accedervi.
-   Quando si configurano le associazioni di file, assicurarsi di specificare correttamente la riga di comando. Usare un percorso completo ed eseguire il wrapping di tutti gli elementi che contengono uno spazio vuoto tra virgolette. Racchiudere tra virgolette i parametri del comando. In caso contrario, è possibile che la stringa venga analizzata in modo errato e che l'applicazione non venga avviata correttamente. Di seguito sono riportati due esempi di righe di comando correttamente formattate.

    ```
    "C:\Program Files\MyApp\MyApp.exe" "%1" "%2"
    C:\MyAppDir\MyApp\MyApp.exe "%1"
    ```

    

> [!Note]  
> Il percorso delle cartelle di installazione standard può variare da sistema a sistema. Per ottenere la posizione di una cartella standard in un particolare sistema Windows Vista o versione successiva, chiamare [**SHGetKnownFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) con il valore [**KNOWNFOLDERID**](knownfolderid.md) appropriato. In Windows XP, Windows Server 2003 o sistemi precedenti, chiamare [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) o [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) con il valore [**CSIDL**](csidl.md) appropriato.

 

## <a name="shlwapi"></a>Shlwapi

La shell lightweight API (shlwapi) include una serie di funzioni di modifica delle stringhe. L'uso errato di queste funzioni può provocare stringhe troncate inaspettate senza alcuna notifica del troncamento restituito. Nei casi seguenti, le funzioni shlwapi non devono essere usate. Le funzioni alternative elencate, che presentano un numero minore di rischi, devono essere usate al loro posto.



| Shlwapi (funzione)                                                 | Funzione alternativa                                                                                             |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**Strcat**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcatw),[**StrNCat**](/windows/desktop/api/Shlwapi/nf-shlwapi-strncata)              | [**StringCchCat**](/windows/win32/api/strsafe/nf-strsafe-stringcchcata), [**StringCbCat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata) e funzioni correlate             |
| [**StrCpy**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcpyw), [ **StrCpyN**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcpynw)             | [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya), [**StringCbCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopya) e funzioni correlate         |
| [**wnsprintf**](/windows/desktop/api/Shlwapi/nf-shlwapi-wnsprintfa), [ **wvnsprintf**](/windows/desktop/api/Shlwapi/nf-shlwapi-wvnsprintfa) | [**StringCchPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcchprintfa), [**StringCbPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa) e funzioni correlate |



 

Con funzioni come [**PathRelativePathTo**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathrelativepathtoa) che restituiscono un percorso di file, impostare sempre le dimensioni del buffer su caratteri di percorso massimi \_ . In questo modo si garantisce che il buffer sia sufficientemente grande da consentire il percorso del file più grande, oltre a un carattere null di terminazione.

Per ulteriori informazioni sulle funzioni stringa alternative, vedere [informazioni su strsafe. h](../menurc/strsafe-ovw.md).

## <a name="autocomplete"></a>Completamento automatico

Non utilizzare la funzionalità di completamento automatico per le password.

## <a name="shellexecute-shellexecuteex-and-related-functions"></a>ShellExecute, ShellExecuteEx e funzioni correlate

Sono disponibili diverse funzioni della shell che è possibile usare per avviare le applicazioni: [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), [**WinExec**](/windows/win32/api/winbase/nf-winbase-winexec)e [**SHCreateProcessAsUserW**](/windows/desktop/api/Shellapi/nf-shellapi-shcreateprocessasuserw). Assicurarsi di specificare una definizione non ambigua dell'applicazione che deve essere eseguita.

-   Quando si specifica il percorso del file eseguibile, specificare il percorso completo. Non dipendere dalla Shell per individuare il file.
-   Se si fornisce una stringa della riga di comando che contiene spazi vuoti, racchiudere la stringa tra virgolette. In caso contrario, il parser potrebbe interpretare un singolo elemento che contiene spazi come più elementi.

## <a name="moving-and-copying-files"></a>Trasferimento e copia di file

Una chiave per la sicurezza del sistema è l'assegnazione corretta degli ACL. È anche possibile usare file crittografati. Assicurarsi che, quando si spostano o si copiano i file, a cui viene assegnato l'ACL corretto e che non siano stati accidentalmente decrittografati. Questo include lo stato di trasferimento dei file al **Cestino**, nonché all'interno del file System. Utilizzare [**IFileOperation**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation) (Windows Vista o versione successiva) o [**SHFILEOPERATION**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) (Windows XP e versioni precedenti). Non utilizzare [**MoveFile**](/windows/win32/api/winbase/nf-winbase-movefile), che potrebbe non impostare l'ACL previsto per il file di destinazione.

## <a name="writing-secure-namespace-extensions"></a>Scrittura di estensioni dello spazio dei nomi sicure

Le estensioni dello spazio dei nomi shell sono un modo potente e flessibile per presentare i dati all'utente. Tuttavia, possono causare un errore di sistema se non sono correttamente scritti. Alcuni punti chiave da tenere presente:

-   Non presupporre che i dati, ad esempio le immagini, siano formattati correttamente.
-   Non presupporre che \_ il percorso massimo sia equivalente al numero di *byte* in una stringa. È il numero di *caratteri*.

## <a name="security-alerts"></a>Avvisi di sicurezza

Nella tabella seguente sono elencate alcune funzionalità che possono essere usate in modo non corretto e compromettere la sicurezza delle applicazioni.



| Funzionalità                                                                        | Strategia di riduzione del rischio                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), [ **ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) | Le ricerche che dipendono dal controllo di una serie di percorsi predefiniti per trovare un file specifico possono essere usate in un attacco di spoofing. Usare un percorso completo per assicurarsi di accedere al file desiderato.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**StrCat**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcatw)                                                       | Il primo argomento, *psz1*, deve essere sufficientemente grande da contenere *psz2* è \\ 0' di chiusura; in caso contrario, potrebbe verificarsi un sovraccarico del buffer. In alternativa, utilizzare una delle alternative seguenti. [**StringCbCat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata), [**StringCbCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatexa), [**StringCbCatN**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatna), [**StringCbCatNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatnexa), [**StringCchCat**](/windows/win32/api/strsafe/nf-strsafe-stringcchcata), [**StringCchCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatexa), [**StringCchCatN**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatna)o [**StringCchCatNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatnexa).                                                                                                                                                             |
| [**StrCatBuff**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcatbuffa)                                               | Non è garantito che la stringa finale sia con terminazione null. In alternativa, utilizzare una delle alternative seguenti. [**StringCbCat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata), [**StringCbCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatexa), [**StringCbCatN**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatna), [**StringCbCatNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatnexa), [**StringCchCat**](/windows/win32/api/strsafe/nf-strsafe-stringcchcata), [**StringCchCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatexa), [**StringCchCatN**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatna)o [**StringCchCatNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatnexa).                                                                                                                                                                                                                                  |
| [**StrCatChainW**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcatchainw)                                           | Non è garantito che la stringa finale sia con terminazione null. In alternativa, utilizzare una delle alternative seguenti. [**StringCbCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatexa), [**StringCbCatNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatnexa), [**StringCchCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatexa)o [**StringCchCatNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatnexa).                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**StrCpy**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcpyw)                                                       | Il primo argomento, *psz1*, deve essere sufficientemente grande da contenere *psz2* è \\ 0' di chiusura; in caso contrario, potrebbe verificarsi un sovraccarico del buffer. In alternativa, utilizzare una delle alternative seguenti. [**StringCbCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopya), [**StringCbCopyEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopyexa), [**StringCbCopyN**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopyna), [**StringCbCopyNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopynexa), [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya), [**StringCchCopyEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyexa), [**StringCchCopyN**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyna)o [**StringCchCopyNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopynexa).                                                                                                                                             |
| [**StrCpyN**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcpynw)                                                     | Non è garantito che la stringa copiata sia con terminazione null. In alternativa, utilizzare una delle alternative seguenti. [**StringCbCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopya), [**StringCbCopyEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopyexa), [**StringCbCopyN**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopyna), [**StringCbCopyNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopynexa), [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya), [**StringCchCopyEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyexa), [**StringCchCopyN**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyna), [**StringCchCopyNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopynexa).                                                                                                                                                                                                                    |
| [**StrDup**](/windows/desktop/api/Shlwapi/nf-shlwapi-strdupa)                                                       | [**StrDup**](/windows/desktop/api/Shlwapi/nf-shlwapi-strdupa) presuppone che *lpsz* sia una stringa con terminazione null. Inoltre, la stringa restituita non è garantita con terminazione null. In alternativa, utilizzare una delle alternative seguenti. [**StringCbCat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata), [**StringCbCopyEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopyexa), [**StringCbCopyN**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopyna), [**StringCbCopyNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopynexa), [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya), [**StringCchCopyEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyexa), [**StringCchCopyN**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyna)o [**StringCchCopyNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopynexa).                                                                                                                              |
| [**StrNCat**](/windows/desktop/api/Shlwapi/nf-shlwapi-strncata)                                                     | Il primo argomento, *pszFront*, deve essere sufficientemente grande da contenere *pszBack* è \\ 0' di chiusura; in caso contrario, potrebbe verificarsi un sovraccarico del buffer. Tenere presente che l'ultimo argomento, *cchMax*, è il numero di caratteri da copiare in *pszFront*, non necessariamente la dimensione di *pszFront* in byte. In alternativa, utilizzare una delle alternative seguenti. [**StringCbCat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata), [**StringCbCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatexa), [**StringCbCatN**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatna), [**StringCbCatNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatnexa), [**StringCchCat**](/windows/win32/api/strsafe/nf-strsafe-stringcchcata), [**StringCchCatEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatexa), [**StringCchCatN**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatna)o [**StringCchCatNEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatnexa). |
| [**wnsprintf**](/windows/desktop/api/Shlwapi/nf-shlwapi-wnsprintfa)                                                 | Non è garantito che la stringa copiata sia con terminazione null. In alternativa, utilizzare una delle alternative seguenti. [**StringCbPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa), [**StringCbPrintfEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfexa), [**StringCbVPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbvprintfa), [**StringCbVPrintfEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbvprintfexa), [**StringCchPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcchprintfa), [**StringCchPrintfEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchprintfexa), [**StringCchVPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcchvprintfa)o [**StringCchVPrintfEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchvprintfexa).                                                                                                                                                                                 |
| [**wvnsprintf**](/windows/desktop/api/Shlwapi/nf-shlwapi-wvnsprintfa)                                               | Non è garantito che la stringa copiata sia con terminazione null. In alternativa, utilizzare una delle alternative seguenti. [**StringCbPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa), [**StringCbPrintfEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfexa), [**StringCbVPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbvprintfa), [**StringCbVPrintfEx**](/windows/win32/api/strsafe/nf-strsafe-stringcbvprintfexa), [**StringCchPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcchprintfa), [**StringCchPrintfEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchprintfexa), [**StringCchVPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcchvprintfa)o [**StringCchVPrintfEx**](/windows/win32/api/strsafe/nf-strsafe-stringcchvprintfexa).                                                                                                                                                                                 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Microsoft Security](https://www.microsoft.com/security/default.aspx)
</dt> <dt>

[Centro per sviluppatori dedicato alla sicurezza](https://msdn.microsoft.com/security/)
</dt> <dt>

[Microsoft Solution Accelerator](/previous-versions/tn-archive/cc936627(v=technet.10))
</dt> <dt>

[Security TechCenter](https://technet.microsoft.com/security/default.aspx)
</dt> <dt>

[Informazioni su strsafe. h](../menurc/strsafe-ovw.md)
</dt> </dl>

 

 
