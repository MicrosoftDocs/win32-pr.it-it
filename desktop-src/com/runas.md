---
title: RunAs
description: Configura una classe per l'esecuzione con un account utente specifico quando viene attivato da un client remoto senza essere scritto come applicazione di servizio.
ms.assetid: 2325a7da-8acd-41f4-a658-36a02532505a
keywords:
- Valore COM del registro di sistema RunAs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3139d12864eb92cc153b919dc4b9b9a4059379d
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300500"
---
# <a name="runas"></a><span data-ttu-id="efeac-104">RunAs</span><span class="sxs-lookup"><span data-stu-id="efeac-104">RunAs</span></span>

<span data-ttu-id="efeac-105">Configura una classe per l'esecuzione con un account utente specifico quando viene attivato da un client remoto senza essere scritto come applicazione di servizio.</span><span class="sxs-lookup"><span data-stu-id="efeac-105">Configures a class to run under a specific user account when activated by a remote client without being written as a service application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="efeac-106">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="efeac-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      RunAs = value
```

## <a name="remarks"></a><span data-ttu-id="efeac-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="efeac-107">Remarks</span></span>

<span data-ttu-id="efeac-108">Il valore specifica il nome utente e deve essere del formato *username*, *Domain ***\\*** username* o della stringa "Interactive User".</span><span class="sxs-lookup"><span data-stu-id="efeac-108">The value specifies the user name and must be either of the form *UserName*, *Domain ***\\*** UserName* or of the string "Interactive User".</span></span> <span data-ttu-id="efeac-109">È inoltre possibile specificare le stringhe "NT Authority \\ LocalService" (per il servizio locale) e "NT Authority \\ NetworkService" (per servizio di rete).</span><span class="sxs-lookup"><span data-stu-id="efeac-109">You can also specify the strings "nt authority\\localservice" (for Local Service) and "nt authority\\networkservice" (for Network Service).</span></span> <span data-ttu-id="efeac-110">È inoltre possibile specificare la stringa "NT Authority \\ System" quando {*AppID \_ GUID*} fa riferimento a un server com già avviato o con una voce nella tabella della classe.</span><span class="sxs-lookup"><span data-stu-id="efeac-110">You can also specify the string "nt authority\\system" when {*AppID\_GUID*} refers to a COM server that is already started or that has an entry in the class table.</span></span> <span data-ttu-id="efeac-111">Tuttavia, non è possibile utilizzare "NT Authority \\ System" con un server com non ancora avviato.</span><span class="sxs-lookup"><span data-stu-id="efeac-111">However, you cannot use "nt authority\\system" with a COM server that is not already started.</span></span> <span data-ttu-id="efeac-112">La password predefinita per "NT Authority \\ LocalService", "NT Authority \\ NetworkService" e "NT Authority \\ System" è "" (stringa vuota).</span><span class="sxs-lookup"><span data-stu-id="efeac-112">The default password for "nt authority\\localservice", "nt authority\\networkservice", and "nt authority\\system" is "" (empty string).</span></span>

> [!Note]  
> <span data-ttu-id="efeac-113">A partire da Windows Vista, non è più necessaria una password vuota per configurare le \\ Impostazioni RunAs "NT Authority LocalService", "NT Authority \\ NetworkService" e "NT Authority \\ System". </span><span class="sxs-lookup"><span data-stu-id="efeac-113">As of Windows Vista, an empty password is no longer required to configure the "nt authority\\localservice", "nt authority\\networkservice" and "nt authority\\system" **RunAs** settings.</span></span>

 

<span data-ttu-id="efeac-114">Le classi configurate per l'esecuzione come utente specifico potrebbero non essere registrate con altre identità, quindi le chiamate a [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) con questo CLSID hanno esito negativo a meno che il processo non sia stato avviato da com per conto di una richiesta di attivazione effettiva.</span><span class="sxs-lookup"><span data-stu-id="efeac-114">Classes configured to run as a particular user may not be registered under any other identity, so calls to [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) with this CLSID fail unless the process was launched by COM on behalf of an actual activation request.</span></span>

<span data-ttu-id="efeac-115">Il nome utente viene tratto dal valore **RunAs** sotto la chiave **AppID** della classe.</span><span class="sxs-lookup"><span data-stu-id="efeac-115">The user-name is taken from the **RunAs** value under the class's **AppID** key.</span></span> <span data-ttu-id="efeac-116">Se il nome utente è "utente interattivo", il server viene eseguito con l'identità dell'utente attualmente connesso ed è connesso al desktop interattivo.</span><span class="sxs-lookup"><span data-stu-id="efeac-116">If the user name is "Interactive User", the server is run in the identity of the user currently logged on and is connected to the interactive desktop.</span></span>

<span data-ttu-id="efeac-117">In caso contrario, la password viene recuperata da una parte del registro di sistema disponibile solo per gli amministratori del computer e del sistema.</span><span class="sxs-lookup"><span data-stu-id="efeac-117">Otherwise, the password is retrieved from a portion of the registry that is available only to administrators of the computer and to the system.</span></span> <span data-ttu-id="efeac-118">Il nome utente e la password vengono quindi utilizzati per creare una sessione di accesso in cui viene eseguito il server.</span><span class="sxs-lookup"><span data-stu-id="efeac-118">The user-name and password are then used to create a logon session in which the server is run.</span></span> <span data-ttu-id="efeac-119">Quando viene avviato in questo modo, l'utente viene eseguito con il proprio desktop e la propria stazione di Windows e non condivide gli handle di finestra, gli Appunti o altri elementi dell'interfaccia utente con l'utente interattivo o con un altro utente in esecuzione in altri account utente.</span><span class="sxs-lookup"><span data-stu-id="efeac-119">When launched in this way, the user runs with its own desktop and window station and does not share window-handles, the clipboard, or other UI elements with the interactive user or other user running in other user accounts.</span></span>

<span data-ttu-id="efeac-120">Per stabilire una password per una classe **RunAs** , è necessario utilizzare lo strumento di amministrazione DCOMCNFG installato nella directory di sistema.</span><span class="sxs-lookup"><span data-stu-id="efeac-120">To establish a password for a **RunAs** class, you must use the DCOMCNFG administrative tool installed in the system directory.</span></span>

<span data-ttu-id="efeac-121">Per le identità **RunAs** utilizzate dai server DCOM, l'account utente specificato nel valore deve disporre dei diritti di accesso come processo batch.</span><span class="sxs-lookup"><span data-stu-id="efeac-121">For **RunAs** identities used by DCOM servers, the user account specified in the value must have the rights to log on as a batch job.</span></span> <span data-ttu-id="efeac-122">Questo diritto può essere aggiunto utilizzando lo strumento di amministrazione Criteri di sicurezza locali.</span><span class="sxs-lookup"><span data-stu-id="efeac-122">This right can be added using Local Security Policy administrative tool.</span></span> <span data-ttu-id="efeac-123">Passare a **criteri locali** e aprire **assegnazione diritti utente**.</span><span class="sxs-lookup"><span data-stu-id="efeac-123">Go to **Local Policies** and open **User Rights Assignment**.</span></span> <span data-ttu-id="efeac-124">Selezionare **Accedi come processo batch** e aggiungere l'account utente.</span><span class="sxs-lookup"><span data-stu-id="efeac-124">Select **Log on as a batch job**, and add the user account.</span></span>

<span data-ttu-id="efeac-125">Il valore **RunAs** non viene utilizzato per i server configurati per l'esecuzione come servizi.</span><span class="sxs-lookup"><span data-stu-id="efeac-125">The **RunAs** value is not used for servers configured to be run as services.</span></span> <span data-ttu-id="efeac-126">I servizi COM che devono essere eseguiti con un'identità diversa da LocalSystem devono impostare il nome utente e la password appropriati utilizzando l'applet del pannello di controllo dei servizi o le funzioni del controller di servizio.</span><span class="sxs-lookup"><span data-stu-id="efeac-126">COM services that need to run under an identity other than LocalSystem should set the appropriate user name and password using the services control panel applet or the service controller functions.</span></span> <span data-ttu-id="efeac-127">Per ulteriori informazioni su queste funzioni, vedere [Servizi](/windows/desktop/Services/services).</span><span class="sxs-lookup"><span data-stu-id="efeac-127">(For more information about these functions, see [Services](/windows/desktop/Services/services).)</span></span>

> [!Note]  
> <span data-ttu-id="efeac-128">A partire da Microsoft Windows Server 2003, la classe AppID viene letta in modo esplicito dalle **\_ \_ classi software del computer locale HKEY \\ \\ \\ AppID**, che, a differenza della maggior parte delle chiavi del registro di sistema, non è interscambiabile con le **\_ classi HKEY \_ radice \\ AppID**.</span><span class="sxs-lookup"><span data-stu-id="efeac-128">As of Microsoft Windows Server 2003, the class AppID is explicitly read from **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\AppID**, which, unlike most registry keys, is not interchangeable with **HKEY\_CLASSES\_ROOT\\AppID**.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="efeac-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="efeac-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="efeac-130">Registrazione di server COM</span><span class="sxs-lookup"><span data-stu-id="efeac-130">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> </dl>

 

 