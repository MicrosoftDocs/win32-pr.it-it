---
description: Il menu Start di Windows XP e Windows Vista contiene slot riservati per i client Internet (browser) e di posta elettronica (posta) predefiniti, insieme comunemente noti come applicazioni Internet del menu Start.
ms.assetid: a3d7416f-0dbd-4af2-ab38-758f9cc8aec5
title: Come registrare un browser Internet o un client di posta elettronica con il menu Start di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eccdd8fb8efe32522947b30ab2ce1a50b7058e97
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104234554"
---
# <a name="how-to-register-an-internet-browser-or-email-client-with-the-windows-start-menu"></a><span data-ttu-id="60a86-103">Come registrare un browser Internet o un client di posta elettronica con il menu Start di Windows</span><span class="sxs-lookup"><span data-stu-id="60a86-103">How to Register an Internet Browser or Email Client With the Windows Start Menu</span></span>

> [!Note]  
> <span data-ttu-id="60a86-104">Questo argomento si applica a Windows XP, Windows Vista e Windows 7.</span><span class="sxs-lookup"><span data-stu-id="60a86-104">This topic applies to Windows XP, Windows Vista, and Windows 7.</span></span>

 

<span data-ttu-id="60a86-105">Il menu Start di Windows XP e Windows Vista contiene slot riservati per i client **Internet** (browser) e di **posta elettronica** (posta) predefiniti, insieme comunemente noti come *applicazioni Internet del menu Start*.</span><span class="sxs-lookup"><span data-stu-id="60a86-105">The Start menu in Windows XP and Windows Vista contains reserved slots for the default **Internet** (browser) and **E-mail** (mail) clients, together commonly known as *Start Menu Internet Applications*.</span></span> <span data-ttu-id="60a86-106">Le applicazioni che si registrano come applicazioni Internet del menu Start eseguono questa operazione nell'intero sistema (per computer).</span><span class="sxs-lookup"><span data-stu-id="60a86-106">Applications which register as Start Menu Internet Applications do so across the entire system (per-machine).</span></span> <span data-ttu-id="60a86-107">In Windows Vista, l'utente può utilizzare la funzionalità **programmi predefiniti** per impostare un valore predefinito per singolo utente.</span><span class="sxs-lookup"><span data-stu-id="60a86-107">In Windows Vista, the user may use the **Default Programs** feature to set a per-user default.</span></span>

<span data-ttu-id="60a86-108">Quando le applicazioni si registrano come applicazioni Internet del menu Start, Windows XP e Windows Vista creano icone **Internet** e **posta elettronica** dal menu Start.</span><span class="sxs-lookup"><span data-stu-id="60a86-108">When applications register as Start Menu Internet Applications, Windows XP and Windows Vista create **Internet** and **E-mail** icons on the Start menu.</span></span> <span data-ttu-id="60a86-109">Se si fa clic su queste icone, il menu Start controlla il sottoalbero del registro di sistema per utente (**HKEY \_ Current \_ User**).</span><span class="sxs-lookup"><span data-stu-id="60a86-109">Clicking these icons causes the Start menu to check the per-user registry subtree (**HKEY\_CURRENT\_USER**).</span></span> <span data-ttu-id="60a86-110">Se non viene trovata alcuna impostazione predefinita per utente, il menu Start Cerca la sottochiave predefinita per computer nel sottoalbero **del \_ \_ computer locale HKEY** .</span><span class="sxs-lookup"><span data-stu-id="60a86-110">If no per-user default setting is found, the Start menu looks for the per-machine default subkey in the **HKEY\_LOCAL\_MACHINE** subtree.</span></span>

> [!Note]  
> <span data-ttu-id="60a86-111">L'installazione predefinita di Windows non registra un programma Internet o di posta elettronica predefinito per ogni utente, ma solo un valore predefinito a livello di sistema.</span><span class="sxs-lookup"><span data-stu-id="60a86-111">The default installation of Windows does not register a per-user default Internet or email program, only a system-wide default.</span></span> <span data-ttu-id="60a86-112">Questo fornisce un percorso di aggiornamento uniforme rispetto alle versioni precedenti del sistema operativo, in cui \_ \_ è supportato solo il sottoalbero del computer locale HKEY per le registrazioni client.</span><span class="sxs-lookup"><span data-stu-id="60a86-112">This provides a smooth upgrade path from previous versions of the operating system, in which only the HKEY\_LOCAL\_MACHINE subtree is supported for client registrations.</span></span>

 

<span data-ttu-id="60a86-113">In questo argomento vengono illustrati gli elementi seguenti:</span><span class="sxs-lookup"><span data-stu-id="60a86-113">This topic discusses the following items:</span></span>

