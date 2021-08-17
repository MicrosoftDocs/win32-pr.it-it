---
description: Lo strumento di configurazione dei certificati Microsoft Windows HTTP Services (WinHTTP), &\# 0034;WinHttpCertCfg.exe&0034;, consente agli amministratori di installare e configurare i certificati client in qualsiasi archivio certificati accessibile \# dall'account IWAM (Internet Server Web Application Manager). Lo strumento elimina anche la necessità di eseguire qualsiasi operazione speciale per gli account, ad esempio l'account IWAM, per ottenere l'accesso ai certificati quando si usa Active Server Pages (ASP).
ms.assetid: e4c2afc2-0fd3-4bdd-812e-f112958e1576
title: WinHttpCertCfg.exe, uno strumento di configurazione del certificato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51ce9978f6e2ffcafa1357a45dbeff80c12bf0e6ea2f7f3fb9656376b33dfb23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743799"
---
# <a name="winhttpcertcfgexe-a-certificate-configuration-tool"></a>WinHttpCertCfg.exe, uno strumento di configurazione del certificato

Lo strumento di configurazione del certificato "WinHttpCertCfg.exe" di Servizi HTTP di Microsoft Windows [(WinHTTP)](about-winhttp.md) consente agli amministratori di installare e configurare i certificati client in qualsiasi archivio certificati accessibile dall'account IWAM (Internet Server Web Application Manager). [](glossary.md) Lo strumento elimina anche la necessità di eseguire qualsiasi operazione speciale per gli account, ad esempio l'account IWAM, per ottenere l'accesso ai certificati quando si usa Active Server Pages (ASP).

La Microsoft Management Console (MMC) consente agli amministratori di importare i certificati client in un computer locale. Tuttavia, l'importazione di un certificato non concede automaticamente l'accesso alla chiave privata per altri account. Questa chiave privata è necessaria per l'autenticazione del certificato client. Lo strumento di configurazione dei certificati Microsoft Windows Servizi HTTP (WinHTTP) consente di concedere l'accesso ad altri account, ad esempio l'account IWAM, quando necessario.

-   [Uso dello strumento di configurazione del certificato](#using-the-certificate-configuration-tool)
-   [esempi](#examples)

## <a name="using-the-certificate-configuration-tool"></a>Uso dello strumento di configurazione del certificato

Lo strumento di configurazione del certificato WinHTTP, WinHttpCertCfg.exe, è disponibile come download nel sito Web degli strumenti [di Windows Server 2003 Resource Kit.](https://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd) Il codice di esempio seguente illustra i parametri della riga di comando validi da usare con questo strumento.

``` syntax
winhttpcertcfg [-?]
 
winhttpcertcfg [-i PFXFile | -g | -r | -l]
               [-a Account] [-c CertStore] 
               [-s SubjectStr] [-p PFXPassword]
```

Nella tabella seguente sono elencati i parametri per lo strumento di configurazione.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Parametro</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>-?</td>
<td>Visualizza i dati della sintassi.</td>
</tr>
<tr class="even">
<td>-i</td>
<td>Specifica che il certificato deve essere importato da un file PFX (Personal Information Exchange). Questo parametro deve essere seguito dal nome del file. Quando si specifica questo parametro, è necessario specificare anche -a e &quot; &quot; &quot; &quot; -c.</td>
</tr>
<tr class="odd">
<td>-g</td>
<td>Specifica che l'accesso viene concesso a una chiave privata. Quando si specifica questo parametro, è necessario specificare anche &quot; &quot; &quot; -a , -c &quot; e &quot; &quot; -s.</td>
</tr>
<tr class="even">
<td>-r</td>
<td>Specifica che l'accesso viene rimosso per una chiave privata. Quando si specifica questo parametro, è necessario specificare anche &quot; &quot; &quot; -a , -c &quot; e &quot; &quot; -s.</td>
</tr>
<tr class="odd">
<td>-l</td>
<td>Specifica che vengono elencati gli account con accesso a una chiave privata. Quando si specifica questo parametro, è necessario specificare anche -c e &quot; &quot; &quot; &quot; -s.</td>
</tr>
<tr class="even">
<td>-a</td>
<td>Specifica l'account utente nel computer da configurare. Può trattarsi di un computer locale o di un account di dominio, ad esempio &quot; IWAM_TESTMACHINE &quot; , &quot; TESTUSER o &quot; &quot; TESTDOMAIN\DOMAINUSER &quot; .</td>
</tr>
<tr class="odd">
<td>-c</td>
<td>Specifica il percorso e il nome <a href="glossary.md"><em>dell'archivio certificati</em></a>. Usare &quot; LOCAL_MACHINE o CURRENT_USER &quot; &quot; &quot; designare il ramo del Registro di sistema da usare per il percorso. <em>L'archivio</em> certificati può essere qualsiasi installato nel computer. Esempi di nomi tipici &quot; sono &quot; &quot; MY, Root &quot; e &quot; TrustedPeople. &quot; Il percorso e il nome <em>dell'archivio</em> certificati sono separati da una barra rovesciata, ad esempio &quot; LOCAL_MACHINE\Root &quot; .
<blockquote>
[!Note]<br />
Anche se il ramo CURRENT_USER del Registro di sistema può essere specificato con questo parametro, l'estensione dell'accesso alle chiavi private è destinata principalmente ai certificati installati in un archivio certificati del computer locale a cui possono accedere più &quot; &quot; utenti. <a href="glossary.md"><em></em></a>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>-S</td>
<td>Specifica una stringa di ricerca senza distinzione tra maiuscole e minuscole per trovare il primo certificato enumerato con un nome soggetto che contiene questa sottostringa.</td>
</tr>
<tr class="odd">
<td>-p</td>
<td>Specifica una password utilizzata per importare il certificato e la chiave privata. Viene usato solo con l'opzione import.</td>
</tr>
</tbody>
</table>



 

> [!NOTE]
> L'utente deve disporre di privilegi sufficienti per usare questo strumento, che richiede che l'utente sia un amministratore e lo stesso utente che ha installato il certificato client, se installato.
>
> Lo strumento "WinHttpCertCfg.exe" non è utile per configurare i certificati archiviati in un file system, ad esempio FAT32, che non supporta gli elenchi di controllo di accesso (ACL).

## <a name="examples"></a>Esempio

Gli esempi seguenti illustrano alcuni dei modi in cui è possibile usare lo strumento di configurazione.

1.  Questo comando elenca gli account che hanno accesso alla chiave privata per [](glossary.md) il certificato "MyCertificate" nell'archivio certificati "Radice" del ramo LOCAL \_ MACHINE del Registro di sistema.

    **winhttpcertcfg -l -c LOCAL \_ MACHINE \\ Root -s MyCertificate**

2.  Questo comando concede l'accesso alla chiave privata del certificato "MyCertificate" nell'archivio certificati [*"My"*](glossary.md) per l'account TESTUSER.

    **winhttpcertcfg -g -c LOCAL \_ MACHINE \\ My -s MyCertificate -a TESTUSER**

3.  Questo comando importa un certificato e una chiave privata da un file PFX ed estende l'accesso alla chiave privata a un altro account.

    **winhttpcertcfg -i PFXFile -c LOCAL \_ MACHINE \\ My -a IWAM \_ TESTMACHINE -p PFXPassword**

4.  Questo comando nega l'accesso alla chiave privata per l'account TESTMACHINE IWAM \_ con il certificato specificato.

    **winhttpcertcfg -r -c LOCAL \_ MACHINE \\ Root -s MyCertificate -a IWAM \_ TESTMACHINE**

 

 




