---
description: Le operazioni con privilegi richiedono privilegi di sicurezza, ad esempio SeLoadDriverPrivilege (wbemPrivilegeLoadDriver nelle costanti API di scripting), un privilegio che deve essere abilitato per un account che sta caricando un driver di dispositivo.
ms.assetid: 11bb8723-f329-4083-8219-2256ce44a5e3
ms.tgt_platform: multiple
title: Esecuzione di operazioni con privilegi
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 37abba9d774025825611e311f08414b50e660f65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310353"
---
# <a name="executing-privileged-operations"></a><span data-ttu-id="b25be-103">Esecuzione di operazioni con privilegi</span><span class="sxs-lookup"><span data-stu-id="b25be-103">Executing Privileged Operations</span></span>

<span data-ttu-id="b25be-104">Le operazioni con privilegi richiedono privilegi di sicurezza, ad esempio **SeLoadDriverPrivilege** (**WBEMPRIVILEGELOADDRIVER** nelle [costanti API di scripting](scripting-api-constants.md)), un privilegio che deve essere abilitato per un account che sta caricando un driver di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b25be-104">Privileged operations require security privileges such as **SeLoadDriverPrivilege** (**wbemPrivilegeLoadDriver** in the [Scripting API Constants](scripting-api-constants.md)), a privilege that must be enabled for an account that is loading a device driver.</span></span> <span data-ttu-id="b25be-105">Non è possibile aggiungere privilegi a un amministratore o a un utente tramite WMI. è possibile abilitare solo i privilegi già presenti nell'account.</span><span class="sxs-lookup"><span data-stu-id="b25be-105">You cannot add privileges to an administrator or user through WMI, you can only enable privileges that the account already has.</span></span> <span data-ttu-id="b25be-106">Per un elenco dei privilegi, vedere [**\_ costanti Privilege**](privilege-constants.md).</span><span class="sxs-lookup"><span data-stu-id="b25be-106">For a list of privileges, see [**Privilege\_Constants**](privilege-constants.md).</span></span>

<span data-ttu-id="b25be-107">Per impostazione predefinita, un utente locale in un computer può leggere i dati statici dal [*repository WMI*](gloss-w.md), scrivere nelle istanze fornite dai provider ed eseguire i metodi del provider, a meno che il provider non imponga specifici requisiti di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="b25be-107">By default, a local user on a computer can read static data from the [*WMI repository*](gloss-w.md), write to instances supplied by providers, and execute provider methods, unless the provider enforces special security requirements of its own.</span></span> <span data-ttu-id="b25be-108">Solo gli amministratori possono [connettersi a un computer remoto](connecting-to-wmi-on-a-remote-computer.md), modificare i descrittori di sicurezza o modificare i dati del repository WMI statici, ad esempio una definizione di classe WMI.</span><span class="sxs-lookup"><span data-stu-id="b25be-108">Only administrators can [connect to a remote computer](connecting-to-wmi-on-a-remote-computer.md), change security descriptors, or change static WMI repository data, such as a WMI class definition.</span></span> <span data-ttu-id="b25be-109">Tutti i privilegi sono abilitati per una connessione remota.</span><span class="sxs-lookup"><span data-stu-id="b25be-109">All privileges are enabled for a remote connection.</span></span> <span data-ttu-id="b25be-110">Per ulteriori informazioni, vedere [protezione di una connessione WMI remota](securing-a-remote-wmi-connection.md).</span><span class="sxs-lookup"><span data-stu-id="b25be-110">For more information, see [Securing a Remote WMI Connection](securing-a-remote-wmi-connection.md).</span></span>

<span data-ttu-id="b25be-111">Le costanti dei privilegi per C++ sono diverse da quelle utilizzate dai linguaggi di automazione, ad esempio Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="b25be-111">The privilege constants for C++ differ from those that are used by automation languages such as Visual Basic.</span></span> <span data-ttu-id="b25be-112">Gli script devono usare il valore della costante anziché il nome.</span><span class="sxs-lookup"><span data-stu-id="b25be-112">Scripts must use the value of the constant rather than the name.</span></span> <span data-ttu-id="b25be-113">Per altre informazioni, vedere [esecuzione di operazioni con privilegi con C++](executing-privileged-operations-using-c-.md) o [esecuzione di operazioni con privilegi tramite VBScript](executing-privileged-operations-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="b25be-113">For more information, see [Executing Privileged Operations Using C++](executing-privileged-operations-using-c-.md) or [Executing Privileged Operations Using VBScript](executing-privileged-operations-using-vbscript.md).</span></span>

<span data-ttu-id="b25be-114">Una causa comune degli errori di accesso negato quando si utilizza WMI è la mancanza di un privilegio abilitato per le operazioni, ad esempio il recupero di tutte le istanze di [**Win32 \_ NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b25be-114">A common cause of access denied errors when using WMI is the lack of an enabled privilege for operations, such as getting all instances of [**Win32\_NTEventlogFile**](/previous-versions/windows/desktop/legacy/aa394225(v=vs.85)).</span></span> <span data-ttu-id="b25be-115">Se non si Abilita il privilegio di **sesecurity** , non è possibile accedere al file di registro di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="b25be-115">Without enabling the **SeSecurity** privilege, you cannot access the Security log file.</span></span>

<span data-ttu-id="b25be-116">Nell'esempio di codice VBScript riportato di seguito viene illustrato come impostare il privilegio di **sesicurezza** nella stringa del moniker.</span><span class="sxs-lookup"><span data-stu-id="b25be-116">The following VBScript code example shows how to set the **SeSecurity** privilege in the moniker string.</span></span> <span data-ttu-id="b25be-117">Quando viene usato nel moniker, il nome del privilegio tra parentesi Elimina il "se" iniziale.</span><span class="sxs-lookup"><span data-stu-id="b25be-117">When used in the moniker, the privilege name in parentheses drops the initial "Se".</span></span> <span data-ttu-id="b25be-118">Per ulteriori informazioni, vedere [creazione di una stringa di moniker](constructing-a-moniker-string.md).</span><span class="sxs-lookup"><span data-stu-id="b25be-118">For more information, see [Constructing a Moniker String](constructing-a-moniker-string.md).</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate,(Security)}!\\" _
    & strComputer & "\root\cimv2")
Set colFiles = objWMIService.ExecQuery _
    ("Select * from Win32_NTEventLogFile " _
    & "Where LogFileName='Security'")
For Each LogFile in colFiles
Wscript.Echo LogFile.NumberOfRecords
Next
```



## <a name="related-topics"></a><span data-ttu-id="b25be-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b25be-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b25be-120">**Costanti Privilege**</span><span class="sxs-lookup"><span data-stu-id="b25be-120">**Privilege Constants**</span></span>](privilege-constants.md)
</dt> </dl>

 

 
