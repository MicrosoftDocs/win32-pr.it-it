---
description: Gli utenti possono configurare il debug automatico per consentire loro di determinare il motivo per cui il sistema o un'applicazione ha smesso di rispondere.
ms.assetid: c3c7aa98-c298-452c-b8d0-10a08b4d82a3
title: Configurazione del debug automatico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2630784d678e08b67a93d00ec52d9bc67c949bc7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125748"
---
# <a name="configuring-automatic-debugging"></a><span data-ttu-id="b9b36-103">Configurazione del debug automatico</span><span class="sxs-lookup"><span data-stu-id="b9b36-103">Configuring Automatic Debugging</span></span>

<span data-ttu-id="b9b36-104">Gli utenti possono configurare il debug automatico per consentire loro di determinare il motivo per cui il sistema o un'applicazione ha smesso di rispondere.</span><span class="sxs-lookup"><span data-stu-id="b9b36-104">Users can configure automatic debugging to help them determine why their system or an application has stopped responding.</span></span>

## <a name="configuring-automatic-debugging-for-system-crashes"></a><span data-ttu-id="b9b36-105">Configurazione del debug automatico per arresti anomali del sistema</span><span class="sxs-lookup"><span data-stu-id="b9b36-105">Configuring Automatic Debugging for System Crashes</span></span>

<span data-ttu-id="b9b36-106">Per configurare il computer di destinazione in modo da generare un file di dump di arresto anomalo del sistema quando il sistema smette di rispondere, usare l'applicazione di **sistema** nel pannello di controllo</span><span class="sxs-lookup"><span data-stu-id="b9b36-106">To configure the target computer to generate a crash dump file when the system stops responding, use the **System** application in Control Panel.</span></span> <span data-ttu-id="b9b36-107">Fare clic su **impostazioni di sistema avanzate**, che consente di visualizzare la finestra di dialogo **proprietà del sistema** .</span><span class="sxs-lookup"><span data-stu-id="b9b36-107">Click **Advanced system settings**, which displays the **System Properties** dialog box.</span></span> <span data-ttu-id="b9b36-108">Nella scheda **Avanzate** della casella fare clic su **Impostazioni** in **avvio e ripristino**, quindi utilizzare le opzioni di ripristino appropriate.</span><span class="sxs-lookup"><span data-stu-id="b9b36-108">On the **Advanced** tab of that box, click **Settings** under **Startup and Recovery**, and then use the appropriate recovery options.</span></span> <span data-ttu-id="b9b36-109">In alternativa, è possibile configurare le opzioni di dump di arresto anomalo del sistema utilizzando la seguente chiave del registro</span><span class="sxs-lookup"><span data-stu-id="b9b36-109">Alternatively, you can configure crash dump options using the following registry key:</span></span>

<span data-ttu-id="b9b36-110">**HKEY \_ Controllo CurrentControlSet del sistema del \_ computer locale** \\  \\  \\  \\ **CrashControl**</span><span class="sxs-lookup"><span data-stu-id="b9b36-110">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Control**\\**CrashControl**</span></span>

<span data-ttu-id="b9b36-111">Il file che è possibile specificare è il file di dump di arresto anomalo del sistema.</span><span class="sxs-lookup"><span data-stu-id="b9b36-111">The file you can specify is the crash dump file.</span></span> <span data-ttu-id="b9b36-112">Il nome predefinito è Memory. dmp.</span><span class="sxs-lookup"><span data-stu-id="b9b36-112">Its default name is Memory.dmp.</span></span> <span data-ttu-id="b9b36-113">È possibile eseguire il debug di un dump di arresto anomalo del sistema con un debugger in modalità kernel, ad esempio WinDbg o KD.</span><span class="sxs-lookup"><span data-stu-id="b9b36-113">You can debug a crash dump with a kernel-mode debugger, such as WinDbg or KD.</span></span> <span data-ttu-id="b9b36-114">Per ulteriori informazioni, vedere la documentazione inclusa nel debugger.</span><span class="sxs-lookup"><span data-stu-id="b9b36-114">For more information, see the documentation included with the debugger.</span></span>

