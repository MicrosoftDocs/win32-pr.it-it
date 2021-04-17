---
description: Le applicazioni possono controllare la posizione da cui viene caricata una DLL specificando un percorso completo o un altro meccanismo, ad esempio un manifesto. Se questi metodi non vengono usati, il sistema cerca la DLL in fase di caricamento, come descritto in questo argomento.
ms.assetid: 44228cf2-6306-466c-8f16-f513cd3ba8b5
title: Ordine di ricerca della libreria Dynamic-Link
ms.topic: article
ms.date: 09/11/2020
ms.custom: contperf-fy21q1
ms.openlocfilehash: 928cf9030e24c91145ae95e1eed680017bf68533
ms.sourcegitcommit: f374b50b37160b683da16b59ac9340282a8f50a5
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/04/2021
ms.locfileid: "104520330"
---
# <a name="dynamic-link-library-search-order"></a>Ordine di ricerca della libreria Dynamic-Link

Un sistema può contenere più versioni della stessa libreria di collegamento dinamico (DLL). Le applicazioni possono controllare la posizione da cui viene caricata una DLL specificando un percorso completo o un altro meccanismo, ad esempio un manifesto. Se questi metodi non vengono usati, il sistema cerca la DLL in fase di caricamento, come descritto in questo argomento.

