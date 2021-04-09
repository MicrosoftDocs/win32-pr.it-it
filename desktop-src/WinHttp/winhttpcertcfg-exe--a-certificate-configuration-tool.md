---
description: Lo strumento di configurazione del certificato Microsoft Windows HTTP Services (WinHTTP), &\# 0034; WinHttpCertCfg.exe&\# 0034;, consente agli amministratori di installare e configurare i certificati client in qualsiasi archivio certificati a cui è possibile accedere tramite l'account IWAM (Internet server Web Application Manager). Lo strumento Elimina inoltre la necessità di eseguire operazioni speciali per gli account, ad esempio l'account IWAM, per ottenere l'accesso ai certificati quando si utilizza Active Server Pages (ASP).
ms.assetid: e4c2afc2-0fd3-4bdd-812e-f112958e1576
title: WinHttpCertCfg.exe, uno strumento di configurazione del certificato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4250cd717b9f611f4f23f17c93069760c283c97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129251"
---
# <a name="winhttpcertcfgexe-a-certificate-configuration-tool"></a><span data-ttu-id="b3921-104">WinHttpCertCfg.exe, uno strumento di configurazione del certificato</span><span class="sxs-lookup"><span data-stu-id="b3921-104">WinHttpCertCfg.exe, a Certificate Configuration Tool</span></span>

<span data-ttu-id="b3921-105">Lo strumento di configurazione del certificato [Microsoft Windows HTTP Services (WinHTTP)](about-winhttp.md) , "WinHttpCertCfg.exe", consente agli amministratori di installare e configurare i certificati client in qualsiasi [*archivio certificati*](glossary.md) a cui è possibile accedere tramite l'account di gestione applicazioni Web (IWAM) di Internet Server.</span><span class="sxs-lookup"><span data-stu-id="b3921-105">The [Microsoft Windows HTTP Services (WinHTTP)](about-winhttp.md) certificate configuration tool, "WinHttpCertCfg.exe", enables administrators to install and configure client certificates in any [*certificate store*](glossary.md) that can be accessed by the Internet Server Web Application Manager (IWAM) account.</span></span> <span data-ttu-id="b3921-106">Lo strumento Elimina inoltre la necessità di eseguire operazioni speciali per gli account, ad esempio l'account IWAM, per ottenere l'accesso ai certificati quando si utilizza Active Server Pages (ASP).</span><span class="sxs-lookup"><span data-stu-id="b3921-106">The tool also eliminates the need to do anything special to accounts such as the IWAM account to gain access to certificates when using Active Server Pages (ASP).</span></span>

<span data-ttu-id="b3921-107">Microsoft Management Console (MMC) consente agli amministratori di importare i certificati client in un computer locale.</span><span class="sxs-lookup"><span data-stu-id="b3921-107">The Microsoft Management Console (MMC) enables administrators to import client certificates to a local computer.</span></span> <span data-ttu-id="b3921-108">Tuttavia, l'importazione di un certificato non concede automaticamente l'accesso alla chiave privata per gli altri account.</span><span class="sxs-lookup"><span data-stu-id="b3921-108">However, importing a certificate does not automatically grant access to the private key for other accounts.</span></span> <span data-ttu-id="b3921-109">Questa chiave privata è obbligatoria per l'autenticazione del certificato client.</span><span class="sxs-lookup"><span data-stu-id="b3921-109">This private key is required for client certificate authentication.</span></span> <span data-ttu-id="b3921-110">Lo strumento di configurazione dei certificati Microsoft Windows HTTP Services (WinHTTP) offre la possibilità di concedere l'accesso ad altri account, ad esempio l'account IWAM, quando necessario.</span><span class="sxs-lookup"><span data-stu-id="b3921-110">The Microsoft Windows HTTP Services (WinHTTP) certificate configuration tool provides the ability to grant access to additional accounts, such as the IWAM account, when required.</span></span>

