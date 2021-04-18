---
description: È possibile richiedere che le applicazioni e gli script client stabiliscano una connessione crittografata per l'autenticazione aggiungendo il qualificatore RequiresEncryption al file MOF (Managed Object Format). mof che crea lo spazio dei nomi.
ms.assetid: 07b225a2-3834-4879-beae-f5b9180d112f
ms.tgt_platform: multiple
title: Richiesta di una connessione crittografata a uno spazio dei nomi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e42415c0f714f99a51d6a1a0ee1a0b22f398b1b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318535"
---
# <a name="requiring-an-encrypted-connection-to-a-namespace"></a><span data-ttu-id="35ef3-103">Richiesta di una connessione crittografata a uno spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="35ef3-103">Requiring an Encrypted Connection to a Namespace</span></span>

<span data-ttu-id="35ef3-104">È possibile richiedere che le applicazioni e gli script client stabiliscano una connessione crittografata per l'autenticazione aggiungendo il qualificatore **RequiresEncryption** al file mof (Managed Object Format). mof che crea lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="35ef3-104">You can require that client scripts and applications establish an encrypted connection for authentication by adding the **RequiresEncryption** qualifier to the Managed Object Format (MOF) .mof file that creates the namespace.</span></span>


<span data-ttu-id="35ef3-105">Una connessione crittografata a uno spazio dei nomi WMI specifica il livello di autenticazione **\_ \_ \_ \_ PKT \_** (o **su PktPrivacy** in uno script) RPC C per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="35ef3-105">An encrypted connection to a WMI namespace specifies **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** (or **PktPrivacy** in a script) for authentication.</span></span> <span data-ttu-id="35ef3-106">Il qualificatore **RequiresEncryption** fa in modo che WMI rifiuti le richieste di dati in ingresso a meno che non utilizzi in modo esplicito l'autenticazione crittografata.</span><span class="sxs-lookup"><span data-stu-id="35ef3-106">The **RequiresEncryption** qualifier causes WMI to reject any incoming data requests unless they explicitly use encrypted authentication.</span></span> <span data-ttu-id="35ef3-107">Per ulteriori informazioni, vedere [impostazione del livello di sicurezza del processo predefinito tramite VBScript](setting-the-default-process-security-level-using-vbscript.md) o [impostazione dell'autenticazione mediante C++](setting-authentication-using-c-.md).</span><span class="sxs-lookup"><span data-stu-id="35ef3-107">For more information, see [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md) or [Setting Authentication Using C++](setting-authentication-using-c-.md).</span></span>

<span data-ttu-id="35ef3-108">È anche possibile modificare uno spazio dei nomi esistente aggiungendo questo attributo e quindi compilare nuovamente il file MOF.</span><span class="sxs-lookup"><span data-stu-id="35ef3-108">You can also modify an existing namespace by adding this attribute and then compile the MOF file again.</span></span> <span data-ttu-id="35ef3-109">**RequiresEncryption** viene usato in [*MOF*](gloss-m.md) con l'istruzione del preprocessore [pragma namespace](pragma-namespace.md) .</span><span class="sxs-lookup"><span data-stu-id="35ef3-109">**RequiresEncryption** is used in [*MOF*](gloss-m.md) with the [pragma namespace](pragma-namespace.md) preprocessor instruction.</span></span>

<span data-ttu-id="35ef3-110">La procedura seguente imposta lo spazio dei nomi per richiedere una connessione crittografata.</span><span class="sxs-lookup"><span data-stu-id="35ef3-110">The following procedure sets the namespace to require an encrypted connection.</span></span>

<span data-ttu-id="35ef3-111">**Per impostare la crittografia necessaria**</span><span class="sxs-lookup"><span data-stu-id="35ef3-111">**To set required encryption**</span></span>

1.  <span data-ttu-id="35ef3-112">Creare un file di Managed Object Format (MOF) o modificare il file MOF esistente che definisce lo spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="35ef3-112">Create a Managed Object Format (MOF) file or modify your existing MOF file that defines the namespace.</span></span>

    <span data-ttu-id="35ef3-113">Nell'esempio di codice seguente viene illustrato lo spazio dei nomi che verrà modificato è *root \\ MyNamespace* e il file è denominato *MyNamespace \_ Security. mof*.</span><span class="sxs-lookup"><span data-stu-id="35ef3-113">The following code example shows the namespace that will be modified is *root\\MyNamespace* and the file is named *MyNamespace\_security.mof*.</span></span> <span data-ttu-id="35ef3-114">**RequiresEncryption** ha un tipo di dati booleano, quindi deve essere impostato su **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="35ef3-114">**RequiresEncryption** has a Boolean datatype so it must be set to **True** or **False**.</span></span>

    ```mof
    #pragma namespace("\\\\.\\Root\\MyNamespace") 

    [RequiresEncryption(TRUE)] 
    instance of __systemSecurity { };
    ```

    

