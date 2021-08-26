---
description: Le applicazioni possono controllare il percorso da cui viene caricata una DLL specificando un percorso completo o usando un altro meccanismo, ad esempio un manifesto. Se questi metodi non vengono utilizzati, il sistema cerca la DLL in fase di caricamento, come descritto in questo argomento.
ms.assetid: 44228cf2-6306-466c-8f16-f513cd3ba8b5
title: Dynamic-Link di ricerca della libreria
ms.topic: article
ms.date: 09/11/2020
ms.custom: contperf-fy21q1
ms.openlocfilehash: e2abe21e0283adab4fbc3c17db6503772e20c217cf3019ea775812b0f45e5145
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083441"
---
# <a name="dynamic-link-library-search-order"></a>Dynamic-Link di ricerca della libreria

Un sistema può contenere più versioni della stessa libreria a collegamento dinamico (DLL). Le applicazioni possono controllare il percorso da cui viene caricata una DLL specificando un percorso completo o usando un altro meccanismo, ad esempio un manifesto. Se questi metodi non vengono utilizzati, il sistema cerca la DLL in fase di caricamento, come descritto in questo argomento.

-   [Fattori che influiscono sulla ricerca](#factors-that-affect-searching)
-   [Ordine di ricerca per le app UWP](#search-order-for-uwp-apps)
    -   [Ordine di ricerca standard per le app UWP](#standard-search-order-for-uwp-apps)
    -   [Ordine di ricerca alternativo per le app UWP](#alternate-search-order-for-uwp-apps)
-   [Ordine di ricerca per le applicazioni desktop](#search-order-for-desktop-applications)
    -   [Ordine di ricerca standard per le applicazioni desktop](#standard-search-order-for-desktop-applications)
    -   [Ordine di ricerca alternativo per le applicazioni desktop](#alternate-search-order-for-desktop-applications)
    -   [Ordine di ricerca con **i flag DI RICERCA \_ \_ DI LOAD LIBRARY**](#search-order-using-load_library_search-flags)
-   [Argomenti correlati](#related-topics)

## <a name="factors-that-affect-searching"></a>Fattori che influiscono sulla ricerca

I fattori seguenti influiscono sulla ricerca di una DLL da parte del sistema:

-   Se una DLL con lo stesso nome di modulo è già caricata in memoria, il sistema verifica solo il reindirizzamento e un manifesto prima di risolvere la DLL caricata, indipendentemente dalla directory in cui si trova. Il sistema non cerca la DLL.
-   Se la DLL è in elenco di DLL note per la versione di Windows in cui è in esecuzione l'applicazione, il sistema usa la copia della DLL nota (e delle DLL dipendenti della DLL nota, se presenti) anziché cercare la DLL. Per un elenco di DLL note nel sistema corrente, vedere la chiave del Registro di sistema **seguente: HKEY \_ LOCAL MACHINE SYSTEM \_ \\ \\ CurrentControlSet \\ Control Session Manager \\ \\ KnownDLLs**.
-   Se una DLL ha dipendenze, il sistema cerca le DLL dipendenti come se fossero caricate solo con i relativi nomi di modulo. Questo vale anche se la prima DLL è stata caricata specificando un percorso completo.

## <a name="search-order-for-uwp-apps"></a>Ordine di ricerca per le app UWP

Quando un'app UWP per Windows 10 (o un'app dello Store per Windows 8.x) carica un modulo in pacchetto chiamando la funzione [**LoadPackagedLibrary,**](/windows/desktop/api/Winbase/nf-winbase-loadpackagedlibrary) la DLL deve essere nel grafico delle dipendenze del pacchetto del processo. Per altre informazioni, vedere **LoadPackagedLibrary.** Quando un'app UWP carica un modulo in altro modo e non specifica un percorso completo, il sistema cerca la DLL e le relative dipendenze in fase di caricamento, come descritto in questa sezione.

Prima di cercare una DLL, il sistema verifica quanto segue:

-   Se una DLL con lo stesso nome di modulo è già caricata in memoria, il sistema usa la DLL caricata, indipendentemente dalla directory in cui si trova. Il sistema non cerca la DLL.
-   Se la DLL è in elenco di DLL note per la versione di Windows in cui è in esecuzione l'applicazione, il sistema usa la copia della DLL nota (e le DLL dipendenti della DLL nota, se presenti). Il sistema non cerca la DLL. Per un elenco di DLL note nel sistema corrente, vedere la chiave del Registro di sistema **seguente: HKEY \_ LOCAL MACHINE SYSTEM \_ \\ \\ CurrentControlSet \\ Control Session Manager \\ \\ KnownDLLs**.

Se il sistema deve cercare un modulo o le relative dipendenze, usa sempre l'ordine di ricerca per le app UWP anche se una dipendenza non è il codice dell'app UWP.

### <a name="standard-search-order-for-uwp-apps"></a>Ordine di ricerca standard per le app UWP

Se il modulo non è già caricato o nell'elenco di DLL note, il sistema esegue la ricerca in questi percorsi nell'ordine seguente:

1.  Grafico delle dipendenze del pacchetto del processo. Si tratta del pacchetto dell'applicazione più eventuali dipendenze specificate come `<PackageDependency>` nella sezione del manifesto del pacchetto `<Dependencies>` dell'applicazione. Le dipendenze vengono ricercate nell'ordine in cui vengono visualizzate nel manifesto.
2.  Directory da cui è stato caricato il processo chiamante.
3.  Directory di sistema (%SystemRoot% \\ system32).

Se una DLL ha dipendenze, il sistema cerca le DLL dipendenti come se fossero caricate solo con i relativi nomi di modulo. Questo vale anche se la prima DLL è stata caricata specificando un percorso completo.

### <a name="alternate-search-order-for-uwp-apps"></a>Ordine di ricerca alternativo per le app UWP

Se un modulo modifica l'ordine di ricerca standard chiamando la funzione [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) con **LOAD WITH \_ \_ ALTERED SEARCH \_ \_ PATH,** il sistema cerca nella directory da cui è stato caricato il modulo specificato anziché nella directory del processo chiamante. Il sistema esegue la ricerca in queste posizioni nell'ordine seguente:

1.  Grafico delle dipendenze del pacchetto del processo. Si tratta del pacchetto dell'applicazione più eventuali dipendenze specificate come `<PackageDependency>` nella sezione del manifesto del pacchetto `<Dependencies>` dell'applicazione. Le dipendenze vengono ricercate nell'ordine in cui vengono visualizzate nel manifesto.
2.  Directory da cui è stato caricato il modulo specificato.
3.  Directory di sistema (%SystemRoot% \\ system32).

## <a name="search-order-for-desktop-applications"></a>Ordine di ricerca per le applicazioni desktop

Le applicazioni desktop possono controllare il percorso da cui viene caricata una DLL specificando un percorso completo, usando il reindirizzamento [DLL](dynamic-link-library-redirection.md)o un [manifesto](/windows/desktop/SbsCs/manifests). Se non viene usato nessuno di questi metodi, il sistema cerca la DLL in fase di caricamento, come descritto in questa sezione.

Prima di cercare una DLL, il sistema verifica quanto segue:

-   Se una DLL con lo stesso nome di modulo è già caricata in memoria, il sistema usa la DLL caricata, indipendentemente dalla directory in cui si trova. Il sistema non cerca la DLL.
-   Se la DLL è in elenco di DLL note per la versione di Windows in cui è in esecuzione l'applicazione, il sistema usa la copia della DLL nota (e le DLL dipendenti della DLL nota, se presenti). Il sistema non cerca la DLL. Per un elenco di DLL note nel sistema corrente, vedere la chiave del Registro di sistema **seguente: HKEY \_ LOCAL MACHINE SYSTEM \_ \\ \\ CurrentControlSet \\ Control Session Manager \\ \\ KnownDLLs**.

Se una DLL ha dipendenze, il sistema cerca le DLL dipendenti come se fossero caricate solo con i relativi nomi di modulo. Questo vale anche se la prima DLL è stata caricata specificando un percorso completo.

> [!IMPORTANT]
> Se un utente malintenzionato ottiene il controllo di una delle directory in cui viene cercata, può inserire una copia dannosa della DLL in tale directory. Per informazioni su come prevenire tali attacchi, vedere [Sicurezza della libreria a collegamento dinamico.](dynamic-link-library-security.md)

### <a name="standard-search-order-for-desktop-applications"></a>Ordine di ricerca standard per le applicazioni desktop

L'ordine di ricerca delle DLL standard utilizzato dal sistema dipende dall'attivazione o meno della modalità di ricerca DLL sicura. Cassaforte La modalità di ricerca DLL inserisce la directory corrente dell'utente in un secondo momento nell'ordine di ricerca.

Cassaforte La modalità di ricerca DLL è abilitata per impostazione predefinita. Per disabilitare questa funzionalità, creare il valore del Registro di sistema **HKEY \_ LOCAL MACHINE System \_ \\ \\ CurrentControlSet \\ Control Session \\ Manager** \\ **SafeDllSearchMode** e impostarlo su 0. La chiamata [**alla funzione SetDllDirectory**](/windows/desktop/api/winbase/nf-winbase-setdlldirectorya) disabilita in modo efficace **SafeDllSearchMode** mentre la directory specificata si trova nel percorso di ricerca e modifica l'ordine di ricerca come descritto in questo argomento.

Se **SafeDllSearchMode è** abilitato, l'ordine di ricerca è il seguente:

1.  Directory da cui è stata caricata l'applicazione.
2.  Directory di sistema. Usare la [**funzione GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) per ottenere il percorso di questa directory.
3.  Directory di sistema a 16 bit. Non esiste alcuna funzione che ottiene il percorso di questa directory, ma viene cercata.
4.  Directory Windows. Usare la [**funzione GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) per ottenere il percorso di questa directory.
5.  La directory corrente.
6.  Directory elencate nella variabile di ambiente PATH. Si noti che non include il percorso per applicazione specificato dalla chiave del Registro di sistema **Percorsi** app. La **chiave Dei percorsi** dell'app non viene usata durante il calcolo del percorso di ricerca della DLL.

Se **SafeDllSearchMode è** disabilitato, l'ordine di ricerca è il seguente:

1.  Directory da cui è stata caricata l'applicazione.
2.  La directory corrente.
3.  Directory di sistema. Usare la [**funzione GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) per ottenere il percorso di questa directory.
4.  Directory di sistema a 16 bit. Non esiste alcuna funzione che ottiene il percorso di questa directory, ma viene cercata.
5.  Directory Windows. Usare la [**funzione GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) per ottenere il percorso di questa directory.
6.  Directory elencate nella variabile di ambiente PATH. Si noti che non include il percorso per applicazione specificato dalla chiave del Registro di sistema **Percorsi** app. La **chiave Dei percorsi** dell'app non viene usata durante il calcolo del percorso di ricerca della DLL.

### <a name="alternate-search-order-for-desktop-applications"></a>Ordine di ricerca alternativo per le applicazioni desktop

L'ordine di ricerca standard usato dal sistema può essere modificato chiamando la [**funzione LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) **con LOAD WITH \_ \_ ALTERED SEARCH \_ \_ PATH**. L'ordine di ricerca standard può essere modificato anche chiamando la [**funzione SetDllDirectory.**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya)

> [!NOTE]
> L'ordine di ricerca standard del processo sarà influenzato anche dalla chiamata della [**funzione SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) nel processo padre prima dell'avvio del processo corrente.

Se si specifica una strategia di ricerca alternativa, il relativo comportamento continua fino a quando non vengono individuati tutti i moduli eseguibili associati. Dopo che il sistema ha avviato l'elaborazione delle routine di inizializzazione delle DLL, viene ripristinata la strategia di ricerca standard.

La [**funzione LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) supporta un ordine di ricerca alternativo se la chiamata specifica **LOAD WITH \_ \_ ALTERED SEARCH \_ \_ PATH** e il parametro *lpFileName* specifica un percorso assoluto.

Si noti che la strategia di ricerca standard e la strategia di ricerca alternativa specificata da [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) con **LOAD WITH \_ \_ ALTERED SEARCH \_ \_ PATH** differiscono in un solo modo: la ricerca standard inizia nella directory dell'applicazione chiamante e la ricerca alternativa inizia nella directory del modulo eseguibile che **LoadLibraryEx** sta caricando.

Se **SafeDllSearchMode è** abilitato, l'ordine di ricerca alternativo è il seguente:

1.  Directory specificata da *lpFileName.*
2.  Directory di sistema. Usare la [**funzione GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) per ottenere il percorso di questa directory.
3.  Directory di sistema a 16 bit. Non esiste alcuna funzione che ottiene il percorso di questa directory, ma viene cercata.
4.  Directory Windows. Usare la [**funzione GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) per ottenere il percorso di questa directory.
5.  La directory corrente.
6.  Directory elencate nella variabile di ambiente PATH. Si noti che non include il percorso per applicazione specificato dalla chiave del Registro di sistema **Percorsi** app. La **chiave Dei percorsi** dell'app non viene usata durante il calcolo del percorso di ricerca della DLL.

Se **SafeDllSearchMode è** disabilitato, l'ordine di ricerca alternativo è il seguente:

1.  Directory specificata da *lpFileName.*
2.  La directory corrente.
3.  Directory di sistema. Usare la [**funzione GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) per ottenere il percorso di questa directory.
4.  Directory di sistema a 16 bit. Non esiste alcuna funzione che ottiene il percorso di questa directory, ma viene cercata.
5.  Directory Windows. Usare la [**funzione GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) per ottenere il percorso di questa directory.
6.  Directory elencate nella variabile di ambiente PATH. Si noti che non include il percorso per applicazione specificato dalla chiave del Registro di sistema **Percorsi** app. La **chiave Dei percorsi** dell'app non viene usata durante il calcolo del percorso di ricerca della DLL.

La [**funzione SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) supporta un ordine di ricerca alternativo se il *parametro lpPathName* specifica un percorso. L'ordine di ricerca alternativo è il seguente:

1.  Directory da cui è stata caricata l'applicazione.
2.  Directory specificata dal parametro *lpPathName* di [**SetDllDirectory.**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya)
3.  Directory di sistema. Usare la [**funzione GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) per ottenere il percorso di questa directory. Il nome di questa directory è System32.
4.  Directory di sistema a 16 bit. Non esiste alcuna funzione che ottiene il percorso di questa directory, ma viene cercata. Il nome di questa directory è System.
5.  Directory Windows. Usare la [**funzione GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) per ottenere il percorso di questa directory.
6.  Directory elencate nella variabile di ambiente PATH. Si noti che non include il percorso per applicazione specificato dalla chiave del Registro di sistema **Percorsi** app. La **chiave Dei percorsi** dell'app non viene usata durante il calcolo del percorso di ricerca della DLL.

Se il *parametro lpPathName* è una stringa vuota, la chiamata rimuove la directory corrente dall'ordine di ricerca.

[**SetDllDirectory disabilita**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) in modo efficace la modalità di ricerca dll sicura mentre la directory specificata si trova nel percorso di ricerca. Per ripristinare la modalità di ricerca DLL sicura in base al valore del Registro di sistema **SafeDllSearchMode** e ripristinare la directory corrente nell'ordine di ricerca, chiamare **SetDllDirectory** con *lpPathName* come NULL.

### <a name="search-order-using-load_library_search-flags"></a>Ordine di ricerca con **i flag DI RICERCA \_ \_ DI LOAD LIBRARY**

Un'applicazione può specificare un ordine di ricerca usando uno o più flag **LOAD \_ LIBRARY \_ SEARCH** con la [**funzione LoadLibraryEx.**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) Un'applicazione può anche usare **i flag LOAD LIBRARY \_ \_ SEARCH** con la [**funzione SetDefaultDllDirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories) per stabilire un ordine di ricerca dll per un processo. L'applicazione può specificare directory aggiuntive per l'ordine di ricerca della DLL del processo usando le [**funzioni AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory) [**o SetDllDirectory.**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya)

Le directory in cui viene cercata dipendono dai flag specificati con [**SetDefaultDllDirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories) [**o LoadLibraryEx.**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) Se si usa più di un flag, le directory corrispondenti vengono ricercate nell'ordine seguente:

1.  Directory che contiene la DLL (**LOAD LIBRARY SEARCH DLL LOAD \_ \_ \_ \_ \_ DIR**). Questa directory viene cercata solo per le dipendenze della DLL da caricare.
2.  Directory dell'applicazione (**LOAD LIBRARY SEARCH APPLICATION \_ \_ \_ \_ DIR**).
3.  Percorsi aggiunti in modo [**esplicito con la funzione AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory) (**LOAD LIBRARY SEARCH USER \_ \_ \_ \_ DIRS**) o [**la funzione SetDllDirectory.**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) Se sono stati aggiunti più percorsi, l'ordine in cui vengono cercati i percorsi non è specificato.
4.  Directory di sistema (**LOAD \_ LIBRARY SEARCH \_ \_ SYSTEM32**).

Se l'applicazione non chiama [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) con alcun flag **LOAD LIBRARY \_ \_ SEARCH** o stabilisce un ordine di ricerca dll per il processo, il sistema cerca le DLL usando l'ordine di ricerca standard o l'ordine di ricerca alternativo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory)
</dt> <dt>

[Registrazione dell'applicazione](/windows/desktop/shell/app-registration)
</dt> <dt>

[Reindirizzamento della libreria a collegamento dinamico](dynamic-link-library-redirection.md)
</dt> <dt>

[Sicurezza delle librerie a collegamento dinamico](dynamic-link-library-security.md)
</dt> <dt>

[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)
</dt> <dt>

[**LoadPackagedLibrary**](/windows/desktop/api/Winbase/nf-winbase-loadpackagedlibrary)
</dt> <dt>

[**SetDefaultDllDirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories)
</dt> <dt>

[**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya)
</dt> <dt>

[Componenti side-by-side](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal)
</dt> </dl>

 

 