## <a name="configuring-automatic-debugging-for-application-crashes"></a><span data-ttu-id="b9b36-115">Configurazione del debug automatico per arresti anomali dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="b9b36-115">Configuring Automatic Debugging for Application Crashes</span></span>

<span data-ttu-id="b9b36-116">Quando un'applicazione smette di rispondere, ad esempio dopo una violazione di accesso, il sistema richiama automaticamente un debugger specificato nel registro di sistema per il debug di post-mortem, l'ID del processo e l'handle di evento vengono passati al debugger se la riga di comando è configurata correttamente.</span><span class="sxs-lookup"><span data-stu-id="b9b36-116">When an application stops responding (for example, after an access violation), the system automatically invokes a debugger that is specified in the registry for postmortem debugging, The process ID and event handle are passed to the debugger if the command line is properly configured.</span></span> <span data-ttu-id="b9b36-117">Nella procedura riportata di seguito viene descritto come specificare un debugger nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="b9b36-117">The following procedure describes how to specify a debugger in the registry.</span></span>

<span data-ttu-id="b9b36-118">**Per impostare un debugger come debugger di post-mortem**</span><span class="sxs-lookup"><span data-stu-id="b9b36-118">**To set a debugger as the postmortem debugger**</span></span>

1.  <span data-ttu-id="b9b36-119">Passare alla chiave del registro di sistema seguente:</span><span class="sxs-lookup"><span data-stu-id="b9b36-119">Go to the following registry key:</span></span>

    <span data-ttu-id="b9b36-120">**HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **AeDebug**</span><span class="sxs-lookup"><span data-stu-id="b9b36-120">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**AeDebug**</span></span>

2.  <span data-ttu-id="b9b36-121">Aggiungere o modificare il valore del **debugger** utilizzando una \_ stringa reg SZ che specifica la riga di comando per il debugger.</span><span class="sxs-lookup"><span data-stu-id="b9b36-121">Add or edit the **Debugger** value, using a REG\_SZ string that specifies the command line for the debugger.</span></span>

    <span data-ttu-id="b9b36-122">La stringa deve includere il percorso completo dell'eseguibile del debugger.</span><span class="sxs-lookup"><span data-stu-id="b9b36-122">The string should include the fully qualified path to the debugger executable.</span></span> <span data-ttu-id="b9b36-123">Indica l'ID processo e l'handle evento con i parametri "% LD" alla riga di comando del debugger.</span><span class="sxs-lookup"><span data-stu-id="b9b36-123">Indicate the process ID and event handle with "%ld" parameters to the debugger command line.</span></span> <span data-ttu-id="b9b36-124">Debugger diversi possono disporre di proprie sintassi dei parametri per indicare questi valori.</span><span class="sxs-lookup"><span data-stu-id="b9b36-124">Different debuggers may have their own parameter syntaxes for indicating these values.</span></span> <span data-ttu-id="b9b36-125">Quando viene richiamato il debugger, il primo "% LD" viene sostituito con l'ID del processo e la seconda "% LD" viene sostituita con l'handle dell'evento.</span><span class="sxs-lookup"><span data-stu-id="b9b36-125">When the debugger is invoked, the first "%ld" is replaced with the process ID and the second "%ld" is replaced with the event handle.</span></span>

    <span data-ttu-id="b9b36-126">Il testo seguente è un esempio di come configurare WinDbg come debugger.</span><span class="sxs-lookup"><span data-stu-id="b9b36-126">The following text is an example of how to setup up WinDbg as the debugger.</span></span>

    ``` syntax
    "C:\debuggers\windbg.exe" -p %ld -e %ld -g
    ```

3.  <span data-ttu-id="b9b36-127">Se si desidera che il debugger venga richiamato senza interazione dell'utente, aggiungere o modificare il valore **auto** utilizzando una \_ stringa reg SZ che specifica se il sistema deve visualizzare una finestra di dialogo per l'utente prima che venga richiamato il debugger.</span><span class="sxs-lookup"><span data-stu-id="b9b36-127">If you want the debugger to be invoked without user interaction, add or edit the **Auto** value, using a REG\_SZ string that specifies whether the system should display a dialog box to the user before the debugger is invoked.</span></span> <span data-ttu-id="b9b36-128">La stringa "1" Disabilita la finestra di dialogo; la stringa "0" Abilita la finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="b9b36-128">The string "1" disables the dialog box; the string "0" enables the dialog box.</span></span>

