---
description: Questo argomento contiene informazioni sulle API di basso livello usate dall'infrastruttura client di Windows.
ms.assetid: 14a6e970-2032-420e-9930-a15909dbbb97
title: Supporto client vario Low-Level
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11558c9994a9c622f71e803521352d1073e68c05
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877145"
---
# <a name="miscellaneous-low-level-client-support"></a><span data-ttu-id="39fb7-103">Supporto client vario Low-Level</span><span class="sxs-lookup"><span data-stu-id="39fb7-103">Miscellaneous Low-Level Client Support</span></span>

<span data-ttu-id="39fb7-104">Questo argomento contiene informazioni sulle API di basso livello usate dall'infrastruttura client di Windows.</span><span class="sxs-lookup"><span data-stu-id="39fb7-104">This topic contains information about low-level APIs that are used by the Windows client infrastructure.</span></span>

### <a name="functions"></a><span data-ttu-id="39fb7-105">Funzioni</span><span class="sxs-lookup"><span data-stu-id="39fb7-105">Functions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="39fb7-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="39fb7-106">Topic</span></span></th>
<th><span data-ttu-id="39fb7-107">Contenuto</span><span class="sxs-lookup"><span data-stu-id="39fb7-107">Contents</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="39fb7-108"><a href="/windows/desktop/api/winbase/nf-winbase-_lclose"><strong>_lclose</strong></a></span><span class="sxs-lookup"><span data-stu-id="39fb7-108"><a href="/windows/desktop/api/winbase/nf-winbase-_lclose"><strong>_lclose</strong></a></span></span></td>
<td><span data-ttu-id="39fb7-109">La funzione _lclose chiude il file specificato in modo che non sia più disponibile per la lettura o la scrittura.</span><span class="sxs-lookup"><span data-stu-id="39fb7-109">The _lclose function closes the specified file so that it is no longer available for reading or writing.</span></span> <span data-ttu-id="39fb7-110">Questa funzione viene fornita per la compatibilità con le versioni di Windows a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="39fb7-110">This function is provided for compatibility with 16-bit versions of Windows.</span></span> <span data-ttu-id="39fb7-111">Le applicazioni basate su Win32 devono usare la funzione CloseHandle.</span><span class="sxs-lookup"><span data-stu-id="39fb7-111">Win32-based applications should use the CloseHandle function.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39fb7-112"><a href="/windows/desktop/api/winbase/nf-winbase-_lopen"><strong>_lopen</strong></a></span><span class="sxs-lookup"><span data-stu-id="39fb7-112"><a href="/windows/desktop/api/winbase/nf-winbase-_lopen"><strong>_lopen</strong></a></span></span></td>
<td><span data-ttu-id="39fb7-113">La funzione _lopen apre un file esistente e imposta il puntatore del file all'inizio del file.</span><span class="sxs-lookup"><span data-stu-id="39fb7-113">The _lopen function opens an existing file and sets the file pointer to the beginning of the file.</span></span> <span data-ttu-id="39fb7-114">Questa funzione viene fornita per la compatibilità con le versioni di Windows a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="39fb7-114">This function is provided for compatibility with 16-bit versions of Windows.</span></span> <span data-ttu-id="39fb7-115">Le applicazioni basate su Win32 devono utilizzare la funzione CreateFile.</span><span class="sxs-lookup"><span data-stu-id="39fb7-115">Win32-based applications should use the CreateFile function.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="39fb7-116"><a href="/windows/desktop/api/winbase/nf-winbase-_lread"><strong>_lread</strong></a></span><span class="sxs-lookup"><span data-stu-id="39fb7-116"><a href="/windows/desktop/api/winbase/nf-winbase-_lread"><strong>_lread</strong></a></span></span></td>
<td><span data-ttu-id="39fb7-117">La funzione _lread legge i dati dal file specificato.</span><span class="sxs-lookup"><span data-stu-id="39fb7-117">The _lread function reads data from the specified file.</span></span> <span data-ttu-id="39fb7-118">Questa funzione viene fornita per la compatibilità con le versioni di Windows a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="39fb7-118">This function is provided for compatibility with 16-bit versions of Windows.</span></span> <span data-ttu-id="39fb7-119">Le applicazioni basate su Win32 devono usare la funzione ReadFile.</span><span class="sxs-lookup"><span data-stu-id="39fb7-119">Win32-based applications should use the ReadFile function.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39fb7-120"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-aredvdcodecsenabled"><strong>AreDvdCodecsEnabled</strong></a></span><span class="sxs-lookup"><span data-stu-id="39fb7-120"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-aredvdcodecsenabled"><strong>AreDvdCodecsEnabled</strong></a></span></span></td>
<td><span data-ttu-id="39fb7-121">Restituisce un valore che indica se i codec DVD sono abilitati nel dispositivo corrente.</span><span class="sxs-lookup"><span data-stu-id="39fb7-121">Returns a value indicating whether DVD codecs are enabled on the current device.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="39fb7-122"><a href="/windows/desktop/api/Winuser/nf-winuser-disableprocesswindowsghosting"><strong>DisableProcessWindowsGhosting</strong></a></span><span class="sxs-lookup"><span data-stu-id="39fb7-122"><a href="/windows/desktop/api/Winuser/nf-winuser-disableprocesswindowsghosting"><strong>DisableProcessWindowsGhosting</strong></a></span></span></td>
<td><span data-ttu-id="39fb7-123">Disabilita la funzionalità di ghosting della finestra per il processo GUI chiamante.</span><span class="sxs-lookup"><span data-stu-id="39fb7-123">Disables the window ghosting feature for the calling GUI process.</span></span> <span data-ttu-id="39fb7-124">Il fantasma della finestra è una funzionalità di Windows Manager che consente all'utente di ridurre, spostare o chiudere la finestra principale di un'applicazione che non risponde.</span><span class="sxs-lookup"><span data-stu-id="39fb7-124">Window ghosting is a Windows Manager feature that lets the user minimize, move, or close the main window of an application that is not responding.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39fb7-125"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-getmediacomponentpackageinfo"><strong>GetMediaComponentPackageInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="39fb7-125"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-getmediacomponentpackageinfo"><strong>GetMediaComponentPackageInfo</strong></a></span></span></td>
<td><span data-ttu-id="39fb7-126">Restituisce un elenco di proprietà per tutti i codec multimediali installati nel sistema che soddisfano i requisiti specificati.</span><span class="sxs-lookup"><span data-stu-id="39fb7-126">Returns a list of properties for all media codecs installed on the system that meet the specified requirements.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="39fb7-127"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-getmediaextensioncommunicationfactory"><strong>GetMediaExtensionCommunicationFactory</strong></a></span><span class="sxs-lookup"><span data-stu-id="39fb7-127"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-getmediaextensioncommunicationfactory"><strong>GetMediaExtensionCommunicationFactory</strong></a></span></span></td>
<td><span data-ttu-id="39fb7-128">Crea una factory di comunicazione per la registrazione di un'estensione per supporti.</span><span class="sxs-lookup"><span data-stu-id="39fb7-128">Creates a communication factory for registering a media extension.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39fb7-129"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-instantiatecomponentfrompackage"><strong>InstantiateComponentFromPackage</strong></a></span><span class="sxs-lookup"><span data-stu-id="39fb7-129"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-instantiatecomponentfrompackage"><strong>InstantiateComponentFromPackage</strong></a></span></span></td>
<td><span data-ttu-id="39fb7-130">Crea un'istanza di una classe in un pacchetto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="39fb7-130">Creates an instance of a class in an application package.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="39fb7-131"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-ismediabehaviorenabled"><strong>IsMediaBehaviorEnabled</strong></a></span><span class="sxs-lookup"><span data-stu-id="39fb7-131"><a href="/windows/desktop/api/comppkgsup/nf-comppkgsup-ismediabehaviorenabled"><strong>IsMediaBehaviorEnabled</strong></a></span></span></td>
<td><span data-ttu-id="39fb7-132">Ottiene un valore che indica se il comportamento del supporto associato al GUID specificato è abilitato.</span><span class="sxs-lookup"><span data-stu-id="39fb7-132">Gets a value indicating whether the media behavior associated with the specified GUID is enabled.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39fb7-133"><a href="/windows/desktop/api/Winternl/nf-winternl-ntclose"><strong>NtClose</strong></a></span><span class="sxs-lookup"><span data-stu-id="39fb7-133"><a href="/windows/desktop/api/Winternl/nf-winternl-ntclose"><strong>NtClose</strong></a></span></span></td>
<td><span data-ttu-id="39fb7-134">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="39fb7-134">Deprecated.</span></span> <span data-ttu-id="39fb7-135">Questa funzione viene utilizzata per chiudere l'handle specificato.</span><span class="sxs-lookup"><span data-stu-id="39fb7-135">This function is used to close the specified handle.</span></span> <span data-ttu-id="39fb7-136"><a href="/windows/desktop/api/Winternl/nf-winternl-ntclose"><strong>NtClose</strong></a> viene sostituito da <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>.</span><span class="sxs-lookup"><span data-stu-id="39fb7-136"><a href="/windows/desktop/api/Winternl/nf-winternl-ntclose"><strong>NtClose</strong></a> is superseded by <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="39fb7-137"><a href="/windows/desktop/api/Winternl/nf-winternl-ntdeviceiocontrolfile"><strong>NtDeviceIoControlFile</strong></a></span><span class="sxs-lookup"><span data-stu-id="39fb7-137"><a href="/windows/desktop/api/Winternl/nf-winternl-ntdeviceiocontrolfile"><strong>NtDeviceIoControlFile</strong></a></span></span></td>
<td><span data-ttu-id="39fb7-138">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="39fb7-138">Deprecated.</span></span> <span data-ttu-id="39fb7-139">Compila i descrittori per i buffer forniti e passa i dati non tipizzati al driver di dispositivo associato all'handle di file.</span><span class="sxs-lookup"><span data-stu-id="39fb7-139">Builds descriptors for the supplied buffer(s) and passes the untyped data to the device driver associated with the file handle.</span></span> <span data-ttu-id="39fb7-140"><a href="/windows/desktop/api/Winternl/nf-winternl-ntdeviceiocontrolfile"><strong>NtDeviceIoControlFile</strong></a> viene sostituito da <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>.</span><span class="sxs-lookup"><span data-stu-id="39fb7-140"><a href="/windows/desktop/api/Winternl/nf-winternl-ntdeviceiocontrolfile"><strong>NtDeviceIoControlFile</strong></a> is superseded by <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39fb7-141"><a href="/windows/desktop/api/Winternl/nf-winternl-ntwaitforsingleobject"><strong>NtWaitForSingleObject</strong></a></span><span class="sxs-lookup"><span data-stu-id="39fb7-141"><a href="/windows/desktop/api/Winternl/nf-winternl-ntwaitforsingleobject"><strong>NtWaitForSingleObject</strong></a></span></span></td>
<td><span data-ttu-id="39fb7-142">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="39fb7-142">Deprecated.</span></span> <span data-ttu-id="39fb7-143">Attende che l'oggetto specificato raggiunga uno stato <code>signaled</code> .</span><span class="sxs-lookup"><span data-stu-id="39fb7-143">Waits until the specified object attains a state of <code>signaled</code>.</span></span> <span data-ttu-id="39fb7-144"><a href="/windows/desktop/api/Winternl/nf-winternl-ntwaitforsingleobject"><strong>NtWaitForSingleObject</strong></a> viene sostituito da <a href="/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject">WaitForSingleObject</a>.</span><span class="sxs-lookup"><span data-stu-id="39fb7-144"><a href="/windows/desktop/api/Winternl/nf-winternl-ntwaitforsingleobject"><strong>NtWaitForSingleObject</strong></a> is superseded by <a href="/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject">WaitForSingleObject</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="39fb7-145"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlansistringtounicodestring"><strong>RtlAnsiStringToUnicodeString</strong></a></span><span class="sxs-lookup"><span data-stu-id="39fb7-145"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlansistringtounicodestring"><strong>RtlAnsiStringToUnicodeString</strong></a></span></span></td>
<td><span data-ttu-id="39fb7-146">Converte la stringa di origine ANSI specificata in una stringa Unicode.</span><span class="sxs-lookup"><span data-stu-id="39fb7-146">Converts the specified ANSI source string into a Unicode string.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39fb7-147"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlchartointeger"><strong>RtlCharToInteger</strong></a></span><span class="sxs-lookup"><span data-stu-id="39fb7-147"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlchartointeger"><strong>RtlCharToInteger</strong></a></span></span></td>
<td><span data-ttu-id="39fb7-148">Converte una stringa di caratteri in un Integer.</span><span class="sxs-lookup"><span data-stu-id="39fb7-148">Converts a character string to an integer.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="39fb7-149"><a href="/previous-versions//ff899322(v=vs.85)"><strong>RtlFormatCurrentUserKeyPath</strong></a></span><span class="sxs-lookup"><span data-stu-id="39fb7-149"><a href="/previous-versions//ff899322(v=vs.85)"><strong>RtlFormatCurrentUserKeyPath</strong></a></span></span></td>
<td><span data-ttu-id="39fb7-150">Inizializza il buffer fornito con una rappresentazione di stringa del SID per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="39fb7-150">Initializes the supplied buffer with a string representation of the SID for the current user.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39fb7-151"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeansistring"><strong>RtlFreeAnsiString</strong></a></span><span class="sxs-lookup"><span data-stu-id="39fb7-151"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeansistring"><strong>RtlFreeAnsiString</strong></a></span></span></td>
<td><span data-ttu-id="39fb7-152">Libera il buffer di stringa allocato da <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtoansistring"><strong>RtlUnicodeStringToAnsiString</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="39fb7-152">Frees the string buffer allocated by <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtoansistring"><strong>RtlUnicodeStringToAnsiString</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="39fb7-153"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeoemstring"><strong>RtlFreeOemString</strong></a></span><span class="sxs-lookup"><span data-stu-id="39fb7-153"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeoemstring"><strong>RtlFreeOemString</strong></a></span></span></td>
<td><span data-ttu-id="39fb7-154">Libera il buffer di stringa allocato da <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring"><strong>RtlUnicodeStringToOemString</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="39fb7-154">Frees the string buffer allocated by <a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring"><strong>RtlUnicodeStringToOemString</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39fb7-155"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeunicodestring"><strong>RtlFreeUnicodeString</strong></a></span><span class="sxs-lookup"><span data-stu-id="39fb7-155"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlfreeunicodestring"><strong>RtlFreeUnicodeString</strong></a></span></span></td>
<td><span data-ttu-id="39fb7-156">Libera il buffer di stringa allocato da <a href="/windows/desktop/api/Winternl/nf-winternl-rtlansistringtounicodestring"><strong>RtlAnsiStringToUnicodeString</strong></a> o da <a href="https://msdn.microsoft.com/library/ms803011.aspx">RtlUpcaseUnicodeString</a>.</span><span class="sxs-lookup"><span data-stu-id="39fb7-156">Frees the string buffer allocated by <a href="/windows/desktop/api/Winternl/nf-winternl-rtlansistringtounicodestring"><strong>RtlAnsiStringToUnicodeString</strong></a> or by <a href="https://msdn.microsoft.com/library/ms803011.aspx">RtlUpcaseUnicodeString</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="39fb7-157"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlinitstring"><strong>RtlInitString</strong></a></span><span class="sxs-lookup"><span data-stu-id="39fb7-157"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlinitstring"><strong>RtlInitString</strong></a></span></span></td>
<td><span data-ttu-id="39fb7-158">Inizializza una stringa calcolata.</span><span class="sxs-lookup"><span data-stu-id="39fb7-158">Initializes a counted string.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39fb7-159"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlinitunicodestring"><strong>RtlInitUnicodeString</strong></a></span><span class="sxs-lookup"><span data-stu-id="39fb7-159"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlinitunicodestring"><strong>RtlInitUnicodeString</strong></a></span></span></td>
<td><span data-ttu-id="39fb7-160">Inizializza una stringa Unicode conteggiata.</span><span class="sxs-lookup"><span data-stu-id="39fb7-160">Initializes a counted Unicode string.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="39fb7-161"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtoansistring"><strong>RtlUnicodeStringToAnsiString</strong></a></span><span class="sxs-lookup"><span data-stu-id="39fb7-161"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtoansistring"><strong>RtlUnicodeStringToAnsiString</strong></a></span></span></td>
<td><span data-ttu-id="39fb7-162">Converte la stringa di origine Unicode specificata in una stringa ANSI.</span><span class="sxs-lookup"><span data-stu-id="39fb7-162">Converts the specified Unicode source string into an ANSI string.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39fb7-163"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring"><strong>RtlUnicodeStringToOemString</strong></a></span><span class="sxs-lookup"><span data-stu-id="39fb7-163"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring"><strong>RtlUnicodeStringToOemString</strong></a></span></span></td>
<td><span data-ttu-id="39fb7-164">Questa funzione converte la stringa di origine Unicode specificata in una stringa OEM.</span><span class="sxs-lookup"><span data-stu-id="39fb7-164">This functions converts the specified Unicode source string into an OEM string.</span></span> <span data-ttu-id="39fb7-165">La traduzione viene eseguita rispetto alla tabella codici OEM (OCP).</span><span class="sxs-lookup"><span data-stu-id="39fb7-165">The translation is done with respect to the OEM code page (OCP).</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="39fb7-166"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodetomultibytesize"><strong>RtlUnicodeToMultiByteSize</strong></a></span><span class="sxs-lookup"><span data-stu-id="39fb7-166"><a href="/windows/desktop/api/Winternl/nf-winternl-rtlunicodetomultibytesize"><strong>RtlUnicodeToMultiByteSize</strong></a></span></span></td>
<td><span data-ttu-id="39fb7-167">Determina il numero di byte necessari per rappresentare una stringa Unicode come stringa ANSI.</span><span class="sxs-lookup"><span data-stu-id="39fb7-167">Determines how many bytes are needed to represent a Unicode string as an ANSI string.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39fb7-168"><a href="/windows/desktop/devnotes/rtlunicodetoutf8n"><strong>RtlUnicodeToUTF8N</strong></a></span><span class="sxs-lookup"><span data-stu-id="39fb7-168"><a href="/windows/desktop/devnotes/rtlunicodetoutf8n"><strong>RtlUnicodeToUTF8N</strong></a></span></span></td>
<td><span data-ttu-id="39fb7-169">La funzione <a href="/windows/desktop/devnotes/rtlunicodetoutf8n"><strong>RtlUnicodeToUTF8N</strong></a> converte la stringa Unicode specificata in una nuova stringa di caratteri, usando la tabella codici UTF-8 (Unicode Transformation Format) a 8 bit.</span><span class="sxs-lookup"><span data-stu-id="39fb7-169">The <a href="/windows/desktop/devnotes/rtlunicodetoutf8n"><strong>RtlUnicodeToUTF8N</strong></a> function translates the specified Unicode string into a new character string, using the 8-bit Unicode Transformation Format (UTF-8) code page.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="39fb7-170"><a href="/windows/desktop/devnotes/rtlutf8tounicoden"><strong>RtlUTF8ToUnicodeN</strong></a></span><span class="sxs-lookup"><span data-stu-id="39fb7-170"><a href="/windows/desktop/devnotes/rtlutf8tounicoden"><strong>RtlUTF8ToUnicodeN</strong></a></span></span></td>
<td><span data-ttu-id="39fb7-171">La funzione <a href="/windows/desktop/devnotes/rtlutf8tounicoden"><strong>RtlUTF8ToUnicodeN</strong></a> converte la stringa di origine specificata in una stringa Unicode, usando la tabella codici UTF-8.</span><span class="sxs-lookup"><span data-stu-id="39fb7-171">The <a href="/windows/desktop/devnotes/rtlutf8tounicoden"><strong>RtlUTF8ToUnicodeN</strong></a> function translates the specified source string into a Unicode string, using the UTF-8 code page.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="39fb7-172"><a href="/windows/desktop/api/Ime/nf-ime-sendimemessageexa"><strong>SendIMEMessageEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="39fb7-172"><a href="/windows/desktop/api/Ime/nf-ime-sendimemessageexa"><strong>SendIMEMessageEx</strong></a></span></span></td>
<td><span data-ttu-id="39fb7-173">Specifica un'azione o un'elaborazione per l'IME (Input Method Editor) tramite una sottofunzione specificata.</span><span class="sxs-lookup"><span data-stu-id="39fb7-173">Specifies an action or processing for the Input Method Editor (IME) through a specified subfunction.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="39fb7-174">Questa funzione è obsoleta e non deve essere utilizzata.</span><span class="sxs-lookup"><span data-stu-id="39fb7-174">This function is obsolete and should not be used.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="39fb7-175"><a href="/windows/desktop/api/Winnls32/nf-winnls32-winnlsenableime"><strong>WINNLSEnableIME</strong></a></span><span class="sxs-lookup"><span data-stu-id="39fb7-175"><a href="/windows/desktop/api/Winnls32/nf-winnls32-winnlsenableime"><strong>WINNLSEnableIME</strong></a></span></span></td>
<td><span data-ttu-id="39fb7-176">Abilita o Disabilita temporaneamente un IME e, allo stesso tempo, attiva o disattiva la visualizzazione di tutte le finestre di proprietà dell'IME.</span><span class="sxs-lookup"><span data-stu-id="39fb7-176">Temporarily enables or disables an IME and, at the same time, turns on or off the display of all windows owned by the IME.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="39fb7-177">Questa funzione è obsoleta e non deve essere utilizzata.</span><span class="sxs-lookup"><span data-stu-id="39fb7-177">This function is obsolete and should not be used.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="structures"></a><span data-ttu-id="39fb7-178">Strutture</span><span class="sxs-lookup"><span data-stu-id="39fb7-178">Structures</span></span>



