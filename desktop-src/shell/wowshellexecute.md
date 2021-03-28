---
description: Esegue un'operazione su un file specificato.
ms.assetid: ce652565-40b6-4f69-bd2a-9e05e3f360ac
title: WOWShellExecute (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WOWShellExecute
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 841c30be827ddabc40bd8af50423c844ce927e6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524426"
---
# <a name="wowshellexecute-function"></a><span data-ttu-id="646fb-103">WOWShellExecute (funzione)</span><span class="sxs-lookup"><span data-stu-id="646fb-103">WOWShellExecute function</span></span>

<span data-ttu-id="646fb-104">\[Questa funzione è disponibile tramite Windows XP con Service Pack 2 (SP2) e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="646fb-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="646fb-105">Potrebbe essere modificato o non disponibile nelle versioni successive di Windows.\]</span><span class="sxs-lookup"><span data-stu-id="646fb-105">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="646fb-106">Esegue un'operazione su un file specificato.</span><span class="sxs-lookup"><span data-stu-id="646fb-106">Performs an operation on a specified file.</span></span> <span data-ttu-id="646fb-107">**WOWShellExecute** è disponibile solo per l'utilizzo con la macchina virtuale dos (Ntvdm.exe) di Microsoft Windows NT, che consente l'esecuzione di software DOS (Disk Operating System) e software a 16 bit in un sistema Windows e che non devono essere utilizzati da altri utenti.</span><span class="sxs-lookup"><span data-stu-id="646fb-107">**WOWShellExecute** exists only for use with the Microsoft Windows NT Virtual DOS Machine (Ntvdm.exe), which allows disk operating system (DOS) and 16-bit software to run on a Windows system, and should not be used by anyone else.</span></span> <span data-ttu-id="646fb-108">In alternativa, usare [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) .</span><span class="sxs-lookup"><span data-stu-id="646fb-108">Use [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="646fb-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="646fb-109">Syntax</span></span>


```C++
HINSTANCE WOWShellExecute(
  _In_ HWND    hwnd,
  _In_ LPCTSTR lpOperation,
  _In_ LPCTSTR lpFile,
  _In_ LPCTSTR lpParameters,
  _In_ LPCTSTR lpDirectory,
  _In_ INT     nShowCmd,
       void    *lpfnCBWinExec
);
```



## <a name="parameters"></a><span data-ttu-id="646fb-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="646fb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="646fb-111">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="646fb-111">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="646fb-112">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="646fb-112">Type: **HWND**</span></span>

<span data-ttu-id="646fb-113">Handle per la finestra proprietaria utilizzato per visualizzare un'interfaccia utente o messaggi di errore.</span><span class="sxs-lookup"><span data-stu-id="646fb-113">A handle to the owner window used for displaying a UI or error messages.</span></span> <span data-ttu-id="646fb-114">Questo valore può essere **null** se l'operazione non è associata a una finestra.</span><span class="sxs-lookup"><span data-stu-id="646fb-114">This value can be **NULL** if the operation is not associated with a window.</span></span>

</dd> <dt>

<span data-ttu-id="646fb-115">*lpOperation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="646fb-115">*lpOperation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="646fb-116">Tipo: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="646fb-116">Type: **LPCTSTR**</span></span>

<span data-ttu-id="646fb-117">Puntatore a una stringa con terminazione **null**, a cui si fa riferimento in questo caso come *verbo*, che specifica l'azione da eseguire.</span><span class="sxs-lookup"><span data-stu-id="646fb-117">A pointer to a **null**-terminated string, referred to in this case as a *verb*, that specifies the action to be performed.</span></span> <span data-ttu-id="646fb-118">Il set di verbi disponibili dipende dal file o dalla cartella specifica.</span><span class="sxs-lookup"><span data-stu-id="646fb-118">The set of available verbs depends on the particular file or folder.</span></span> <span data-ttu-id="646fb-119">In genere, le azioni disponibili dal menu di scelta rapida di un oggetto sono i verbi disponibili.</span><span class="sxs-lookup"><span data-stu-id="646fb-119">Generally, the actions available from an object's shortcut menu are available verbs.</span></span> <span data-ttu-id="646fb-120">Per ulteriori informazioni sui verbi e sulla relativa disponibilità, vedere la sezione relativa ai *verbi degli oggetti* di [avvio delle applicazioni](launch.md).</span><span class="sxs-lookup"><span data-stu-id="646fb-120">For more information about verbs and their availability, see the *Object Verbs* section of [Launching Applications](launch.md).</span></span> <span data-ttu-id="646fb-121">Per ulteriori informazioni sui menu di scelta rapida, vedere [estensione dei menu di scelta rapida](context.md) .</span><span class="sxs-lookup"><span data-stu-id="646fb-121">See [Extending Shortcut Menus](context.md) for further discussion of shortcut menus.</span></span> <span data-ttu-id="646fb-122">I verbi seguenti sono comunemente usati.</span><span class="sxs-lookup"><span data-stu-id="646fb-122">The following verbs are commonly used.</span></span>

<dt>

<span id="edit"></span><span id="EDIT"></span>

<span data-ttu-id="646fb-123"><span id="edit"></span><span id="EDIT"></span>**modifica**</span><span class="sxs-lookup"><span data-stu-id="646fb-123"><span id="edit"></span><span id="EDIT"></span>**edit**</span></span>


</dt> <dd>

<span data-ttu-id="646fb-124">Avvia un editor e apre il documento per la modifica.</span><span class="sxs-lookup"><span data-stu-id="646fb-124">Launches an editor and opens the document for editing.</span></span> <span data-ttu-id="646fb-125">Se *lpFile* non è un file di documento, la funzione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="646fb-125">If *lpFile* is not a document file, the function will fail.</span></span>

</dd> <dt>

<span id="explore"></span><span id="EXPLORE"></span>

<span data-ttu-id="646fb-126"><span id="explore"></span><span id="EXPLORE"></span>**esplorare**</span><span class="sxs-lookup"><span data-stu-id="646fb-126"><span id="explore"></span><span id="EXPLORE"></span>**explore**</span></span>


</dt> <dd>

<span data-ttu-id="646fb-127">Esplora la cartella specificata da *lpFile*.</span><span class="sxs-lookup"><span data-stu-id="646fb-127">Explores the folder specified by *lpFile*.</span></span>

</dd> <dt>

<span id="find"></span><span id="FIND"></span>

<span data-ttu-id="646fb-128"><span id="find"></span><span id="FIND"></span>**trovare**</span><span class="sxs-lookup"><span data-stu-id="646fb-128"><span id="find"></span><span id="FIND"></span>**find**</span></span>


</dt> <dd>

<span data-ttu-id="646fb-129">Avvia una ricerca a partire dalla directory specificata.</span><span class="sxs-lookup"><span data-stu-id="646fb-129">Initiates a search starting from the specified directory.</span></span>

</dd> <dt>

<span id="open"></span><span id="OPEN"></span>

<span data-ttu-id="646fb-130"><span id="open"></span><span id="OPEN"></span>**aprire**</span><span class="sxs-lookup"><span data-stu-id="646fb-130"><span id="open"></span><span id="OPEN"></span>**open**</span></span>


</dt> <dd>

<span data-ttu-id="646fb-131">Apre il file specificato dal parametro *lpFile* .</span><span class="sxs-lookup"><span data-stu-id="646fb-131">Opens the file specified by the *lpFile* parameter.</span></span> <span data-ttu-id="646fb-132">Il file può essere un file eseguibile, un file di documento o una cartella.</span><span class="sxs-lookup"><span data-stu-id="646fb-132">The file can be an executable file, a document file, or a folder.</span></span>

</dd> <dt>

<span id="print"></span><span id="PRINT"></span>

<span data-ttu-id="646fb-133"><span id="print"></span><span id="PRINT"></span>**stampa**</span><span class="sxs-lookup"><span data-stu-id="646fb-133"><span id="print"></span><span id="PRINT"></span>**print**</span></span>


</dt> <dd>

<span data-ttu-id="646fb-134">Stampa il file di documento specificato da *lpFile*.</span><span class="sxs-lookup"><span data-stu-id="646fb-134">Prints the document file specified by *lpFile*.</span></span> <span data-ttu-id="646fb-135">Se *lpFile* non è un file di documento, la funzione avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="646fb-135">If *lpFile* is not a document file, the function will fail.</span></span>

</dd> <dt>

<span id="NULL"></span><span id="null"></span>

<span data-ttu-id="646fb-136"><span id="NULL"></span><span id="null"></span>**NULL**</span><span class="sxs-lookup"><span data-stu-id="646fb-136"><span id="NULL"></span><span id="null"></span>**NULL**</span></span>


</dt> <dd>

<span data-ttu-id="646fb-137">Per i sistemi precedenti a Windows 2000, viene usato il verbo predefinito se è valido e disponibile nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="646fb-137">For systems prior to Windows 2000, the default verb is used if it is valid and available in the registry.</span></span> <span data-ttu-id="646fb-138">In caso contrario, viene utilizzato il verbo "Open".</span><span class="sxs-lookup"><span data-stu-id="646fb-138">If not, the "open" verb is used.</span></span>

<span data-ttu-id="646fb-139">Per i sistemi Windows 2000 e versioni successive, viene usato il verbo predefinito, se disponibile.</span><span class="sxs-lookup"><span data-stu-id="646fb-139">For Windows 2000 and later systems, the default verb is used if available.</span></span> <span data-ttu-id="646fb-140">In caso contrario, viene utilizzato il verbo "Open".</span><span class="sxs-lookup"><span data-stu-id="646fb-140">If not, the "open" verb is used.</span></span> <span data-ttu-id="646fb-141">Se nessuno dei due verbi è disponibile, il sistema usa il primo verbo elencato nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="646fb-141">If neither verb is available, the system uses the first verb listed in the registry.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="646fb-142">*lpFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="646fb-142">*lpFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="646fb-143">Tipo: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="646fb-143">Type: **LPCTSTR**</span></span>

<span data-ttu-id="646fb-144">Puntatore a una stringa con terminazione **null** che specifica il file o l'oggetto su cui eseguire il verbo specificato.</span><span class="sxs-lookup"><span data-stu-id="646fb-144">A pointer to a **null**-terminated string that specifies the file or object on which to execute the specified verb.</span></span> <span data-ttu-id="646fb-145">Per specificare un oggetto spazio dei nomi della shell, passare il nome completo dell'analisi.</span><span class="sxs-lookup"><span data-stu-id="646fb-145">To specify a Shell namespace object, pass the fully qualified parse name.</span></span> <span data-ttu-id="646fb-146">Si noti che non tutti i verbi sono supportati in tutti gli oggetti.</span><span class="sxs-lookup"><span data-stu-id="646fb-146">Note that not all verbs are supported on all objects.</span></span> <span data-ttu-id="646fb-147">Ad esempio, non tutti i tipi di documento supportano il verbo "Print".</span><span class="sxs-lookup"><span data-stu-id="646fb-147">For example, not all document types support the "print" verb.</span></span>

</dd> <dt>

<span data-ttu-id="646fb-148">*lpParameters* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="646fb-148">*lpParameters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="646fb-149">Tipo: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="646fb-149">Type: **LPCTSTR**</span></span>

<span data-ttu-id="646fb-150">Se il parametro *lpFile* specifica un file eseguibile, *lpParameters* è un puntatore a una stringa con terminazione **null** che specifica i parametri da passare all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="646fb-150">If the *lpFile* parameter specifies an executable file, *lpParameters* is a pointer to a **null**-terminated string that specifies the parameters to be passed to the application.</span></span> <span data-ttu-id="646fb-151">Il formato di questa stringa è determinato dal verbo da richiamare.</span><span class="sxs-lookup"><span data-stu-id="646fb-151">The format of this string is determined by the verb that is to be invoked.</span></span> <span data-ttu-id="646fb-152">Se *lpFile* specifica un file di documento, *LpParameters* deve essere **null**.</span><span class="sxs-lookup"><span data-stu-id="646fb-152">If *lpFile* specifies a document file, *lpParameters* should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="646fb-153">*lpDirectory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="646fb-153">*lpDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="646fb-154">Tipo: **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="646fb-154">Type: **LPCTSTR**</span></span>

<span data-ttu-id="646fb-155">Puntatore a una stringa con terminazione **null** che specifica la directory predefinita.</span><span class="sxs-lookup"><span data-stu-id="646fb-155">A pointer to a **null**-terminated string that specifies the default directory.</span></span>

</dd> <dt>

<span data-ttu-id="646fb-156">*nShowCmd* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="646fb-156">*nShowCmd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="646fb-157">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="646fb-157">Type: **INT**</span></span>

<span data-ttu-id="646fb-158">Flag che specificano la modalità di visualizzazione di un'applicazione all'apertura.</span><span class="sxs-lookup"><span data-stu-id="646fb-158">The flags that specify how an application is to be displayed when it is opened.</span></span> <span data-ttu-id="646fb-159">Se *lpFile* specifica un file di documento, il flag viene semplicemente passato all'applicazione associata.</span><span class="sxs-lookup"><span data-stu-id="646fb-159">If *lpFile* specifies a document file, the flag is simply passed to the associated application.</span></span> <span data-ttu-id="646fb-160">Spetta all'applicazione decidere come gestirla.</span><span class="sxs-lookup"><span data-stu-id="646fb-160">It is up to the application to decide how to handle it.</span></span>

<dt>

<span id="SW_HIDE"></span><span id="sw_hide"></span>

<span data-ttu-id="646fb-161"><span id="SW_HIDE"></span><span id="sw_hide"></span>**Nascondi il SW \_**</span><span class="sxs-lookup"><span data-stu-id="646fb-161"><span id="SW_HIDE"></span><span id="sw_hide"></span>**SW\_HIDE**</span></span>


</dt> <dd>

<span data-ttu-id="646fb-162">Nasconde la finestra e attiva un'altra finestra.</span><span class="sxs-lookup"><span data-stu-id="646fb-162">Hides the window and activates another window.</span></span>

</dd> <dt>

<span id="SW_MAXIMIZE"></span><span id="sw_maximize"></span>

<span data-ttu-id="646fb-163"><span id="SW_MAXIMIZE"></span><span id="sw_maximize"></span>**\_ingrandimento SW**</span><span class="sxs-lookup"><span data-stu-id="646fb-163"><span id="SW_MAXIMIZE"></span><span id="sw_maximize"></span>**SW\_MAXIMIZE**</span></span>


</dt> <dd>

<span data-ttu-id="646fb-164">Ingrandisce la finestra specificata.</span><span class="sxs-lookup"><span data-stu-id="646fb-164">Maximizes the specified window.</span></span>

</dd> <dt>

<span id="SW_MINIMIZE"></span><span id="sw_minimize"></span>

<span data-ttu-id="646fb-165"><span id="SW_MINIMIZE"></span><span id="sw_minimize"></span>**SW \_ Riduci a icona**</span><span class="sxs-lookup"><span data-stu-id="646fb-165"><span id="SW_MINIMIZE"></span><span id="sw_minimize"></span>**SW\_MINIMIZE**</span></span>


</dt> <dd>

<span data-ttu-id="646fb-166">Riduce a icona la finestra specificata e attiva la finestra di primo livello successiva nell'ordine z.</span><span class="sxs-lookup"><span data-stu-id="646fb-166">Minimizes the specified window and activates the next top-level window in the z-order.</span></span>

</dd> <dt>

<span id="SW_RESTORE"></span><span id="sw_restore"></span>

<span data-ttu-id="646fb-167"><span id="SW_RESTORE"></span><span id="sw_restore"></span>**\_ripristino SW**</span><span class="sxs-lookup"><span data-stu-id="646fb-167"><span id="SW_RESTORE"></span><span id="sw_restore"></span>**SW\_RESTORE**</span></span>


</dt> <dd>

<span data-ttu-id="646fb-168">Attiva e visualizza la finestra.</span><span class="sxs-lookup"><span data-stu-id="646fb-168">Activates and displays the window.</span></span> <span data-ttu-id="646fb-169">Se la finestra è ridotta a icona o ingrandita, Windows ne ripristina le dimensioni e la posizione originali.</span><span class="sxs-lookup"><span data-stu-id="646fb-169">If the window is minimized or maximized, Windows restores it to its original size and position.</span></span> <span data-ttu-id="646fb-170">Un'applicazione deve specificare questo flag durante il ripristino di una finestra ridotta a icona.</span><span class="sxs-lookup"><span data-stu-id="646fb-170">An application should specify this flag when restoring a minimized window.</span></span>

</dd> <dt>

<span id="SW_SHOW"></span><span id="sw_show"></span>

<span data-ttu-id="646fb-171"><span id="SW_SHOW"></span><span id="sw_show"></span>**\_visualizzazione SW**</span><span class="sxs-lookup"><span data-stu-id="646fb-171"><span id="SW_SHOW"></span><span id="sw_show"></span>**SW\_SHOW**</span></span>


</dt> <dd>

<span data-ttu-id="646fb-172">Attiva la finestra e la Visualizza nelle dimensioni e nella posizione correnti.</span><span class="sxs-lookup"><span data-stu-id="646fb-172">Activates the window and displays it in its current size and position.</span></span>

</dd> <dt>

<span id="SW_SHOWDEFAULT"></span><span id="sw_showdefault"></span>

<span data-ttu-id="646fb-173"><span id="SW_SHOWDEFAULT"></span><span id="sw_showdefault"></span>**\_SHOWDEFAULT SW**</span><span class="sxs-lookup"><span data-stu-id="646fb-173"><span id="SW_SHOWDEFAULT"></span><span id="sw_showdefault"></span>**SW\_SHOWDEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="646fb-174">Imposta lo stato di visualizzazione basato sul \_ flag SW specificato nella struttura [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) passata alla funzione [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) dal programma che ha avviato l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="646fb-174">Sets the show state based on the SW\_ flag specified in the [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) structure passed to the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) function by the program that started the application.</span></span> <span data-ttu-id="646fb-175">Un'applicazione deve chiamare [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) con questo flag per impostare lo stato di visualizzazione iniziale della finestra principale.</span><span class="sxs-lookup"><span data-stu-id="646fb-175">An application should call [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) with this flag to set the initial show state of its main window.</span></span>

</dd> <dt>

<span id="SW_SHOWMAXIMIZED"></span><span id="sw_showmaximized"></span>

<span data-ttu-id="646fb-176"><span id="SW_SHOWMAXIMIZED"></span><span id="sw_showmaximized"></span>**\_SHOWMAXIMIZED SW**</span><span class="sxs-lookup"><span data-stu-id="646fb-176"><span id="SW_SHOWMAXIMIZED"></span><span id="sw_showmaximized"></span>**SW\_SHOWMAXIMIZED**</span></span>


</dt> <dd>

<span data-ttu-id="646fb-177">Attiva la finestra e la Visualizza come finestra ingrandita.</span><span class="sxs-lookup"><span data-stu-id="646fb-177">Activates the window and displays it as a maximized window.</span></span>

</dd> <dt>

<span id="SW_SHOWMINIMIZED"></span><span id="sw_showminimized"></span>

<span data-ttu-id="646fb-178"><span id="SW_SHOWMINIMIZED"></span><span id="sw_showminimized"></span>**\_SHOWMINIMIZED SW**</span><span class="sxs-lookup"><span data-stu-id="646fb-178"><span id="SW_SHOWMINIMIZED"></span><span id="sw_showminimized"></span>**SW\_SHOWMINIMIZED**</span></span>


</dt> <dd>

<span data-ttu-id="646fb-179">Attiva la finestra e la Visualizza come finestra ridotta a icona.</span><span class="sxs-lookup"><span data-stu-id="646fb-179">Activates the window and displays it as a minimized window.</span></span>

</dd> <dt>

<span id="SW_SHOWMINNOACTIVE"></span><span id="sw_showminnoactive"></span>

<span data-ttu-id="646fb-180"><span id="SW_SHOWMINNOACTIVE"></span><span id="sw_showminnoactive"></span>**\_SHOWMINNOACTIVE SW**</span><span class="sxs-lookup"><span data-stu-id="646fb-180"><span id="SW_SHOWMINNOACTIVE"></span><span id="sw_showminnoactive"></span>**SW\_SHOWMINNOACTIVE**</span></span>


</dt> <dd>

<span data-ttu-id="646fb-181">Visualizza la finestra come finestra ridotta a icona.</span><span class="sxs-lookup"><span data-stu-id="646fb-181">Displays the window as a minimized window.</span></span> <span data-ttu-id="646fb-182">La finestra attiva rimane attiva.</span><span class="sxs-lookup"><span data-stu-id="646fb-182">The active window remains active.</span></span>

</dd> <dt>

<span id="SW_SHOWNA"></span><span id="sw_showna"></span>

<span data-ttu-id="646fb-183"><span id="SW_SHOWNA"></span><span id="sw_showna"></span>**SW \_ visualizzato**</span><span class="sxs-lookup"><span data-stu-id="646fb-183"><span id="SW_SHOWNA"></span><span id="sw_showna"></span>**SW\_SHOWNA**</span></span>


</dt> <dd>

<span data-ttu-id="646fb-184">Consente di visualizzare la finestra nello stato corrente.</span><span class="sxs-lookup"><span data-stu-id="646fb-184">Displays the window in its current state.</span></span> <span data-ttu-id="646fb-185">La finestra attiva rimane attiva.</span><span class="sxs-lookup"><span data-stu-id="646fb-185">The active window remains active.</span></span>

</dd> <dt>

<span id="SW_SHOWNOACTIVATE"></span><span id="sw_shownoactivate"></span>

<span data-ttu-id="646fb-186"><span id="SW_SHOWNOACTIVATE"></span><span id="sw_shownoactivate"></span>**\_SHOWNOACTIVATE SW**</span><span class="sxs-lookup"><span data-stu-id="646fb-186"><span id="SW_SHOWNOACTIVATE"></span><span id="sw_shownoactivate"></span>**SW\_SHOWNOACTIVATE**</span></span>


</dt> <dd>

<span data-ttu-id="646fb-187">Visualizza una finestra nelle dimensioni e nella posizione più recenti.</span><span class="sxs-lookup"><span data-stu-id="646fb-187">Displays a window in its most recent size and position.</span></span> <span data-ttu-id="646fb-188">La finestra attiva rimane attiva.</span><span class="sxs-lookup"><span data-stu-id="646fb-188">The active window remains active.</span></span>

</dd> <dt>

<span id="SW_SHOWNORMAL"></span><span id="sw_shownormal"></span>

<span data-ttu-id="646fb-189"><span id="SW_SHOWNORMAL"></span><span id="sw_shownormal"></span>**\_SHOWNORMAL SW**</span><span class="sxs-lookup"><span data-stu-id="646fb-189"><span id="SW_SHOWNORMAL"></span><span id="sw_shownormal"></span>**SW\_SHOWNORMAL**</span></span>


</dt> <dd>

<span data-ttu-id="646fb-190">Attiva e visualizza una finestra.</span><span class="sxs-lookup"><span data-stu-id="646fb-190">Activates and displays a window.</span></span> <span data-ttu-id="646fb-191">Se la finestra è ridotta a icona o ingrandita, Windows ne ripristina le dimensioni e la posizione originali.</span><span class="sxs-lookup"><span data-stu-id="646fb-191">If the window is minimized or maximized, Windows restores it to its original size and position.</span></span> <span data-ttu-id="646fb-192">Un'applicazione deve specificare questo flag quando la finestra viene visualizzata per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="646fb-192">An application should specify this flag when displaying the window for the first time.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="646fb-193">*lpfnCBWinExec*</span><span class="sxs-lookup"><span data-stu-id="646fb-193">*lpfnCBWinExec*</span></span> 
</dt> <dd>

<span data-ttu-id="646fb-194">Tipo: \**void \** _</span><span class="sxs-lookup"><span data-stu-id="646fb-194">Type: \**void\** _</span></span>

<span data-ttu-id="646fb-195">Funzione di callback utilizzata per chiamare [_ *CreateProcess* \*](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) nel kernel a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="646fb-195">Callback function used to call [_ *CreateProcess*\*](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) in the 16-bit kernel.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="646fb-196">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="646fb-196">Return value</span></span>

<span data-ttu-id="646fb-197">Tipo: **HINSTANCE**</span><span class="sxs-lookup"><span data-stu-id="646fb-197">Type: **HINSTANCE**</span></span>

<span data-ttu-id="646fb-198">Restituisce un valore maggiore di 32 in caso di esito positivo o un valore di errore minore o uguale a 32 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="646fb-198">Returns a value greater than 32 if successful, or an error value that is less than or equal to 32 otherwise.</span></span> <span data-ttu-id="646fb-199">Nella tabella seguente sono elencati i valori di errore.</span><span class="sxs-lookup"><span data-stu-id="646fb-199">The following table lists the error values.</span></span> <span data-ttu-id="646fb-200">Viene eseguito il cast del valore restituito come HINSTANCE per la compatibilità con le versioni precedenti delle applicazioni Windows a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="646fb-200">The return value is cast as an HINSTANCE for backward compatibility with 16-bit Windows applications.</span></span> <span data-ttu-id="646fb-201">Tuttavia, non si tratta di un vero e proprio HINSTANCE.</span><span class="sxs-lookup"><span data-stu-id="646fb-201">It is not a true HINSTANCE, however.</span></span> <span data-ttu-id="646fb-202">L'unica cosa che può essere eseguita con il HINSTANCE restituito è eseguirne il cast a un valore **int** e confrontarlo con il valore 32 o uno dei codici di errore riportati di seguito.</span><span class="sxs-lookup"><span data-stu-id="646fb-202">The only thing that can be done with the returned HINSTANCE is to cast it to an **int** and compare it with the value 32 or one of the error codes below.</span></span>



| <span data-ttu-id="646fb-203">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="646fb-203">Return code</span></span>                                                                                             | <span data-ttu-id="646fb-204">Descrizione</span><span class="sxs-lookup"><span data-stu-id="646fb-204">Description</span></span>                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="646fb-205"><dt>**0**</dt></span><span class="sxs-lookup"><span data-stu-id="646fb-205"><dt>**0**</dt></span></span> </dl>                        | <span data-ttu-id="646fb-206">Memoria o risorse insufficienti per il sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="646fb-206">The operating system is out of memory or resources.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="646fb-207"><dt>**FILE di errore \_ \_ non \_ trovato**</dt></span><span class="sxs-lookup"><span data-stu-id="646fb-207"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt></span></span> </dl>  | <span data-ttu-id="646fb-208">Il file specificato non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="646fb-208">The specified file was not found.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="646fb-209"><dt>**il percorso dell'errore non è stato \_ \_ \_ trovato**</dt></span><span class="sxs-lookup"><span data-stu-id="646fb-209"><dt>**ERROR\_PATH\_NOT\_FOUND**</dt></span></span> </dl>  | <span data-ttu-id="646fb-210">Il percorso specificato non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="646fb-210">The specified path was not found.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="646fb-211"><dt>**\_formato errore errato \_**</dt></span><span class="sxs-lookup"><span data-stu-id="646fb-211"><dt>**ERROR\_BAD\_FORMAT**</dt></span></span> </dl>       | <span data-ttu-id="646fb-212">Il file exe non è valido (non Win32. exe o errore nell'immagine exe).</span><span class="sxs-lookup"><span data-stu-id="646fb-212">The .exe file is invalid (non-Win32 .exe or error in .exe image).</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="646fb-213"><dt>**SE \_ Err \_ AccessDenied**</dt></span><span class="sxs-lookup"><span data-stu-id="646fb-213"><dt>**SE\_ERR\_ACCESSDENIED**</dt></span></span> </dl>    | <span data-ttu-id="646fb-214">Il sistema operativo ha negato l'accesso al file specificato.</span><span class="sxs-lookup"><span data-stu-id="646fb-214">The operating system denied access to the specified file.</span></span><br/>                                                                                                     |
| <dl> <span data-ttu-id="646fb-215"><dt>**SE \_ Err \_ ASSOCINCOMPLETE**</dt></span><span class="sxs-lookup"><span data-stu-id="646fb-215"><dt>**SE\_ERR\_ASSOCINCOMPLETE**</dt></span></span> </dl> | <span data-ttu-id="646fb-216">L'associazione del nome file è incompleta o non valida.</span><span class="sxs-lookup"><span data-stu-id="646fb-216">The file name association is incomplete or invalid.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="646fb-217"><dt>**SE \_ Err \_ DDEBUSY**</dt></span><span class="sxs-lookup"><span data-stu-id="646fb-217"><dt>**SE\_ERR\_DDEBUSY**</dt></span></span> </dl>         | <span data-ttu-id="646fb-218">Non è stato possibile completare la transazione DDE perché sono in corso l'elaborazione di altre transazioni DDE.</span><span class="sxs-lookup"><span data-stu-id="646fb-218">The DDE transaction could not be completed because other DDE transactions were being processed.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="646fb-219"><dt>**SE \_ Err \_ DDEFAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="646fb-219"><dt>**SE\_ERR\_DDEFAIL**</dt></span></span> </dl>         | <span data-ttu-id="646fb-220">Transazione DDE non riuscita.</span><span class="sxs-lookup"><span data-stu-id="646fb-220">The DDE transaction failed.</span></span><br/>                                                                                                                                   |
| <dl> <span data-ttu-id="646fb-221"><dt>**SE \_ Err \_ DDETIMEOUT**</dt></span><span class="sxs-lookup"><span data-stu-id="646fb-221"><dt>**SE\_ERR\_DDETIMEOUT**</dt></span></span> </dl>      | <span data-ttu-id="646fb-222">Non è stato possibile completare la transazione DDE perché si è verificato il timeout della richiesta.</span><span class="sxs-lookup"><span data-stu-id="646fb-222">The DDE transaction could not be completed because the request timed out.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="646fb-223"><dt>**SE \_ Err \_ DLLNOTFOUND**</dt></span><span class="sxs-lookup"><span data-stu-id="646fb-223"><dt>**SE\_ERR\_DLLNOTFOUND**</dt></span></span> </dl>     | <span data-ttu-id="646fb-224">Impossibile trovare la DLL specificata.</span><span class="sxs-lookup"><span data-stu-id="646fb-224">The specified DLL was not found.</span></span><br/>                                                                                                                              |
| <dl> <span data-ttu-id="646fb-225"><dt>**SE \_ Err \_ FNF**</dt></span><span class="sxs-lookup"><span data-stu-id="646fb-225"><dt>**SE\_ERR\_FNF**</dt></span></span> </dl>             | <span data-ttu-id="646fb-226">Il file specificato non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="646fb-226">The specified file was not found.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="646fb-227"><dt>**SE \_ Err \_ NOASSOC**</dt></span><span class="sxs-lookup"><span data-stu-id="646fb-227"><dt>**SE\_ERR\_NOASSOC**</dt></span></span> </dl>         | <span data-ttu-id="646fb-228">All'estensione di file specificata non è associata alcuna applicazione.</span><span class="sxs-lookup"><span data-stu-id="646fb-228">There is no application associated with the given file name extension.</span></span> <span data-ttu-id="646fb-229">Questo errore viene restituito anche se si tenta di stampare un file non stampabile.</span><span class="sxs-lookup"><span data-stu-id="646fb-229">This error will also be returned if you attempt to print a file that is not printable.</span></span><br/> |
| <dl> <span data-ttu-id="646fb-230"><dt>**SE \_ Err \_**</dt></span><span class="sxs-lookup"><span data-stu-id="646fb-230"><dt>**SE\_ERR\_OOM**</dt></span></span> </dl>             | <span data-ttu-id="646fb-231">Memoria insufficiente per completare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="646fb-231">There was not enough memory to complete the operation.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="646fb-232"><dt>**SE \_ Err \_ PNF**</dt></span><span class="sxs-lookup"><span data-stu-id="646fb-232"><dt>**SE\_ERR\_PNF**</dt></span></span> </dl>             | <span data-ttu-id="646fb-233">Il percorso specificato non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="646fb-233">The specified path was not found.</span></span><br/>                                                                                                                             |
| <dl> <span data-ttu-id="646fb-234"><dt>**SE \_ Err, \_ condivisione**</dt></span><span class="sxs-lookup"><span data-stu-id="646fb-234"><dt>**SE\_ERR\_SHARE**</dt></span></span> </dl>           | <span data-ttu-id="646fb-235">Si è verificata una violazione di condivisione.</span><span class="sxs-lookup"><span data-stu-id="646fb-235">A sharing violation occurred.</span></span><br/>                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="646fb-236">Commenti</span><span class="sxs-lookup"><span data-stu-id="646fb-236">Remarks</span></span>