-   [<span data-ttu-id="b3921-111">Utilizzo dello strumento di configurazione dei certificati</span><span class="sxs-lookup"><span data-stu-id="b3921-111">Using the Certificate Configuration Tool</span></span>](#using-the-certificate-configuration-tool)
-   [<span data-ttu-id="b3921-112">esempi</span><span class="sxs-lookup"><span data-stu-id="b3921-112">Examples</span></span>](#examples)

## <a name="using-the-certificate-configuration-tool"></a><span data-ttu-id="b3921-113">Utilizzo dello strumento di configurazione dei certificati</span><span class="sxs-lookup"><span data-stu-id="b3921-113">Using the Certificate Configuration Tool</span></span>

<span data-ttu-id="b3921-114">Lo strumento di configurazione dei certificati WinHTTP, WinHttpCertCfg.exe, è disponibile come download nel sito Web [Windows Server 2003 Resource Kit Tools](https://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd) .</span><span class="sxs-lookup"><span data-stu-id="b3921-114">The WinHTTP certificate configuration tool, WinHttpCertCfg.exe, is available as a download on the [Windows Server 2003 Resource Kit Tools](https://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd) website.</span></span> <span data-ttu-id="b3921-115">Il codice di esempio seguente mostra i parametri della riga di comando validi da usare con questo strumento.</span><span class="sxs-lookup"><span data-stu-id="b3921-115">The following example code shows the valid command line parameters to use with this tool.</span></span>

``` syntax
winhttpcertcfg [-?]
 
winhttpcertcfg [-i PFXFile | -g | -r | -l]
               [-a Account] [-c CertStore] 
               [-s SubjectStr] [-p PFXPassword]
```

<span data-ttu-id="b3921-116">Nella tabella seguente sono elencati i parametri per lo strumento di configurazione di.</span><span class="sxs-lookup"><span data-stu-id="b3921-116">The following table lists parameters for the configuration tool.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b3921-117">Parametro</span><span class="sxs-lookup"><span data-stu-id="b3921-117">Parameter</span></span></th>
<th><span data-ttu-id="b3921-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b3921-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b3921-119">-?</span><span class="sxs-lookup"><span data-stu-id="b3921-119">-?</span></span></td>
<td><span data-ttu-id="b3921-120">Visualizza i dati di sintassi.</span><span class="sxs-lookup"><span data-stu-id="b3921-120">Displays syntax data.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3921-121">-i</span><span class="sxs-lookup"><span data-stu-id="b3921-121">-i</span></span></td>
<td><span data-ttu-id="b3921-122">Specifica che il certificato deve essere importato da un file PFX (Personal Information Exchange).</span><span class="sxs-lookup"><span data-stu-id="b3921-122">Specifies that the certificate is to be imported from a Personal Information Exchange (PFX) file.</span></span> <span data-ttu-id="b3921-123">Questo parametro deve essere seguito dal nome del file.</span><span class="sxs-lookup"><span data-stu-id="b3921-123">This parameter must be followed by the name of the file.</span></span> <span data-ttu-id="b3921-124">Quando si specifica questo parametro, è &quot; &quot; necessario specificare anche-a e &quot; -c &quot; .</span><span class="sxs-lookup"><span data-stu-id="b3921-124">When this parameter is specified, &quot;-a&quot; and &quot;-c&quot; must also be specified.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3921-125">-g</span><span class="sxs-lookup"><span data-stu-id="b3921-125">-g</span></span></td>
<td><span data-ttu-id="b3921-126">Specifica che l'accesso viene concesso a una chiave privata.</span><span class="sxs-lookup"><span data-stu-id="b3921-126">Specifies that access is granted to a private key.</span></span> <span data-ttu-id="b3921-127">Quando si specifica questo parametro, è &quot; &quot; &quot; necessario specificare anche-a,-c &quot; e &quot; -s &quot; .</span><span class="sxs-lookup"><span data-stu-id="b3921-127">When this parameter is specified, &quot;-a&quot;, &quot;-c&quot;, and &quot;-s&quot; must also be specified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3921-128">-r</span><span class="sxs-lookup"><span data-stu-id="b3921-128">-r</span></span></td>
<td><span data-ttu-id="b3921-129">Specifica che l'accesso viene rimosso per una chiave privata.</span><span class="sxs-lookup"><span data-stu-id="b3921-129">Specifies that access is removed for a private key.</span></span> <span data-ttu-id="b3921-130">Quando si specifica questo parametro, è &quot; &quot; &quot; necessario specificare anche-a,-c &quot; e &quot; -s &quot; .</span><span class="sxs-lookup"><span data-stu-id="b3921-130">When this parameter is specified, &quot;-a&quot;, &quot;-c&quot;, and &quot;-s&quot; must also be specified.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3921-131">-l</span><span class="sxs-lookup"><span data-stu-id="b3921-131">-l</span></span></td>
<td><span data-ttu-id="b3921-132">Specifica che sono elencati gli account con accesso a una chiave privata.</span><span class="sxs-lookup"><span data-stu-id="b3921-132">Specifies that accounts with access to a private key are listed.</span></span> <span data-ttu-id="b3921-133">Quando si specifica questo parametro, è &quot; &quot; necessario specificare anche-c e &quot; -s &quot; .</span><span class="sxs-lookup"><span data-stu-id="b3921-133">When this parameter is specified, &quot;-c&quot; and &quot;-s&quot; must also be specified.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3921-134">-a</span><span class="sxs-lookup"><span data-stu-id="b3921-134">-a</span></span></td>
<td><span data-ttu-id="b3921-135">Specifica l'account utente nel computer che si sta configurando.</span><span class="sxs-lookup"><span data-stu-id="b3921-135">Specifies the user account on the machine being configured.</span></span> <span data-ttu-id="b3921-136">Potrebbe trattarsi di un computer locale o di un account di dominio, ad esempio &quot; IWAM_TESTMACHINE &quot; , &quot; TESTUSER &quot; o &quot; TESTDOMAIN\DOMAINUSER &quot; .</span><span class="sxs-lookup"><span data-stu-id="b3921-136">This could be a local machine or domain account, such as &quot;IWAM_TESTMACHINE&quot;, &quot;TESTUSER&quot;, or &quot;TESTDOMAIN\DOMAINUSER&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3921-137">-c</span><span class="sxs-lookup"><span data-stu-id="b3921-137">-c</span></span></td>
<td><span data-ttu-id="b3921-138">Specifica il percorso e il nome dell' <a href="glossary.md"><em>archivio certificati</em></a>.</span><span class="sxs-lookup"><span data-stu-id="b3921-138">Specifies the location and name of the <a href="glossary.md"><em>certificate store</em></a>.</span></span> <span data-ttu-id="b3921-139">Utilizzare &quot; LOCAL_MACHINE &quot; o &quot; CURRENT_USER &quot; per definire il ramo del registro di sistema da utilizzare per la posizione.</span><span class="sxs-lookup"><span data-stu-id="b3921-139">Use &quot;LOCAL_MACHINE&quot; or &quot;CURRENT_USER&quot; to designate which registry branch to use for the location.</span></span> <span data-ttu-id="b3921-140">L' <em>archivio certificati</em> può essere installato nel computer.</span><span class="sxs-lookup"><span data-stu-id="b3921-140">The <em>certificate store</em> can be any installed on the machine.</span></span> <span data-ttu-id="b3921-141">Esempi di nomi tipici sono &quot; My &quot; , &quot; root &quot; e &quot; TrustedPeople &quot; .</span><span class="sxs-lookup"><span data-stu-id="b3921-141">Typical name examples are &quot;MY&quot;, &quot;Root&quot;, and &quot;TrustedPeople&quot;.</span></span> <span data-ttu-id="b3921-142">Il percorso e il nome dell' <em>archivio certificati</em> sono separati da una barra rovesciata, ad esempio &quot; LOCAL_MACHINE \Directory principale &quot; .</span><span class="sxs-lookup"><span data-stu-id="b3921-142">The location and name of the <em>certificate store</em> are separated with a backward slash, for example, &quot;LOCAL_MACHINE\Root&quot;.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="b3921-143">Sebbene &quot; &quot; sia possibile specificare il ramo CURRENT_USER del registro di sistema con questo parametro, l'estensione dell'accesso alle chiavi private è destinata principalmente ai certificati installati in un <a href="glossary.md"><em>archivio certificati</em></a> del computer locale a cui possono accedere più utenti.</span><span class="sxs-lookup"><span data-stu-id="b3921-143">Although the &quot;CURRENT_USER&quot; branch of the registry can be specified with this parameter, extending access to private keys is primarily intended for certificates installed in a local computer <a href="glossary.md"><em>certificate store</em></a> that can be accessed by multiple users.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3921-144">-S</span><span class="sxs-lookup"><span data-stu-id="b3921-144">-s</span></span></td>
<td><span data-ttu-id="b3921-145">Specifica una stringa di ricerca senza distinzione tra maiuscole e minuscole per trovare il primo certificato enumerato con un nome soggetto che contiene la sottostringa.</span><span class="sxs-lookup"><span data-stu-id="b3921-145">Specifies a case-insensitive search string for finding the first enumerated certificate with a subject name that contains this substring.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3921-146">-p</span><span class="sxs-lookup"><span data-stu-id="b3921-146">-p</span></span></td>
<td><span data-ttu-id="b3921-147">Specifica una password utilizzata per importare il certificato e la chiave privata.</span><span class="sxs-lookup"><span data-stu-id="b3921-147">Specifies a password that is used to import the certificate and the private key.</span></span> <span data-ttu-id="b3921-148">Viene utilizzato solo con l'opzione Import.</span><span class="sxs-lookup"><span data-stu-id="b3921-148">This is only used with the import option.</span></span></td>
</tr>
</tbody>
</table>



 

> [!NOTE]
> <span data-ttu-id="b3921-149">L'utente deve disporre di privilegi sufficienti per usare questo strumento, che richiede che l'utente sia un amministratore e lo stesso utente che ha installato il certificato client, se installato.</span><span class="sxs-lookup"><span data-stu-id="b3921-149">The user must have sufficient privileges to use this tool, which requires the user to be an administrator and the same user who installed the client certificate, if installed.</span></span>
>
> <span data-ttu-id="b3921-150">Lo strumento "WinHttpCertCfg.exe" non è utile per configurare i certificati archiviati in un file system, ad esempio FAT32, che non supporta gli elenchi di controllo di accesso (ACL).</span><span class="sxs-lookup"><span data-stu-id="b3921-150">The "WinHttpCertCfg.exe" tool is not useful to configure certificates stored in a file system such as FAT32, which does not support access control lists (ACL).</span></span>

## <a name="examples"></a><span data-ttu-id="b3921-151">Esempio</span><span class="sxs-lookup"><span data-stu-id="b3921-151">Examples</span></span>

<span data-ttu-id="b3921-152">Negli esempi seguenti vengono illustrati alcuni dei modi in cui è possibile utilizzare lo strumento di configurazione.</span><span class="sxs-lookup"><span data-stu-id="b3921-152">The following examples show some of the ways in which the configuration tool can be used.</span></span>

1.  <span data-ttu-id="b3921-153">Questo comando elenca gli account che hanno accesso alla chiave privata per il certificato "certificato" nell' [*archivio certificati*](glossary.md) "radice" del ramo del computer locale \_ del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="b3921-153">This command lists accounts that have access to the private key for the "MyCertificate" certificate in the "Root" [*certificate store*](glossary.md) of the LOCAL\_MACHINE branch of the registry.</span></span>

    <span data-ttu-id="b3921-154">**Winhttpcertcfg-l-c \_ computer locale \\ radice-s certificato**</span><span class="sxs-lookup"><span data-stu-id="b3921-154">**winhttpcertcfg -l -c LOCAL\_MACHINE\\Root -s MyCertificate**</span></span>

2.  <span data-ttu-id="b3921-155">Questo comando concede l'accesso alla chiave privata del certificato "certificato" nell' [*archivio certificati*](glossary.md) "My" per l'account TESTUSER.</span><span class="sxs-lookup"><span data-stu-id="b3921-155">This command grants access to the private key of the "MyCertificate" certificate in the "My" [*certificate store*](glossary.md) for the TESTUSER account.</span></span>

    <span data-ttu-id="b3921-156">**Winhttpcertcfg-g-c \_ computer locale \\ My-s certificato-a TESTUSER**</span><span class="sxs-lookup"><span data-stu-id="b3921-156">**winhttpcertcfg -g -c LOCAL\_MACHINE\\My -s MyCertificate -a TESTUSER**</span></span>

3.  <span data-ttu-id="b3921-157">Questo comando importa un certificato e una chiave privata da un file PFX e estende l'accesso alla chiave privata a un altro account.</span><span class="sxs-lookup"><span data-stu-id="b3921-157">This command imports a certificate and private key from a PFX file and extends private key access to another account.</span></span>

    <span data-ttu-id="b3921-158">**Winhttpcertcfg-i FilePFX-c LOCAL \_ computer \\ My-a IWAM \_ TESTMACHINE-p PFXPassword**</span><span class="sxs-lookup"><span data-stu-id="b3921-158">**winhttpcertcfg -i PFXFile -c LOCAL\_MACHINE\\My -a IWAM\_TESTMACHINE -p PFXPassword**</span></span>

4.  <span data-ttu-id="b3921-159">Questo comando Nega l'accesso alla chiave privata per l'account IWAM \_ TESTMACHINE con il certificato specificato.</span><span class="sxs-lookup"><span data-stu-id="b3921-159">This command denies access to the private key for the IWAM\_TESTMACHINE account with the specified certificate.</span></span>

    <span data-ttu-id="b3921-160">**Winhttpcertcfg-r-c \_ computer locale \\ radice-s certificato-a IWAM \_ TESTMACHINE**</span><span class="sxs-lookup"><span data-stu-id="b3921-160">**winhttpcertcfg -r -c LOCAL\_MACHINE\\Root -s MyCertificate -a IWAM\_TESTMACHINE**</span></span>

 

 