| <span data-ttu-id="39fb7-179">Argomento</span><span class="sxs-lookup"><span data-stu-id="39fb7-179">Topic</span></span>                                 | <span data-ttu-id="39fb7-180">Contenuto</span><span class="sxs-lookup"><span data-stu-id="39fb7-180">Contents</span></span>                                                                                                                                                                                                                              |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="39fb7-181">**IMESTRUCT**</span><span class="sxs-lookup"><span data-stu-id="39fb7-181">**IMESTRUCT**</span></span>](/windows/win32/api/ime/ns-ime-imestruct) | <span data-ttu-id="39fb7-182">Utilizzato da [**SendIMEMessageEx**](/windows/desktop/api/Ime/nf-ime-sendimemessageexa) per specificare la funzione subfunction da eseguire nel messaggio IME e i relativi parametri.</span><span class="sxs-lookup"><span data-stu-id="39fb7-182">Used by [**SendIMEMessageEx**](/windows/desktop/api/Ime/nf-ime-sendimemessageexa) to specify the subfunction to be executed in the IME message and its parameters.</span></span> <span data-ttu-id="39fb7-183">Questa struttura viene utilizzata anche per ricevere i valori restituiti da tali funzioni.</span><span class="sxs-lookup"><span data-stu-id="39fb7-183">This structure is also used to receive return values from those subfunctions.</span></span><br/> |
| [<span data-ttu-id="39fb7-184">**STRINGA**</span><span class="sxs-lookup"><span data-stu-id="39fb7-184">**STRING**</span></span>](/windows/desktop/api/Winternl/ns-winternl-string)       | <span data-ttu-id="39fb7-185">Questa struttura viene utilizzata con la funzione [**RtlUnicodeStringToOemString**](/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring) .</span><span class="sxs-lookup"><span data-stu-id="39fb7-185">This structure is used with the [**RtlUnicodeStringToOemString**](/windows/desktop/api/Winternl/nf-winternl-rtlunicodestringtooemstring) function.</span></span> <br/>                                                                                                              |



 