<span data-ttu-id="646fb-237">**WOWShellExecute** non è incluso in un'intestazione o in un file con estensione LIB.</span><span class="sxs-lookup"><span data-stu-id="646fb-237">**WOWShellExecute** is not included in a header or .lib file.</span></span> <span data-ttu-id="646fb-238">Viene esportato da Shell32.dll in base al nome.</span><span class="sxs-lookup"><span data-stu-id="646fb-238">It is exported from Shell32.dll by name.</span></span>

<span data-ttu-id="646fb-239">Questo metodo consente di eseguire qualsiasi comando nel menu di scelta rapida di una cartella o di archiviarlo nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="646fb-239">This method allows you to execute any commands in a folder's shortcut menu or stored in the registry.</span></span>

<span data-ttu-id="646fb-240">Se *lpOperation* è **null**, la funzione apre il file specificato da *lpFile*.</span><span class="sxs-lookup"><span data-stu-id="646fb-240">If *lpOperation* is **NULL**, the function opens the file specified by *lpFile*.</span></span> <span data-ttu-id="646fb-241">Se *lpOperation* è "Open" o "Explore", la funzione tenta di aprire o esplorare la cartella.</span><span class="sxs-lookup"><span data-stu-id="646fb-241">If *lpOperation* is "open" or "explore", the function attempts to open or explore the folder.</span></span>