## <a name="excluding-an-application-from-automatic-debugging"></a><span data-ttu-id="b9b36-129">Esclusione di un'applicazione dal debug automatico</span><span class="sxs-lookup"><span data-stu-id="b9b36-129">Excluding an Application from Automatic Debugging</span></span>

<span data-ttu-id="b9b36-130">Nella procedura seguente viene descritto come escludere un'applicazione dal debug automatico dopo che il valore **auto** sotto la chiave **AeDebug** è stato impostato su 1.</span><span class="sxs-lookup"><span data-stu-id="b9b36-130">The following procedure describes how to exclude an application from automatic debugging after the **Auto** value under the **AeDebug** key has been set to 1.</span></span>

<span data-ttu-id="b9b36-131">**Per escludere un'applicazione dal debug automatico**</span><span class="sxs-lookup"><span data-stu-id="b9b36-131">**To exclude an application from automatic debugging**</span></span>

1.  <span data-ttu-id="b9b36-132">Passare alla chiave del registro di sistema seguente:</span><span class="sxs-lookup"><span data-stu-id="b9b36-132">Go to the following registry key:</span></span>

    <span data-ttu-id="b9b36-133">**HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **AeDebug**</span><span class="sxs-lookup"><span data-stu-id="b9b36-133">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**AeDebug**</span></span>

2.  <span data-ttu-id="b9b36-134">Aggiungere un \_ valore reg DWORD alla sottochiave **autoesclusione** , dove il nome è il nome del file eseguibile e il valore è 1.</span><span class="sxs-lookup"><span data-stu-id="b9b36-134">Add a REG\_DWORD value to the **AutoExclusionList** subkey, where the name is the name of the executable file and the value is 1.</span></span> <span data-ttu-id="b9b36-135">Per impostazione predefinita, il Gestione finestre desktop (Dwm.exe) viene escluso dal debug automatico. in caso contrario, può verificarsi un deadlock del sistema se Dwm.exe smette di rispondere (l'utente non può visualizzare l'interfaccia visualizzata dal debugger perché Dwm.exe non risponde e Dwm.exe non può terminare perché è mantenuta dal debugger).</span><span class="sxs-lookup"><span data-stu-id="b9b36-135">By default, the Desktop Window Manager (Dwm.exe) is excluded from automatic debugging because otherwise a system deadlock can occur if Dwm.exe stops responding (the user cannot see the interface displayed by the debugger because Dwm.exe isn't responding, and Dwm.exe cannot terminate because it is held by the debugger).</span></span>

    <span data-ttu-id="b9b36-136">**Windows Server 2003 e Windows XP:** La sottochiave **autoesclusione** non è disponibile. non è quindi possibile escludere alcuna applicazione, incluso Dwm.exe, dal debug automatico.</span><span class="sxs-lookup"><span data-stu-id="b9b36-136">**Windows Server 2003 and Windows XP:** The **AutoExclusionList** subkey is not available; thus you cannot exclude any application, including Dwm.exe, from automatic debugging.</span></span>

<span data-ttu-id="b9b36-137">Le voci del registro di sistema **AeDebug** predefinite possono essere rappresentate come segue:</span><span class="sxs-lookup"><span data-stu-id="b9b36-137">The default **AeDebug** registry entries can be represented as follows:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows NT
            CurrentVersion
               AeDebug
                  Auto = 1
                  AutoExclusionList
                     DWM.exe = 1
```

## <a name="related-topics"></a><span data-ttu-id="b9b36-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b9b36-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9b36-139">Abilitazione del debug postmortem con WinDbg</span><span class="sxs-lookup"><span data-stu-id="b9b36-139">Enabling Postmortem Debugging with WinDbg</span></span>](/windows-hardware/drivers/debugger/enabling-postmortem-debugging)
</dt> </dl>

 

 