### <a name="compiler-routines"></a><span data-ttu-id="39fb7-186">Routine del compilatore</span><span class="sxs-lookup"><span data-stu-id="39fb7-186">Compiler Routines</span></span>



| <span data-ttu-id="39fb7-187">Argomento</span><span class="sxs-lookup"><span data-stu-id="39fb7-187">Topic</span></span>                                                             | <span data-ttu-id="39fb7-188">Contenuto</span><span class="sxs-lookup"><span data-stu-id="39fb7-188">Contents</span></span>                                                                                                     |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="39fb7-189">**\_\_\_Routine del gestore specifico di C \_**</span><span class="sxs-lookup"><span data-stu-id="39fb7-189">**\_\_C\_specific\_handler Routine**</span></span>](--c-specific-handler2.md) | <span data-ttu-id="39fb7-190">Il [**\_ \_ \_ \_ gestore specifico di c**](--c-specific-handler2.md) è una routine di supporto per il compilatore c.</span><span class="sxs-lookup"><span data-stu-id="39fb7-190">[**\_\_C\_specific\_handler**](--c-specific-handler2.md) is a helper routine for the C compiler.</span></span><br/> |
| [<span data-ttu-id="39fb7-191">\_Routine alldiv</span><span class="sxs-lookup"><span data-stu-id="39fb7-191">\_alldiv Routine</span></span>](-win32-alldiv.md)                             | <span data-ttu-id="39fb7-192">la [ \_ routine alldiv](-win32-alldiv.md) è una routine di supporto per il compilatore C.</span><span class="sxs-lookup"><span data-stu-id="39fb7-192">[\_alldiv Routine](-win32-alldiv.md) is a helper routine for the C compiler.</span></span><br/>                     |
| [<span data-ttu-id="39fb7-193">\_allmul</span><span class="sxs-lookup"><span data-stu-id="39fb7-193">\_allmul</span></span>](-win32-allmul.md) | <span data-ttu-id="39fb7-194">Moltiplica due **LONGLONG** o **ULONGLONG**.</span><span class="sxs-lookup"><span data-stu-id="39fb7-194">Multiplies two **LONGLONG** or **ULONGLONG**.</span></span> |
| [<span data-ttu-id="39fb7-195">\_aulldiv</span><span class="sxs-lookup"><span data-stu-id="39fb7-195">\_aulldiv</span></span>](-win32-aulldiv.md) | <span data-ttu-id="39fb7-196">Divide due interi **ULONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="39fb7-196">Divides two **ULONGLONG** integers.</span></span> |
| [<span data-ttu-id="39fb7-197">\_Routine chkstk</span><span class="sxs-lookup"><span data-stu-id="39fb7-197">\_chkstk Routine</span></span>](-win32-chkstk.md)                             | <span data-ttu-id="39fb7-198">la [ \_ routine chkstk](-win32-chkstk.md) è una routine di supporto per il compilatore C.</span><span class="sxs-lookup"><span data-stu-id="39fb7-198">[\_chkstk Routine](-win32-chkstk.md) is a helper routine for the C compiler.</span></span><br/>                     |
