---
title: Uso dei cmdlet di Windows PowerShell per WMI per gestire BITS Compact Server
description: Windows PowerShell fornisce un meccanismo semplice per connettersi a Strumentazione gestione Windows (WMI) in un computer remoto e gestire il server di Servizio trasferimento intelligente in background (BITS) Compact.
ms.assetid: fe174d2f-4ca0-431e-b1b8-1893ec54147a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c3c942672c147ec5daa0caa2a370e487be80809
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963252"
---
# <a name="using-wmi-windows-powershell-cmdlets-to-manage-the-bits-compact-server"></a><span data-ttu-id="2becf-103">Uso dei cmdlet di Windows PowerShell per WMI per gestire BITS Compact Server</span><span class="sxs-lookup"><span data-stu-id="2becf-103">Using WMI Windows PowerShell Cmdlets to Manage the BITS Compact Server</span></span>

<span data-ttu-id="2becf-104">Windows PowerShell fornisce un meccanismo semplice per connettersi a Strumentazione gestione Windows (WMI) in un computer remoto e gestire il server di Servizio trasferimento intelligente in background (BITS) Compact.</span><span class="sxs-lookup"><span data-stu-id="2becf-104">Windows PowerShell provides a simple mechanism to connect to Windows Management Instrumentation (WMI) on a remote computer and manage the Background Intelligent Transfer Service (BITS) Compact Server.</span></span> <span data-ttu-id="2becf-105">BITS Compact Server è un componente server facoltativo che deve essere installato separatamente.</span><span class="sxs-lookup"><span data-stu-id="2becf-105">The BITS Compact Server is an optional server component that must be installed separately.</span></span> <span data-ttu-id="2becf-106">Per informazioni sull'installazione di Compact Server, vedere la documentazione di [BITS Compact Server](bits-compact-server.md) .</span><span class="sxs-lookup"><span data-stu-id="2becf-106">For information about installing the Compact Server, see the [BITS Compact Server](bits-compact-server.md) documentation.</span></span>