2.  <span data-ttu-id="35ef3-115">Eseguire [**mofcomp.exe**](mofcomp.md) per compilare il file MOF.</span><span class="sxs-lookup"><span data-stu-id="35ef3-115">Run [**mofcomp.exe**](mofcomp.md) to compile the MOF file.</span></span>

    <span data-ttu-id="35ef3-116">**c: \\ mofcomp MyNamespace \_ Security. mof**</span><span class="sxs-lookup"><span data-stu-id="35ef3-116">**c:\\mofcomp MyNamespace\_security.mof**</span></span>

    <span data-ttu-id="35ef3-117">In C++ usare i metodi [**IMoFCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .</span><span class="sxs-lookup"><span data-stu-id="35ef3-117">In C++, use the [**IMoFCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) methods.</span></span>

<span data-ttu-id="35ef3-118">WMI rifiuta un client che utilizza il livello di autenticazione predefinito perché DCOM negozia la sicurezza al livello richiesto dal processo SVCHOST in cui è in esecuzione il servizio WMI.</span><span class="sxs-lookup"><span data-stu-id="35ef3-118">WMI rejects a client that uses the default authentication level because DCOM negotiates the security to the level required by the SVCHOST process in which the WMI service is running.</span></span> <span data-ttu-id="35ef3-119">Per ulteriori informazioni sugli host del servizio, vedere [hosting e sicurezza del provider](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="35ef3-119">For more information about service hosts, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span> <span data-ttu-id="35ef3-120">Per ulteriori informazioni su come impostare i livelli di autenticazione durante la connessione agli spazi dei nomi WMI, vedere [impostazione del livello di sicurezza del processo predefinito mediante c++](setting-the-default-process-security-level-using-c-.md), [impostazione dell'autenticazione mediante c++](setting-authentication-using-c-.md)o [impostazione del livello di sicurezza del processo predefinito tramite VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="35ef3-120">For more information about setting authentication levels when connecting to WMI namespaces, see [Setting the Default Process Security Level Using C++](setting-the-default-process-security-level-using-c-.md), [Setting Authentication Using C++](setting-authentication-using-c-.md), or [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span>

<span data-ttu-id="35ef3-121">Quando si restituiscono dati in una connessione di callback asincrona, WMI restituisce un messaggio di accesso negato al computer richiedente.</span><span class="sxs-lookup"><span data-stu-id="35ef3-121">When returning data on an asynchronous callback connection, WMI returns an access denied message to the requesting computer.</span></span> <span data-ttu-id="35ef3-122">WMI rende inoltre una voce di log nel registro eventi NT del computer con lo spazio dei nomi crittografato che informa che non è possibile stabilire una connessione protetta al client.</span><span class="sxs-lookup"><span data-stu-id="35ef3-122">WMI also makes a log entry in the NT Event Log of the computer with the encrypted namespace stating that a secure connection cannot be established to the client.</span></span>

<span data-ttu-id="35ef3-123">A partire da Windows Vista, il file WbemCore. log non esiste più.</span><span class="sxs-lookup"><span data-stu-id="35ef3-123">Starting with Windows Vista, the WbemCore.log file no longer exists.</span></span> <span data-ttu-id="35ef3-124">È possibile controllare il registro eventi NT per le voci che indicano le richieste di dati in ingresso rifiutate agli spazi dei nomi che richiedono la crittografia.</span><span class="sxs-lookup"><span data-stu-id="35ef3-124">You can check the NT Event Log for entries indicating rejected inbound data requests to namespaces that require encryption.</span></span>

## <a name="related-topics"></a><span data-ttu-id="35ef3-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="35ef3-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35ef3-126">Impostazione di descrittori di sicurezza spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="35ef3-126">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="35ef3-127">**WbemAuthenticationLevelEnum**</span><span class="sxs-lookup"><span data-stu-id="35ef3-127">**WbemAuthenticationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[<span data-ttu-id="35ef3-128">Protezione di una connessione WMI remota</span><span class="sxs-lookup"><span data-stu-id="35ef3-128">Securing a Remote WMI Connection</span></span>](securing-a-remote-wmi-connection.md)
</dt> </dl>

 

 