-   [<span data-ttu-id="60a86-114">Registrazione per il collegamento Internet del menu Start</span><span class="sxs-lookup"><span data-stu-id="60a86-114">Registering for the Start Menu Internet Link</span></span>](#registering-for-the-start-menu-internet-link)
    -   [<span data-ttu-id="60a86-115">Come registrarsi come client Internet predefinito</span><span class="sxs-lookup"><span data-stu-id="60a86-115">How to Register as the Default Internet Client</span></span>](#how-to-register-as-the-default-internet-client)
-   [<span data-ttu-id="60a86-116">Registrazione per il collegamento di posta elettronica del menu Start</span><span class="sxs-lookup"><span data-stu-id="60a86-116">Registering for the Start Menu Email Link</span></span>](#registering-for-the-start-menu-email-link)
    -   [<span data-ttu-id="60a86-117">Visualizzazione del client di posta elettronica predefinito nel menu Start</span><span class="sxs-lookup"><span data-stu-id="60a86-117">How the Start Menu Displays the Default Email Client</span></span>](#how-the-start-menu-displays-the-default-email-client)
    -   [<span data-ttu-id="60a86-118">Come registrarsi come client di posta elettronica predefinito</span><span class="sxs-lookup"><span data-stu-id="60a86-118">How to Register as the Default EMail Client</span></span>](#how-to-register-as-the-default-email-client)
-   [<span data-ttu-id="60a86-119">Personalizzazione del menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="60a86-119">Customizing the Context Menu</span></span>](#customizing-the-context-menu)

## <a name="registering-for-the-start-menu-internet-link"></a><span data-ttu-id="60a86-120">Registrazione per il collegamento Internet del menu Start</span><span class="sxs-lookup"><span data-stu-id="60a86-120">Registering for the Start Menu Internet Link</span></span>

> [!Note]  
> <span data-ttu-id="60a86-121">Questa registrazione è deprecata a partire da Windows 7, che non fornisce più un collegamento Internet del menu Start.</span><span class="sxs-lookup"><span data-stu-id="60a86-121">This registration is deprecated as of Windows 7, which no longer provides a Start menu Internet link.</span></span> <span data-ttu-id="60a86-122">Le registrazioni esistenti vengono ignorate in Windows 7 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="60a86-122">Existing registrations are ignored in Windows 7 and later.</span></span> <span data-ttu-id="60a86-123">La registrazione come applicazione Internet predefinita del menu Start non corrisponde a quella registrata come Web browser predefinito.</span><span class="sxs-lookup"><span data-stu-id="60a86-123">Being registered as the default Start menu Internet application is not the same as being registered as the default web browser.</span></span> <span data-ttu-id="60a86-124">Il Web browser predefinito viene utilizzato per avviare URL arbitrari da qualsiasi punto del sistema.</span><span class="sxs-lookup"><span data-stu-id="60a86-124">The default web browser is used for launching arbitrary URLs from anywhere in the system.</span></span> <span data-ttu-id="60a86-125">L'applicazione Internet del menu Start controlla semplicemente il programma avviato quando l'utente fa clic sull'icona Internet nel menu Start.</span><span class="sxs-lookup"><span data-stu-id="60a86-125">The Start menu Internet application merely controls the program that is started when the user clicks the Internet icon on the Start menu.</span></span>

 

<span data-ttu-id="60a86-126">Qualsiasi applicazione Web browser può essere registrata per essere visualizzata come client Internet nel menu Start.</span><span class="sxs-lookup"><span data-stu-id="60a86-126">Any web browser application can register to appear as an Internet client on the Start menu.</span></span> <span data-ttu-id="60a86-127">Questa visibilità, associata alla registrazione corretta per i tipi di [file](fa-intro.md) e di [protocollo](/previous-versions//aa767743(v=vs.85)) di un'applicazione, fornisce uno stato del browser predefinito dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="60a86-127">This visibility, coupled with proper registration for an application's [file](fa-intro.md) and [protocol](/previous-versions//aa767743(v=vs.85)) types, gives an application default browser status.</span></span>

<span data-ttu-id="60a86-128">Le registrazioni effettuate nel sottoalbero dell' **\_ \_ utente corrente di HKEY** hanno una precedenza maggiore per l'utente della console rispetto alle registrazioni corrispondenti effettuate nel **\_ \_ computer locale HKEY**.</span><span class="sxs-lookup"><span data-stu-id="60a86-128">Registrations made in the **HKEY\_CURRENT\_USER** subtree have higher precedence for the console user than corresponding registrations made in the **HKEY\_LOCAL\_MACHINE**.</span></span> <span data-ttu-id="60a86-129">Per i nuovi utenti del sistema, vengono usate le impostazioni archiviate nel **\_ \_ computer locale HKEY** .</span><span class="sxs-lookup"><span data-stu-id="60a86-129">For new users on the system, the settings stored in **HKEY\_LOCAL\_MACHINE** are used.</span></span> <span data-ttu-id="60a86-130">A partire da Windows XP, le impostazioni Internet del menu Start vengono mantenute nelle voci predefinite dei due percorsi del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="60a86-130">As of Windows XP, Start menu Internet settings are kept in the default entries of two registry locations:</span></span>

-   <span data-ttu-id="60a86-131">**HKEY \_ Client \_ software utente corrente** \\  \\  \\ **StartMenuInternet**</span><span class="sxs-lookup"><span data-stu-id="60a86-131">**HKEY\_CURRENT\_USER**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet**</span></span>
-   <span data-ttu-id="60a86-132">**HKEY \_ Client software del \_ computer locale** \\  \\  \\ **StartMenuInternet**</span><span class="sxs-lookup"><span data-stu-id="60a86-132">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet**</span></span>

<span data-ttu-id="60a86-133">La sottochiave **HKEY \_ Current \_ User** \\ **software** \\ **clients** \\ **StartMenuInternet** descrive il browser Internet che viene avviato quando l'utente fa clic sull'icona **Internet** nel menu Start.</span><span class="sxs-lookup"><span data-stu-id="60a86-133">The subkey **HKEY\_CURRENT\_USER**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet** describes the Internet browser that is started when the user clicks the **Internet** icon on the Start menu.</span></span> <span data-ttu-id="60a86-134">Se la sottochiave è vuota o mancante, l'icona **Internet** nel menu Start viene impostata sul valore predefinito di sistema archiviato nella seconda posizione in **HKEY \_ Local \_ Machine** \\ **software** \\ **clients** \\ **StartMenuInternet** , che descrive tutte le applicazioni del browser Internet installate nel sistema.</span><span class="sxs-lookup"><span data-stu-id="60a86-134">If that subkey is blank or missing, then the **Internet** icon on the Start menu is set to the system default stored in the second location at **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet** , which describes all Internet browser applications that are installed on the system.</span></span>

<span data-ttu-id="60a86-135">Quando un nuovo utente accede al sistema, nel menu Start viene usato il valore predefinito nella sottochiave in **HKEY \_ \_ computer locale** \\  \\ **client** software \\ **StartMenuInternet** per visualizzare il client Internet predefinito e avvia l'applicazione registrata quando si fa clic sull'icona.</span><span class="sxs-lookup"><span data-stu-id="60a86-135">When a new user logs onto the system, the Start menu uses the default value in the subkey at **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet** to display the default Internet client and starts the registered application when that icon is clicked.</span></span>

### <a name="how-to-register-as-the-default-internet-client"></a><span data-ttu-id="60a86-136">Come registrarsi come client Internet predefinito</span><span class="sxs-lookup"><span data-stu-id="60a86-136">How to Register as the Default Internet Client</span></span>

<span data-ttu-id="60a86-137">Sotto la sottochiave **HKEY \_ \_ computer locale** \\  \\ **client** software \\ **StartMenuInternet** possono essere presenti zero o più sottochiavi, una per ogni applicazione Internet browser registrata.</span><span class="sxs-lookup"><span data-stu-id="60a86-137">Below the subkey **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**StartMenuInternet** there can be zero or more subkeys, one for each registered Internet browser application.</span></span> <span data-ttu-id="60a86-138">Ad esempio, un sistema ipotetico potrebbe avere questa disposizione:</span><span class="sxs-lookup"><span data-stu-id="60a86-138">For example, a hypothetical system might have this arrangement:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            IEXPLORE.EXE
            BROWSER2.EXE
            BROWSER3.EXE
```

<span data-ttu-id="60a86-139">Vengono illustrate le voci del registro di sistema con un ipotetico browser denominato "Lit View" di una società fittizia denominata Litware Inc. si supponga che il nome dell'eseguibile per la visualizzazione illuminata sia Litview.exe.</span><span class="sxs-lookup"><span data-stu-id="60a86-139">We will demonstrate registry entries with a hypothetical browser called "Lit View" from a fictional company called Litware Inc. Suppose that the executable name for Lit View is Litview.exe.</span></span> <span data-ttu-id="60a86-140">La registrazione della visualizzazione illuminata viene eseguita come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="60a86-140">The registration of Lit View occurs as shown here:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            LITVIEW.EXE
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
```

<span data-ttu-id="60a86-141">I dati LocalizedString sono di tipo REG \_ SZ oppure reg \_ expand \_ SZ se vengono usate variabili di percorso come `%programfiles%` .</span><span class="sxs-lookup"><span data-stu-id="60a86-141">The LocalizedString data is of type REG\_SZ, or REG\_EXPAND\_SZ if path variables such as `%programfiles%` are used.</span></span> <span data-ttu-id="60a86-142">LocalizedString fornisce il percorso di un file eseguibile (con estensione exe) o di una libreria (. dll).</span><span class="sxs-lookup"><span data-stu-id="60a86-142">LocalizedString provides the path to an executable (.exe) or library (.dll) file.</span></span> <span data-ttu-id="60a86-143">Si noti che la stringa di percorso inizia con un simbolo di chiocciola (@) e che non sono necessarie virgolette intorno al percorso indipendentemente dagli spazi al suo interno.</span><span class="sxs-lookup"><span data-stu-id="60a86-143">Note that the path string begins with an "at" sign (@) and that no quotation marks are required around the path regardless of spaces within it.</span></span> <span data-ttu-id="60a86-144">Il numero intero decimale è l'ID di una risorsa di tipo stringa, contenuto all'interno della DLL specificata, il cui valore deve essere visualizzato all'utente.</span><span class="sxs-lookup"><span data-stu-id="60a86-144">The decimal integer is the ID of a string resource, contained within the specified DLL, whose value is to be displayed to the user.</span></span> <span data-ttu-id="60a86-145">In questo modo è possibile usare la stessa registrazione per più linguaggi.</span><span class="sxs-lookup"><span data-stu-id="60a86-145">This enables the same registration to be used for multiple languages.</span></span> <span data-ttu-id="60a86-146">Ogni lingua fornisce un ResourceDLL.dll diverso.</span><span class="sxs-lookup"><span data-stu-id="60a86-146">Each language provides a different ResourceDLL.dll.</span></span> <span data-ttu-id="60a86-147">Ciò consente al sistema di visualizzare la stringa corretta in base alla lingua attualmente selezionata.</span><span class="sxs-lookup"><span data-stu-id="60a86-147">This enables the system to display the correct string based on the currently selected language.</span></span>

<span data-ttu-id="60a86-148">Il valore REG \_ sz o reg \_ expand \_ SZ seguente informa il menu Start dell'icona predefinita da visualizzare quando l'utente seleziona visualizzazione illuminata come browser Internet del menu Start.</span><span class="sxs-lookup"><span data-stu-id="60a86-148">The following REG\_SZ or REG\_EXPAND\_SZ value informs the Start menu of the default icon to display when the user selects Lit View as the Start menu Internet browser.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            LITVIEW.EXE
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LitView.exe,1
```

<span data-ttu-id="60a86-149">La sottochiave del registro di sistema seguente consente di specificare una riga di comando da eseguire quando l'utente fa clic sul comando di menu Internet nel menu Start, supponendo che la visualizzazione illuminata sia il browser Internet selezionato dal menu Start.</span><span class="sxs-lookup"><span data-stu-id="60a86-149">The following registry subkey specifies a command line to run when the user clicks the Internet menu command on the Start menu, assuming that Lit View is the selected Start menu Internet browser.</span></span> <span data-ttu-id="60a86-150">Ad esempio, il comando può aprire il browser con l'home page dell'utente oppure il comando può avviare un'interfaccia utente introduttiva che il fornitore di software indipendente (ISV) ritiene sia appropriato.</span><span class="sxs-lookup"><span data-stu-id="60a86-150">For example, the command might open the browser with the user's home page or the command could launch an introductory user interface that the independent software vendor (ISV) feels is appropriate.</span></span> <span data-ttu-id="60a86-151">I dati sono di tipo REG \_ sz o reg \_ expand \_ SZ, ma si noti che, dal momento che nel percorso della riga di comando è presente uno spazio, il percorso eseguibile è racchiuso tra virgolette.</span><span class="sxs-lookup"><span data-stu-id="60a86-151">The data is of type REG\_SZ or REG\_EXPAND\_SZ, but notice that because there is a space in the command-line path, the executable path is enclosed in quotation marks.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            LITVIEW.EXE
               shell
                  open
                     (Default) = "C:\Program Files\LitwareInc\LitView.exe" -welcome
```

<span data-ttu-id="60a86-152">Quando l'utente specifica tramite [set Program Access e computer Defaults (SPAD)](cpl-setprogramaccess.md) che Lit View deve essere utilizzato come Web browser predefinito a livello di computer, l'applicazione deve impostare la seguente \_ voce reg SZ.</span><span class="sxs-lookup"><span data-stu-id="60a86-152">When the user specifies through [Set Program Access and Computer Defaults (SPAD)](cpl-setprogramaccess.md) that Lit View should be used as the computer-level default web browser, the application should set the following REG\_SZ entry.</span></span> <span data-ttu-id="60a86-153">Si noti che poiché SPAD viene eseguito con privilegi di amministratore, è consentito l'accesso a questa sottochiave.</span><span class="sxs-lookup"><span data-stu-id="60a86-153">Note that because SPAD runs with Administrator privileges, access to this subkey is allowed.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            (Default) = LITVIEW.EXE
```

> [!Note]
> <span data-ttu-id="60a86-154">In Windows Vista, il Web browser predefinito a livello di utente deve essere impostato utilizzando lo strumento **programmi predefiniti** , non [SPAD](cpl-setprogramaccess.md).</span><span class="sxs-lookup"><span data-stu-id="60a86-154">In Windows Vista, the user-level default web browser should be set using the **Default Programs** tool, not [SPAD](cpl-setprogramaccess.md).</span></span>
> 
> <span data-ttu-id="60a86-155">**Le informazioni seguenti si applicano solo a Windows XP.**</span><span class="sxs-lookup"><span data-stu-id="60a86-155">**The following information applies to Windows XP only.**</span></span>
> 
> <span data-ttu-id="60a86-156">Se la registrazione del Web browser predefinito a livello di computer nel computer \_ locale HKEY \_ come illustrato in precedenza ha esito positivo, l'applicazione deve eliminare la voce predefinita nella sottochiave seguente:</span><span class="sxs-lookup"><span data-stu-id="60a86-156">If the registration of the computer-level default web browser under HKEY\_LOCAL\_MACHINE as shown above is successful, the application should delete the Default entry under the following subkey:</span></span>
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          StartMenuInternet
> ```
> 
> <span data-ttu-id="60a86-157">Se la registrazione del Web browser predefinito a livello di computer nel computer \_ locale HKEY ha \_ esito negativo, l'applicazione deve impostare i \_ dati reg SZ come illustrato in questo esempio per l'applicazione di visualizzazione illuminata:</span><span class="sxs-lookup"><span data-stu-id="60a86-157">If the registration of the computer-level default web browser under HKEY\_LOCAL\_MACHINE fails, the application should set the REG\_SZ data as shown in this example for the Lit View application:</span></span>
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          (Default) = LITVIEW.EXE
> ```

 

<span data-ttu-id="60a86-158">Dopo aver aggiornato le sottochiavi appropriate, l'applicazione trasmette il messaggio [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) con il parametro *wParam* impostato su 0 e il parametro *lParam* che punta alla stringa con terminazione null `"Software\Clients\StartMenuInternet"` .</span><span class="sxs-lookup"><span data-stu-id="60a86-158">After updating the appropriate subkeys, the application broadcasts the [**WM\_SETTINGCHANGE**](../winmsg/wm-settingchange.md) message with its *wParam* parameter set to 0 and its *lParam* parameter pointing to the null-terminated string `"Software\Clients\StartMenuInternet"`.</span></span> <span data-ttu-id="60a86-159">Viene notificato al sistema operativo che il client predefinito è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="60a86-159">This notifies the operating system that the default client has changed.</span></span>

<span data-ttu-id="60a86-160">L'impostazione di queste sottochiavi per il browser Internet predefinito del menu Start è necessaria per mantenere la compatibilità con le versioni precedenti di Web browser che non supportano le registrazioni per singolo utente.</span><span class="sxs-lookup"><span data-stu-id="60a86-160">Setting these subkeys for the default Start menu Internet browser is necessary to preserve backward compatibility with old web browsers that do not support per-user registrations.</span></span>

## <a name="registering-for-the-start-menu-email-link"></a><span data-ttu-id="60a86-161">Registrazione per il collegamento di posta elettronica del menu Start</span><span class="sxs-lookup"><span data-stu-id="60a86-161">Registering for the Start Menu Email Link</span></span>

> [!Note]  
> <span data-ttu-id="60a86-162">Il collegamento di posta elettronica del menu Start è stato rimosso a partire da Windows 7.</span><span class="sxs-lookup"><span data-stu-id="60a86-162">The Start menu Email link has been removed as of Windows 7.</span></span> <span data-ttu-id="60a86-163">Questa registrazione, tuttavia, descritta in questa sezione dovrebbe comunque essere eseguita per l'assegnazione del client MAPI predefinito.</span><span class="sxs-lookup"><span data-stu-id="60a86-163">However, this registration discussed in this section should still be performed for its effect in assigning the default MAPI client.</span></span>

 

### <a name="how-the-start-menu-displays-the-default-email-client"></a><span data-ttu-id="60a86-164">Visualizzazione del client di posta elettronica predefinito nel menu Start</span><span class="sxs-lookup"><span data-stu-id="60a86-164">How the Start Menu Displays the Default Email Client</span></span>

<span data-ttu-id="60a86-165">Qualsiasi applicazione di posta elettronica può essere registrata per essere visualizzata come client di posta elettronica nel menu Start.</span><span class="sxs-lookup"><span data-stu-id="60a86-165">Any email application can register to appear as an email client on the Start menu.</span></span> <span data-ttu-id="60a86-166">Questa visibilità, abbinata alla registrazione corretta per i tipi di [file](fa-intro.md) e di [protocollo](/previous-versions//aa767743(v=vs.85)) di un'applicazione, fornisce uno stato di posta predefinito per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="60a86-166">This visibility, coupled with proper registration for an application's [file](fa-intro.md) and [protocol](/previous-versions//aa767743(v=vs.85)) types, gives an application default mail status.</span></span>

<span data-ttu-id="60a86-167">Le registrazioni effettuate nel sottoalbero dell' **\_ \_ utente corrente di HKEY** hanno una precedenza maggiore per l'utente della console rispetto alle registrazioni corrispondenti effettuate nel **\_ \_ computer locale HKEY**.</span><span class="sxs-lookup"><span data-stu-id="60a86-167">Registrations made in the **HKEY\_CURRENT\_USER** subtree have higher precedence for the console user than corresponding registrations made in the **HKEY\_LOCAL\_MACHINE**.</span></span> <span data-ttu-id="60a86-168">Per i nuovi utenti del sistema, vengono usate le impostazioni archiviate nel **\_ \_ computer locale HKEY** .</span><span class="sxs-lookup"><span data-stu-id="60a86-168">For new users on the system, the settings stored in **HKEY\_LOCAL\_MACHINE** are used.</span></span> <span data-ttu-id="60a86-169">A partire da Windows XP, le impostazioni di posta elettronica del menu Start vengono mantenute nelle voci predefinite dei due percorsi del registro di sistema:</span><span class="sxs-lookup"><span data-stu-id="60a86-169">As of Windows XP, Start menu Email settings are kept in the default entries of two registry locations:</span></span>

-   <span data-ttu-id="60a86-170">**HKEY \_ \_** \\  \\  \\ **Posta elettronica** client software utente corrente</span><span class="sxs-lookup"><span data-stu-id="60a86-170">**HKEY\_CURRENT\_USER**\\**SOFTWARE**\\**Clients**\\**Mail**</span></span>
-   <span data-ttu-id="60a86-171">**HKEY \_ \_** \\  \\  \\ **Posta elettronica** client del computer locale</span><span class="sxs-lookup"><span data-stu-id="60a86-171">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail**</span></span>

<span data-ttu-id="60a86-172">La sottochiave **HKEY \_ Current \_ User** \\ **software** \\ **clients** \\ **mail** descrive il client di posta elettronica che viene avviato quando l'utente fa clic sull'icona del **messaggio di posta elettronica** nel menu Start.</span><span class="sxs-lookup"><span data-stu-id="60a86-172">The subkey **HKEY\_CURRENT\_USER**\\**SOFTWARE**\\**Clients**\\**Mail** describes the email client that is started when the user clicks the **E-mail** icon on the Start menu.</span></span>

<span data-ttu-id="60a86-173">La sottochiave **HKEY \_ Local \_ computer** \\ **software** \\ **clients** \\ **mail** descrive le applicazioni di posta elettronica installate nel sistema e l'applicazione di posta elettronica predefinita.</span><span class="sxs-lookup"><span data-stu-id="60a86-173">The subkey **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail** describes the email applications that are installed on the system, as well as the default email application.</span></span>

<span data-ttu-id="60a86-174">Se la posta elettronica client del software **\_ \_ utente corrente di HKEY** \\  \\  \\  è vuota o mancante, il valore predefinito definito in **HKEY \_ \_ computer locale** \\  \\ **client** software \\  viene usato per selezionare l'applicazione di posta elettronica che viene visualizzata nel menu Start.</span><span class="sxs-lookup"><span data-stu-id="60a86-174">If the **HKEY\_CURRENT\_USER**\\**SOFTWARE**\\**Clients**\\**Mail** is blank or missing, the default value defined in **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail** is used to select the email application that appears on the Start menu.</span></span>

<span data-ttu-id="60a86-175">Quando un nuovo utente accede al sistema, nel menu Start viene usato il valore predefinito nella sottochiave in **HKEY \_ Local \_ Machine** \\ **software** \\ **clients** \\ **mail** per visualizzare il client di posta elettronica predefinito e avvia l'applicazione registrata quando si fa clic sull'icona.</span><span class="sxs-lookup"><span data-stu-id="60a86-175">When a new user logs onto the system, the Start menu uses the default value in the subkey at **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail** to display the default email client and starts the registered application when that icon is clicked.</span></span>

### <a name="how-to-register-as-the-default-email-client"></a><span data-ttu-id="60a86-176">Come registrarsi come client di posta elettronica predefinito</span><span class="sxs-lookup"><span data-stu-id="60a86-176">How to Register as the Default EMail Client</span></span>

<span data-ttu-id="60a86-177">**HKEY \_ I client software del \_ computer locale** \\  \\  \\  possono contenere zero o più sottochiavi, una per ogni applicazione di posta elettronica registrata.</span><span class="sxs-lookup"><span data-stu-id="60a86-177">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Clients**\\**Mail** can contain zero or more subkeys, one for each registered email application.</span></span> <span data-ttu-id="60a86-178">Un ipotetico sistema, ad esempio, può definire le sottochiavi seguenti:</span><span class="sxs-lookup"><span data-stu-id="60a86-178">For example, a hypothetical system might define the following subkeys:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            Eudora
            Windows Mail
```

<span data-ttu-id="60a86-179">In questo articolo vengono illustrate le voci del registro di sistema con un ipotetico client di posta elettronica denominato "Lit Mail" della società fittizia denominata Litware Inc. Litware Inc. decide di registrare il client di posta elettronica con il nome interno "LitMail".</span><span class="sxs-lookup"><span data-stu-id="60a86-179">We will demonstrate registry entries with a hypothetical email client called "Lit Mail" from the fictional company called Litware Inc. Litware Inc. decides to register this email client under the internal name "LitMail".</span></span> <span data-ttu-id="60a86-180">Come per un browser, il nome interno è una stringa univoca usata come nome della sottochiave, ma non viene mai visualizzata all'utente.</span><span class="sxs-lookup"><span data-stu-id="60a86-180">As with a browser, the internal name is a unique string used as the subkey name, but it is never shown to the user.</span></span>

<span data-ttu-id="60a86-181">Per installare il client di posta elettronica per la posta illuminata come predefinita, usano la sottochiave e le voci seguenti:</span><span class="sxs-lookup"><span data-stu-id="60a86-181">To install the Lit Mail email client as the default, they use the following subkey and its entries:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               (Default) = Lit Mail
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-456
```

<span data-ttu-id="60a86-182">I dati LocalizedString sono di tipo REG \_ SZ oppure reg \_ expand \_ SZ se vengono usate variabili di percorso come `%programfiles%` .</span><span class="sxs-lookup"><span data-stu-id="60a86-182">The LocalizedString data is of type REG\_SZ, or REG\_EXPAND\_SZ if path variables such as `%programfiles%` are used.</span></span> <span data-ttu-id="60a86-183">LocalizedString fornisce il percorso di un file eseguibile (con estensione exe) o di una libreria (. dll).</span><span class="sxs-lookup"><span data-stu-id="60a86-183">LocalizedString provides the path to an executable (.exe) or library (.dll) file.</span></span> <span data-ttu-id="60a86-184">Si noti che la stringa di percorso inizia con un simbolo di chiocciola (@) e che non sono necessarie virgolette intorno al percorso indipendentemente dagli spazi al suo interno.</span><span class="sxs-lookup"><span data-stu-id="60a86-184">Note that the path string begins with an "at" sign (@) and that no quotation marks are required around the path regardless of spaces within it.</span></span> <span data-ttu-id="60a86-185">Il numero intero decimale è l'ID di una risorsa di tipo stringa, contenuto all'interno della DLL specificata, il cui valore deve essere visualizzato all'utente.</span><span class="sxs-lookup"><span data-stu-id="60a86-185">The decimal integer is the ID of a string resource, contained within the specified DLL, whose value is to be displayed to the user.</span></span> <span data-ttu-id="60a86-186">In questo modo è possibile usare la stessa registrazione per più linguaggi.</span><span class="sxs-lookup"><span data-stu-id="60a86-186">This enables the same registration to be used for multiple languages.</span></span> <span data-ttu-id="60a86-187">Ogni lingua fornisce un ResourceDLL.dll diverso.</span><span class="sxs-lookup"><span data-stu-id="60a86-187">Each language provides a different ResourceDLL.dll.</span></span> <span data-ttu-id="60a86-188">Ciò consente al sistema di visualizzare la stringa corretta in base alla lingua attualmente selezionata.</span><span class="sxs-lookup"><span data-stu-id="60a86-188">This enables the system to display the correct string based on the currently selected language.</span></span>

<span data-ttu-id="60a86-189">Dopo aver aggiornato le sottochiavi appropriate, l'applicazione trasmette il messaggio [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) con il parametro *wParam* impostato su 0 e il parametro *lParam* che punta alla stringa con terminazione null `"Software\Clients\Mail"` .</span><span class="sxs-lookup"><span data-stu-id="60a86-189">After updating the appropriate subkeys, the application broadcasts the [**WM\_SETTINGCHANGE**](../winmsg/wm-settingchange.md) message with its *wParam* parameter set to 0 and its *lParam* parameter pointing to the null-terminated string `"Software\Clients\Mail"`.</span></span> <span data-ttu-id="60a86-190">Viene notificato al sistema operativo che il client predefinito è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="60a86-190">This notifies the operating system that the default client has changed.</span></span>

<span data-ttu-id="60a86-191">Per garantire la compatibilità con le applicazioni che non supportano le stringhe localizzate, il nome dell'applicazione nella lingua installata deve essere impostato anche come valore predefinito per la sottochiave.</span><span class="sxs-lookup"><span data-stu-id="60a86-191">For backward compatibility with applications that do not support localized strings, the name of the application in the installed language should also be set as the default value for the subkey.</span></span>

<span data-ttu-id="60a86-192">Il valore **reg \_ SZ** o **reg \_ expand \_ SZ** seguente informa il menu Start dell'icona predefinita da visualizzare quando l'utente seleziona la posta illuminata come programma di posta elettronica del menu Start:</span><span class="sxs-lookup"><span data-stu-id="60a86-192">The following **REG\_SZ** or **REG\_EXPAND\_SZ** value informs the Start menu of the default icon to display when the user selects Lit Mail as the Start menu mail program:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LitMail.exe,1
```

<span data-ttu-id="60a86-193">La voce seguente consente di specificare una riga di comando da eseguire quando l'utente fa clic sulla voce di menu della **posta elettronica** nel menu Start, supponendo che la posta elettronica sia il programma di posta elettronica del menu Start selezionato.</span><span class="sxs-lookup"><span data-stu-id="60a86-193">The following entry specifies a command line to run when the user clicks the **E-mail** menu item on the Start menu, assuming that Lit Mail is the selected Start menu email program.</span></span> <span data-ttu-id="60a86-194">Questa riga di comando viene eseguita anche se l'utente seleziona **Leggi messaggio di posta elettronica** dal menu **strumenti** di Windows Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="60a86-194">This command line is also run if the user selects **Read email** from the Windows Internet Explorer **Tools** menu.</span></span> <span data-ttu-id="60a86-195">I dati sono di tipo **reg \_ SZ** o **reg \_ expand \_ SZ**, ma si noti che, dal momento che nel percorso della riga di comando è presente uno spazio, il percorso eseguibile è racchiuso tra virgolette.</span><span class="sxs-lookup"><span data-stu-id="60a86-195">The data is of type **REG\_SZ** or **REG\_EXPAND\_SZ**, but notice that because there is a space in the command-line path, the executable path is enclosed in quotation marks.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            shell
               open
                  command
                     (Default) = "C:\Program Files\LitwareInc\LitMail.exe" -inbox
```

<span data-ttu-id="60a86-196">Se (e solo se) *l'utente* specifica che la posta elettronica è stata accesa come applicazione di posta elettronica predefinita del menu Start, l'applicazione di posta elettronica illuminata può scrivere il proprio nome interno nel seguente valore **reg \_ SZ** :</span><span class="sxs-lookup"><span data-stu-id="60a86-196">If (and only if) *the user* specifies Lit Mail to be the default Start menu email application, the Lit Mail application may write its internal name to the following **REG\_SZ** value:</span></span>

```
HKEY_CURRENT_USER
   SOFTWARE
      Clients
         Mail
            (Default) = LitMail
```

<span data-ttu-id="60a86-197">Se (e solo se) *l'utente* specifica la posta illuminata come applicazione di posta elettronica predefinita a livello di sistema, l'applicazione di posta elettronica illuminata può scrivere il proprio nome interno nel valore **reg \_ SZ** specificato di seguito.</span><span class="sxs-lookup"><span data-stu-id="60a86-197">If (and only if) *the user* specifies Lit Mail to be the system-wide default email application, the Lit Mail application may write its internal name to the **REG\_SZ** value specified below.</span></span> <span data-ttu-id="60a86-198">Si noti che l'accesso a questa sottochiave potrebbe essere limitato.</span><span class="sxs-lookup"><span data-stu-id="60a86-198">Note that access to this subkey might be restricted.</span></span> <span data-ttu-id="60a86-199">Le applicazioni non devono presupporre che tutti gli utenti dispongano delle autorizzazioni per modificare l'applicazione di posta elettronica predefinita a livello di sistema.</span><span class="sxs-lookup"><span data-stu-id="60a86-199">Applications should not assume that all users have permission to change the system-wide default email application.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            (Default) = LitMail
```

<span data-ttu-id="60a86-200">La registrazione come applicazione di posta elettronica predefinita del menu Start non equivale alla registrazione come client di posta elettronica predefinito del sistema o gestore *mailto* registrato.</span><span class="sxs-lookup"><span data-stu-id="60a86-200">Registration as the default Start menu email application is not equivalent to registration as the system default email client or the registered *mailto* handler.</span></span>

-   <span data-ttu-id="60a86-201">Il client di posta elettronica predefinito del sistema viene avviato quando l'utente fa clic su **Leggi messaggio di posta elettronica** dal menu **strumenti** di Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="60a86-201">The system default email client is started when the user clicks **Read email** from the Internet Explorer **Tools** menu.</span></span>
-   <span data-ttu-id="60a86-202">Il gestore *mailto* registrato viene avviato quando l'utente fa clic su un URL del modulo `mailto:someone@example.com` .</span><span class="sxs-lookup"><span data-stu-id="60a86-202">The registered *mailto* handler is started when the user clicks a URL of the form `mailto:someone@example.com`.</span></span>
-   <span data-ttu-id="60a86-203">L'applicazione di posta elettronica del menu Start viene avviata quando l'utente fa clic sull'icona del **messaggio di posta elettronica** nel menu Start.</span><span class="sxs-lookup"><span data-stu-id="60a86-203">The Start menu email application is started when the user clicks the **E-mail** icon on the Start menu.</span></span>

<span data-ttu-id="60a86-204">Se non viene specificata alcuna applicazione di posta elettronica predefinita del menu Start, l'icona del messaggio di posta elettronica nel menu Start avvia il client di posta elettronica predefinito del sistema.</span><span class="sxs-lookup"><span data-stu-id="60a86-204">If no default Start menu email application is specified, the Email icon on the Start menu launches the system default email client.</span></span>

<span data-ttu-id="60a86-205">In questo argomento non viene illustrata la registrazione dell'applicazione come gestore di protocollo *mailto* predefinito.</span><span class="sxs-lookup"><span data-stu-id="60a86-205">This topic does not cover registration of the application as the default *mailto* protocol handler.</span></span> <span data-ttu-id="60a86-206">Le applicazioni che si desidera registrare in questo modo devono continuare a seguire le specifiche esistenti in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="60a86-206">Applications that want to register in such a manner should continue to follow existing specifications on this subject.</span></span>

## <a name="customizing-the-context-menu"></a><span data-ttu-id="60a86-207">Personalizzazione del menu di scelta rapida</span><span class="sxs-lookup"><span data-stu-id="60a86-207">Customizing the Context Menu</span></span>

<span data-ttu-id="60a86-208">Un'applicazione può personalizzare le pagine delle proprietà visualizzate quando l'utente seleziona **Proprietà** dal menu di scelta rapida dell'icona del **messaggio di posta elettronica** (o **Internet**).</span><span class="sxs-lookup"><span data-stu-id="60a86-208">An application can customize the property pages that are displayed when the user selects **Properties** from the **E-mail** (or **Internet**) icon's shortcut menu.</span></span> <span data-ttu-id="60a86-209">Ad esempio, l'applicazione Litware email aggiunge i dati **reg \_ SZ** o **reg \_ expand \_ SZ** seguenti per visualizzare una finestra delle proprietà personalizzata per l'icona del **messaggio di posta elettronica** anziché la relativa finestra delle proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="60a86-209">For example, the Litware email application adds the following **REG\_SZ** or **REG\_EXPAND\_SZ** data to display a custom property sheet for the **E-mail** icon rather than its default property sheet.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               shell
                  properties
                     MUIVerb = @C:\Program Files\LitwareInc\ResourceDLL.dll,-789
                     command
                        (Default) = "C:\Program Files\LitwareInc\LitMail.exe" -properties
```

<span data-ttu-id="60a86-210">L'elemento di dati MUIVerb viene costruito a partire da un segno "at" (@), seguito dal percorso completo della DLL della risorsa, da una virgola, da un segno meno (-) e quindi dall'identificatore di risorsa della stringa decimale da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="60a86-210">The MUIVerb data item is constructed beginning with an "at" sign (@), followed by the full path to the resource DLL, a comma, a minus sign (-), and then the decimal string resource identifier to display.</span></span> <span data-ttu-id="60a86-211">Si noti che il percorso del programma LitMail.exe contiene spazi, quindi la stringa di percorso viene posizionata tra virgolette.</span><span class="sxs-lookup"><span data-stu-id="60a86-211">Note that the path to the LitMail.exe program contains spaces, so the path string is placed inside quotation marks.</span></span>

<span data-ttu-id="60a86-212">Un'applicazione può anche aggiungere altri comandi al menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="60a86-212">An application can also add additional commands to the context menu.</span></span> <span data-ttu-id="60a86-213">Ad esempio, l'applicazione Litware email aggiunge un comando **Find** con i seguenti dati **reg \_ SZ** :</span><span class="sxs-lookup"><span data-stu-id="60a86-213">For example, the Litware email application adds a **find** command with the following **REG\_SZ** data:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               shell
                  find
                     MUIVerb = @C:\Program File\LitwareInc\ResourceDLL.dll,-790
                     command
                        (Default) = "C:\Program Files\LitwareInc\LitMail.exe" -contacts
```

<span data-ttu-id="60a86-214">Il nome della sottochiave sottostante **Shell** , in questo caso "Find", è un nome arbitrario e non localizzato.</span><span class="sxs-lookup"><span data-stu-id="60a86-214">The subkey name below **shell** (in this case, "find") is an arbitrary, nonlocalized name.</span></span> <span data-ttu-id="60a86-215">Anche in questo caso i dati di MUIVerb contengono un segno di chiocciola (@) come primo elemento, seguito dal percorso di una DLL di risorse, da un separatore virgola e quindi da un segno meno che precede l'identificatore di risorsa della stringa decimale.</span><span class="sxs-lookup"><span data-stu-id="60a86-215">Once again the MUIVerb data contains an "at" sign (@) as the first element, followed by the path to a resource DLL, a comma separator, and then a minus sign preceding the decimal string resource identifier.</span></span> <span data-ttu-id="60a86-216">Ad esempio, la risorsa stringa potrebbe essere "Apri rubrica".</span><span class="sxs-lookup"><span data-stu-id="60a86-216">For example, that string resource might be "Open Address Book".</span></span> <span data-ttu-id="60a86-217">Si noti infine che la stringa della riga di comando contiene spazi, quindi è racchiusa tra virgolette.</span><span class="sxs-lookup"><span data-stu-id="60a86-217">Finally, note that the command-line string contains spaces, so it is enclosed in quotation marks.</span></span>

 

 