1.  <span data-ttu-id="2becf-107">Connettersi al provider BITS.</span><span class="sxs-lookup"><span data-stu-id="2becf-107">Connect to the BITS provider.</span></span>

    ```PowerShell
    $cred = Get-Credential
    $bcs = Get-WmiObject -Namespace "root\Microsoft\BITS" -Class "BITSCompactServerUrlGroup" `
    -List -ComputerName Server1 -Credential $cred
    ```

    

    <span data-ttu-id="2becf-108">Il cmdlet [Get-Credential](/previous-versions//dd315327(v=technet.10)) richiede le credenziali dell'utente per connettersi al computer remoto e assegna le credenziali all'oggetto $cred.</span><span class="sxs-lookup"><span data-stu-id="2becf-108">The [Get-Credential](/previous-versions//dd315327(v=technet.10)) cmdlet requests the user's credentials to connect to the remote computer and assigns the credentials to the $cred object.</span></span>

    <span data-ttu-id="2becf-109">Gli oggetti restituiti dal cmdlet [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) vengono assegnati alla variabile $BCS.</span><span class="sxs-lookup"><span data-stu-id="2becf-109">The objects returned by the [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) cmdlet are assigned to the $bcs variable.</span></span> <span data-ttu-id="2becf-110">Nell'esempio precedente, il cmdlet [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) recupera la classe [BITSCompactServerUrlGroup](/previous-versions/windows/desktop/bitsprov/bitslightweightserverurlgroup) nello \\ \\ spazio dei nomi Microsoft bits radice di Server1.</span><span class="sxs-lookup"><span data-stu-id="2becf-110">In the preceding example, the [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) cmdlet retrieves the [BITSCompactServerUrlGroup](/previous-versions/windows/desktop/bitsprov/bitslightweightserverurlgroup) class in the root\\Microsoft\\BITS namespace of Server1.</span></span> <span data-ttu-id="2becf-111">I metodi statici esposti dalla classe [BITSCompactServerUrlGroup](/previous-versions/windows/desktop/bitsprov/bitslightweightserverurlgroup) possono essere chiamati sull'oggetto $BCS.</span><span class="sxs-lookup"><span data-stu-id="2becf-111">Static methods exposed by the [BITSCompactServerUrlGroup](/previous-versions/windows/desktop/bitsprov/bitslightweightserverurlgroup) class can be called on the $bcs object.</span></span> <span data-ttu-id="2becf-112">Per ulteriori informazioni sulla gestione remota BITS, vedere classi del [provider bits e](/previous-versions/windows/desktop/bitsprov/bits-provider) del [provider bits]( /previous-versions//dd904507(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2becf-112">For more information about BITS remote management, see [BITS provider](/previous-versions/windows/desktop/bitsprov/bits-provider) and [BITS provider classes]( /previous-versions//dd904507(v=vs.85)).</span></span>

    > [!Note]  
    > <span data-ttu-id="2becf-113">Il carattere di accento grave ( \` ) viene usato per indicare un'interruzioni di riga.</span><span class="sxs-lookup"><span data-stu-id="2becf-113">The grave-accent character (\`) is used to indicate a line break.</span></span>

     

2.  <span data-ttu-id="2becf-114">Creare un gruppo di URL nel server.</span><span class="sxs-lookup"><span data-stu-id="2becf-114">Create a URL group on the server.</span></span>

    ```PowerShell
    $URLGroup = "https://Server1:80/testurlgroup" 
    $bcs.CreateUrlGroup($URLGroup)
    ```

    

    <span data-ttu-id="2becf-115">La https://Server1:80/testurlgroup stringa del prefisso URL "" viene assegnata alla variabile $URLGroup.</span><span class="sxs-lookup"><span data-stu-id="2becf-115">The "https://Server1:80/testurlgroup" URL prefix string is assigned to the $URLGroup variable.</span></span> <span data-ttu-id="2becf-116">La variabile $URLGroup viene passata al metodo [CreateUrlGroup](/previous-versions/windows/desktop/bitsprov/createurlgroup-bitslightweightserverurlgroup) , che crea il gruppo di URL in Server1.</span><span class="sxs-lookup"><span data-stu-id="2becf-116">The $URLGroup variable is passed to the [CreateUrlGroup](/previous-versions/windows/desktop/bitsprov/createurlgroup-bitslightweightserverurlgroup) method, which creates the URL group on Server1.</span></span>

    <span data-ttu-id="2becf-117">È possibile specificare un gruppo di URL diverso.</span><span class="sxs-lookup"><span data-stu-id="2becf-117">You can specify a different URL group.</span></span> <span data-ttu-id="2becf-118">Il gruppo di URL deve essere conforme a una stringa di prefisso URL valida.</span><span class="sxs-lookup"><span data-stu-id="2becf-118">The URL group must conform to a valid URL prefix string.</span></span> <span data-ttu-id="2becf-119">Per ulteriori informazioni sui prefissi URL, vedere [URLPrefix Strings](../http/urlprefix-strings.md).</span><span class="sxs-lookup"><span data-stu-id="2becf-119">For more information about URL prefixes, see [UrlPrefix Strings](../http/urlprefix-strings.md).</span></span>

3.  <span data-ttu-id="2becf-120">Ospitare un file nel gruppo di URL.</span><span class="sxs-lookup"><span data-stu-id="2becf-120">Host a file on the URL group.</span></span>

    ```PowerShell
    $bcsObj = Get-WmiObject -Namespace "root\Microsoft\BITS" -Class "BITSCompactServerUrlGroup" -filter ("UrlGroup='" + $URLGroup + "'") -ComputerName Server1 -Credential $cred
    $bcsObj.CreateURL("url.txt", "c:\\temp\\1.txt", "") -ComputerName Server1 -Credential $cred
    ```

    

    <span data-ttu-id="2becf-121">L'istanza di BITSCompactServerUrlGroup restituita dal cmdlet [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) viene assegnata alla variabile $bcsObj.</span><span class="sxs-lookup"><span data-stu-id="2becf-121">The BITSCompactServerUrlGroup instance returned by the [Get-WmiObject](/previous-versions//dd315295(v=technet.10)) cmdlet is assigned to the $bcsObj variable.</span></span> <span data-ttu-id="2becf-122">Il metodo [CreateURL](/previous-versions/windows/desktop/bitsprov/createurl-bitslightweightserverurlgroup) viene chiamato per il $bcsObj con il suffisso "url.txt" URL, il \\ \\ percorso di origine "c: temp \\ \\1.txt" per il file e una stringa del descrittore di sicurezza vuota come parametri.</span><span class="sxs-lookup"><span data-stu-id="2becf-122">The [CreateUrl](/previous-versions/windows/desktop/bitsprov/createurl-bitslightweightserverurlgroup) method is called for the $bcsObj with the "url.txt" URL suffix, the "c:\\\\temp\\\\1.txt" source path for the file, and an empty security descriptor string as parameters.</span></span> <span data-ttu-id="2becf-123">Il suffisso "url.txt" viene aggiunto al prefisso del gruppo di URL.</span><span class="sxs-lookup"><span data-stu-id="2becf-123">The "url.txt" suffix is added to the URL group prefix.</span></span> <span data-ttu-id="2becf-124">I client possono scaricare il file dall'indirizzo seguente: https://Server1:80/testurlgroup/url.txt .</span><span class="sxs-lookup"><span data-stu-id="2becf-124">Clients can download the file from the following address: https://Server1:80/testurlgroup/url.txt.</span></span>

4.  <span data-ttu-id="2becf-125">Pulire l'URL e il gruppo di URL.</span><span class="sxs-lookup"><span data-stu-id="2becf-125">Clean up the URL and the URL group.</span></span>

    ```PowerShell
    $bcsObj.Delete()
    ```

    

    <span data-ttu-id="2becf-126">Il metodo **System. Object Delete** Elimina l'oggetto $bcsObj.</span><span class="sxs-lookup"><span data-stu-id="2becf-126">The **system.object Delete** method deletes the $bcsObj object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2becf-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2becf-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2becf-128">BITS Compact Server</span><span class="sxs-lookup"><span data-stu-id="2becf-128">BITS Compact Server</span></span>](./bits-compact-server.md)
</dt> <dt>

[<span data-ttu-id="2becf-129">Provider BITS</span><span class="sxs-lookup"><span data-stu-id="2becf-129">BITS provider</span></span>](/previous-versions/windows/desktop/bitsprov/bits-provider)
</dt> <dt>

<span data-ttu-id="2becf-130">[Classi del provider BITS]( /previous-versions//dd904507(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2becf-130">[BITS provider classes]( /previous-versions//dd904507(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="2becf-131">[Get-Credential](/previous-versions//dd315327(v=technet.10))</span><span class="sxs-lookup"><span data-stu-id="2becf-131">[Get-Credential](/previous-versions//dd315327(v=technet.10))</span></span>
</dt> <dt>

<span data-ttu-id="2becf-132">[Get-WmiObject](/previous-versions//dd315295(v=technet.10))</span><span class="sxs-lookup"><span data-stu-id="2becf-132">[Get-WmiObject](/previous-versions//dd315295(v=technet.10))</span></span>
</dt> </dl>

 

 