-   [Fattori che influiscono sulla ricerca](#factors-that-affect-searching)
-   [Ordine di ricerca per le app UWP](#search-order-for-uwp-apps)
    -   [Ordine di ricerca standard per le app UWP](#standard-search-order-for-uwp-apps)
    -   [Ordine di ricerca alternativo per le app UWP](#alternate-search-order-for-uwp-apps)
-   [Ordine di ricerca per le applicazioni desktop](#search-order-for-desktop-applications)
    -   [Ordine di ricerca standard per le applicazioni desktop](#standard-search-order-for-desktop-applications)
    -   [Ordine di ricerca alternativo per le applicazioni desktop](#alternate-search-order-for-desktop-applications)
    -   [Ordine di ricerca usando i flag di **\_ \_ ricerca della libreria di caricamento**](/windows)
-   [Argomenti correlati](#related-topics)

## <a name="factors-that-affect-searching"></a>Fattori che influiscono sulla ricerca

I seguenti fattori influiscono sull'eventuale ricerca di una DLL da parte del sistema:

-   Se una DLL con lo stesso nome di modulo è già caricata in memoria, il sistema controlla solo il reindirizzamento e un manifesto prima della risoluzione nella DLL caricata, indipendentemente dalla directory in cui si trova. Il sistema non esegue la ricerca della DLL.
-   Se la DLL è nell'elenco di dll note per la versione di Windows in cui è in esecuzione l'applicazione, il sistema utilizza la copia della DLL nota (e le DLL dipendenti della DLL, se presenti) invece di cercare la DLL. Per un elenco di dll note nel sistema corrente, vedere la chiave del registro di sistema seguente: **HKEY \_ Local \_ Machine \\ System \\ CurrentControlSet \\ Control \\ Session Manager \\ KnownDLL**.
-   Se una DLL presenta dipendenze, il sistema cerca le DLL dipendenti come se fossero state caricate solo con i nomi dei moduli. Questo vale anche se la prima DLL è stata caricata specificando un percorso completo.

## <a name="search-order-for-uwp-apps"></a>Ordine di ricerca per le app UWP

Quando un'app UWP per Windows 10 (o un'app dello Store per Windows 8. x) carica un modulo in pacchetto chiamando la funzione [**LoadPackagedLibrary**](/windows/desktop/api/Winbase/nf-winbase-loadpackagedlibrary) , la dll deve trovarsi nel grafico delle dipendenze del pacchetto del processo. Per ulteriori informazioni, vedere **LoadPackagedLibrary**. Quando un'app UWP carica un modulo con altri mezzi e non specifica un percorso completo, il sistema cerca la DLL e le relative dipendenze in fase di caricamento, come descritto in questa sezione.

Prima che il sistema esegua la ricerca di una DLL, verifica quanto segue:

-   Se una DLL con lo stesso nome di modulo è già caricata in memoria, il sistema usa la DLL caricata, indipendentemente dalla directory in cui si trova. Il sistema non esegue la ricerca della DLL.
-   Se la DLL è nell'elenco di dll note per la versione di Windows in cui è in esecuzione l'applicazione, il sistema usa la copia della DLL nota (e le DLL dipendenti della DLL, se presenti). Il sistema non esegue la ricerca della DLL. Per un elenco di dll note nel sistema corrente, vedere la chiave del registro di sistema seguente: **HKEY \_ Local \_ Machine \\ System \\ CurrentControlSet \\ Control \\ Session Manager \\ KnownDLL**.

Se il sistema deve cercare un modulo o le relative dipendenze, USA sempre l'ordine di ricerca per le app UWP anche se una dipendenza non è il codice dell'app UWP.

### <a name="standard-search-order-for-uwp-apps"></a>Ordine di ricerca standard per le app UWP

Se il modulo non è già caricato o nell'elenco di dll note, il sistema esegue la ricerca in questi percorsi nell'ordine seguente:

1.  Grafico delle dipendenze del pacchetto del processo. Si tratta del pacchetto dell'applicazione più tutte le dipendenze specificate come `<PackageDependency>` nella `<Dependencies>` sezione del manifesto del pacchetto dell'applicazione. Le dipendenze vengono ricercate nell'ordine in cui sono visualizzate nel manifesto.
2.  La directory da cui è stato caricato il processo chiamante.
3.  Directory di sistema (% SystemRoot% \\ System32).

Se una DLL presenta dipendenze, il sistema cerca le DLL dipendenti come se fossero state caricate solo con i nomi dei moduli. Questo vale anche se la prima DLL è stata caricata specificando un percorso completo.

### <a name="alternate-search-order-for-uwp-apps"></a>Ordine di ricerca alternativo per le app UWP

Se un modulo modifica l'ordine di ricerca standard chiamando la funzione [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) con **Load \_ con \_ il \_ \_ percorso di ricerca modificato**, il sistema cerca nella directory in cui è stato caricato il modulo specificato anziché nella directory del processo chiamante. Il sistema esegue la ricerca di questi percorsi nell'ordine seguente:

1.  Grafico delle dipendenze del pacchetto del processo. Si tratta del pacchetto dell'applicazione più tutte le dipendenze specificate come `<PackageDependency>` nella `<Dependencies>` sezione del manifesto del pacchetto dell'applicazione. Le dipendenze vengono ricercate nell'ordine in cui sono visualizzate nel manifesto.
2.  Directory da cui è stato caricato il modulo specificato.
3.  Directory di sistema (% SystemRoot% \\ System32).

## <a name="search-order-for-desktop-applications"></a>Ordine di ricerca per le applicazioni desktop

Le applicazioni desktop possono controllare la posizione da cui viene caricata una DLL specificando un percorso completo, usando il [Reindirizzamento della dll](dynamic-link-library-redirection.md)o usando un [manifesto](/windows/desktop/SbsCs/manifests). Se nessuno di questi metodi viene usato, il sistema cerca la DLL in fase di caricamento, come descritto in questa sezione.

Prima che il sistema esegua la ricerca di una DLL, verifica quanto segue:

-   Se una DLL con lo stesso nome di modulo è già caricata in memoria, il sistema usa la DLL caricata, indipendentemente dalla directory in cui si trova. Il sistema non esegue la ricerca della DLL.
-   Se la DLL è nell'elenco di dll note per la versione di Windows in cui è in esecuzione l'applicazione, il sistema usa la copia della DLL nota (e le DLL dipendenti della DLL, se presenti). Il sistema non esegue la ricerca della DLL. Per un elenco di dll note nel sistema corrente, vedere la chiave del registro di sistema seguente: **HKEY \_ Local \_ Machine \\ System \\ CurrentControlSet \\ Control \\ Session Manager \\ KnownDLL**.

Se una DLL presenta dipendenze, il sistema cerca le DLL dipendenti come se fossero state caricate solo con i nomi dei moduli. Questo vale anche se la prima DLL è stata caricata specificando un percorso completo.

> [!IMPORTANT]
> Se un utente malintenzionato ottiene il controllo di una delle directory in cui viene eseguita la ricerca, può inserire una copia dannosa della DLL in tale directory. Per informazioni su come prevenire tali attacchi, vedere [sicurezza della libreria a collegamento dinamico](dynamic-link-library-security.md).

### <a name="standard-search-order-for-desktop-applications"></a>Ordine di ricerca standard per le applicazioni desktop

L'ordine di ricerca DLL standard utilizzato dal sistema dipende dall'abilitazione o disabilitazione della modalità di ricerca DLL sicura. La modalità di ricerca DLL sicura inserisce la directory corrente dell'utente in un secondo momento nell'ordine di ricerca.

La modalità di ricerca delle DLL sicure è abilitata per impostazione predefinita. Per disabilitare questa funzionalità, creare il valore del registro di **\_ sistema HKEY LOCAL \_ Machine \\ System \\ CurrentControlSet \\ Control \\ Session Manager** \\ **SafeDllSearchMode** e impostarlo su 0. La chiamata della funzione [**SetDllDirectory**](/windows/desktop/api/winbase/nf-winbase-setdlldirectorya) Disabilita **SafeDllSearchMode** mentre la directory specificata si trova nel percorso di ricerca e modifica l'ordine di ricerca come descritto in questo argomento.

Se **SafeDllSearchMode** è abilitata, l'ordine di ricerca è il seguente:

1.  Directory da cui è stata caricata l'applicazione.
2.  Directory di sistema. Usare la funzione [**GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) per ottenere il percorso di questa directory.
3.  Directory di sistema a 16 bit. Non esiste alcuna funzione che ottenga il percorso di questa directory, ma ne viene eseguita la ricerca.
4.  Directory di Windows. Usare la funzione [**GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) per ottenere il percorso di questa directory.
5.  La directory corrente.
6.  Directory elencate nella variabile di ambiente PATH. Si noti che questo non include il percorso per applicazione specificato dalla chiave del registro di sistema **percorsi app** . La chiave dei **percorsi dell'app** non viene usata per il calcolo del percorso di ricerca della dll.

Se **SafeDllSearchMode** è disabilitato, l'ordine di ricerca sarà il seguente:

1.  Directory da cui è stata caricata l'applicazione.
2.  La directory corrente.
3.  Directory di sistema. Usare la funzione [**GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) per ottenere il percorso di questa directory.
4.  Directory di sistema a 16 bit. Non esiste alcuna funzione che ottenga il percorso di questa directory, ma ne viene eseguita la ricerca.
5.  Directory di Windows. Usare la funzione [**GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) per ottenere il percorso di questa directory.
6.  Directory elencate nella variabile di ambiente PATH. Si noti che questo non include il percorso per applicazione specificato dalla chiave del registro di sistema **percorsi app** . La chiave dei **percorsi dell'app** non viene usata per il calcolo del percorso di ricerca della dll.

### <a name="alternate-search-order-for-desktop-applications"></a>Ordine di ricerca alternativo per le applicazioni desktop

È possibile modificare l'ordine di ricerca standard utilizzato dal sistema chiamando la funzione [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) con **Load \_ con \_ percorso di \_ ricerca \_ modificato**. È anche possibile modificare l'ordine di ricerca standard chiamando la funzione [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) .

> [!NOTE]
> Anche l'ordine di ricerca standard del processo sarà influenzato dalla chiamata della funzione [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) nel processo padre prima dell'avvio del processo corrente.

Se si specifica una strategia di ricerca alternativa, il comportamento continua fino a quando non sono stati individuati tutti i moduli eseguibili associati. Dopo che il sistema ha avviato l'elaborazione delle routine di inizializzazione della DLL, il sistema ripristina la strategia di ricerca standard.

La funzione [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) supporta un ordine di ricerca alternativo se la chiamata specifica **Load \_ con \_ \_ \_ percorso di ricerca modificato** e il parametro *lpFileName* specifica un percorso assoluto.

Si noti che la strategia di ricerca standard e la strategia di ricerca alternativa specificata da [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) con **Load \_ con \_ \_ \_ percorso di ricerca modificato** sono diverse in un solo modo: la ricerca standard inizia nella directory dell'applicazione chiamante e la ricerca alternativa inizia nella directory del modulo eseguibile che **LoadLibraryEx** sta caricando.

Se **SafeDllSearchMode** è abilitato, l'ordine di ricerca alternativo è il seguente:

1.  Directory specificata da *lpFileName*.
2.  Directory di sistema. Usare la funzione [**GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) per ottenere il percorso di questa directory.
3.  Directory di sistema a 16 bit. Non esiste alcuna funzione che ottenga il percorso di questa directory, ma ne viene eseguita la ricerca.
4.  Directory di Windows. Usare la funzione [**GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) per ottenere il percorso di questa directory.
5.  La directory corrente.
6.  Directory elencate nella variabile di ambiente PATH. Si noti che questo non include il percorso per applicazione specificato dalla chiave del registro di sistema **percorsi app** . La chiave dei **percorsi dell'app** non viene usata per il calcolo del percorso di ricerca della dll.

Se **SafeDllSearchMode** è disabilitato, l'ordine di ricerca alternativo è il seguente:

1.  Directory specificata da *lpFileName*.
2.  La directory corrente.
3.  Directory di sistema. Usare la funzione [**GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) per ottenere il percorso di questa directory.
4.  Directory di sistema a 16 bit. Non esiste alcuna funzione che ottenga il percorso di questa directory, ma ne viene eseguita la ricerca.
5.  Directory di Windows. Usare la funzione [**GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) per ottenere il percorso di questa directory.
6.  Directory elencate nella variabile di ambiente PATH. Si noti che questo non include il percorso per applicazione specificato dalla chiave del registro di sistema **percorsi app** . La chiave dei **percorsi dell'app** non viene usata per il calcolo del percorso di ricerca della dll.

La funzione [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) supporta un ordine di ricerca alternativo se il parametro *lpPathName* specifica un percorso. L'ordine di ricerca alternativo è il seguente:

1.  Directory da cui è stata caricata l'applicazione.
2.  Directory specificata dal parametro *lpPathName* di [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya).
3.  Directory di sistema. Usare la funzione [**GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) per ottenere il percorso di questa directory. Il nome di questa directory è system32.
4.  Directory di sistema a 16 bit. Non esiste alcuna funzione che ottenga il percorso di questa directory, ma ne viene eseguita la ricerca. Il nome di questa directory è System.
5.  Directory di Windows. Usare la funzione [**GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) per ottenere il percorso di questa directory.
6.  Directory elencate nella variabile di ambiente PATH. Si noti che questo non include il percorso per applicazione specificato dalla chiave del registro di sistema **percorsi app** . La chiave dei **percorsi dell'app** non viene usata per il calcolo del percorso di ricerca della dll.

Se il parametro *lpPathName* è una stringa vuota, la chiamata rimuove la directory corrente dall'ordine di ricerca.

[**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) Disabilita in modo efficace la modalità di ricerca dll sicura mentre la directory specificata si trova nel percorso di ricerca. Per ripristinare la modalità di ricerca DLL sicura in base al valore del registro di sistema **SafeDllSearchMode** e ripristinare la directory corrente nell'ordine di ricerca, chiamare **SetDllDirectory** con *lpPathName* come null.

### <a name="search-order-using-load_library_search-flags"></a>Ordine di ricerca usando i flag di **\_ \_ ricerca della libreria di caricamento**

Un'applicazione può specificare un ordine di ricerca usando uno o più flag di **\_ \_ ricerca della libreria di caricamento** con la funzione [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) . Un'applicazione può anche usare i flag di **\_ \_ ricerca della libreria di caricamento** con la funzione [**SetDefaultDllDirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories) per stabilire un ordine di ricerca dll per un processo. L'applicazione può specificare directory aggiuntive per l'ordine di ricerca DLL di processo usando le funzioni [**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory) o [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) .

Le directory di cui viene eseguita la ricerca dipendono dai flag specificati con [**SetDefaultDllDirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories) o [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa). Se viene utilizzato più di un flag, viene eseguita la ricerca nelle directory corrispondenti nell'ordine seguente:

1.  Directory che contiene la DLL (carica directory di **caricamento della DLL di \_ \_ ricerca della \_ \_ \_ libreria**). Questa directory viene cercata solo per le dipendenze della DLL da caricare.
2.  Directory dell'applicazione (**caricare la directory \_ \_ \_ dell' \_ applicazione di ricerca**).
3.  Percorsi aggiunti in modo esplicito con la funzione [**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory) (**Load \_ Library \_ Search \_ User \_ directory**) o la funzione [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) . Se è stato aggiunto più di un percorso, l'ordine in cui vengono cercati i percorsi non è specificato.
4.  La directory di sistema **( \_ carica \_ ricerca libreria \_ system32**).

Se l'applicazione non chiama [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) con alcun flag **di \_ \_ ricerca della libreria di caricamento** o stabilisce un ordine di ricerca dll per il processo, il sistema cerca le dll usando l'ordine di ricerca standard o l'ordine di ricerca alternativo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory)
</dt> <dt>

[Registrazione dell'applicazione](/windows/desktop/shell/app-registration)
</dt> <dt>

[Reindirizzamento libreria a collegamento dinamico](dynamic-link-library-redirection.md)
</dt> <dt>

[Sicurezza della libreria a collegamento dinamico](dynamic-link-library-security.md)
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

[Componenti affiancati](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal)
</dt> </dl>

 

 