<span data-ttu-id="646fb-242">Per ottenere informazioni sull'applicazione avviata come risultato della chiamata a **WOWShellExecute**, utilizzare [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span><span class="sxs-lookup"><span data-stu-id="646fb-242">To obtain information about the application that is launched as a result of calling **WOWShellExecute**, use [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).</span></span>

> [!Note]  
> <span data-ttu-id="646fb-243">Le **finestre della cartella di avvio in un'impostazione di processo separata** in Opzioni cartella influiscono su **WOWShellExecute**.</span><span class="sxs-lookup"><span data-stu-id="646fb-243">The **Launch folder windows in a separate process** setting in Folder Options affects **WOWShellExecute**.</span></span> <span data-ttu-id="646fb-244">Se questa opzione è disabilitata (impostazione predefinita), **WOWShellExecute** usa una finestra di Esplora risorse anziché avviarne una nuova.</span><span class="sxs-lookup"><span data-stu-id="646fb-244">If that option is disabled (the default setting), **WOWShellExecute** uses an open Explorer window rather than launch a new one.</span></span> <span data-ttu-id="646fb-245">Se non è aperta alcuna finestra di Esplora risorse, **WOWShellExecute** ne avvia una nuova.</span><span class="sxs-lookup"><span data-stu-id="646fb-245">If no Explorer window is open, **WOWShellExecute** launches a new one.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="646fb-246">Requisiti</span><span class="sxs-lookup"><span data-stu-id="646fb-246">Requirements</span></span>



| <span data-ttu-id="646fb-247">Requisito</span><span class="sxs-lookup"><span data-stu-id="646fb-247">Requirement</span></span> | <span data-ttu-id="646fb-248">Valore</span><span class="sxs-lookup"><span data-stu-id="646fb-248">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="646fb-249">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="646fb-249">Minimum supported client</span></span><br/> | <span data-ttu-id="646fb-250">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="646fb-250">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="646fb-251">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="646fb-251">Minimum supported server</span></span><br/> | <span data-ttu-id="646fb-252">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="646fb-252">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="646fb-253">DLL</span><span class="sxs-lookup"><span data-stu-id="646fb-253">DLL</span></span><br/>                      | <dl> <span data-ttu-id="646fb-254"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="646fb-254"><dt>Shell32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="646fb-255">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="646fb-255">See also</span></span>

<dl> <dt>

[<span data-ttu-id="646fb-256">**ShellExecute**</span><span class="sxs-lookup"><span data-stu-id="646fb-256">**ShellExecute**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)
</dt> </dl>

 

 
