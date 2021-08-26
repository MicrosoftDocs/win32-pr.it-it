---
description: Lo strumento di configurazione dei certificati Microsoft Windows HTTP Services (WinHTTP), &\# 0034;WinHttpCertCfg.exe&0034;, consente agli amministratori di installare e configurare i certificati client in qualsiasi archivio certificati accessibile \# dall'account IWAM (Internet Server Web Application Manager). Lo strumento elimina anche la necessità di eseguire qualsiasi operazione speciale per gli account, ad esempio l'account IWAM, per ottenere l'accesso ai certificati quando si usa asp (Active Server Pages).
ms.assetid: e4c2afc2-0fd3-4bdd-812e-f112958e1576
title: WinHttpCertCfg.exe, uno strumento di configurazione del certificato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21b8fbfadd6cf0282f63b26c8dd40d5ef96b5f54
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466428"
---
# <a name="winhttpcertcfgexe-a-certificate-configuration-tool"></a>WinHttpCertCfg.exe, uno strumento di configurazione del certificato

Lo strumento di configurazione dei certificati Microsoft [Windows HTTP Services (WinHTTP),](about-winhttp.md) "WinHttpCertCfg.exe", consente agli [](glossary.md) amministratori di installare e configurare i certificati client in qualsiasi archivio certificati accessibile dall'account IWAM (Web Application Manager) del server Internet. Lo strumento elimina anche la necessità di eseguire qualsiasi operazione speciale per gli account, ad esempio l'account IWAM, per ottenere l'accesso ai certificati quando si usa asp (Active Server Pages).

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




| Parametro | Descrizione | 
|-----------|-------------|
| -? | Visualizza i dati della sintassi. | 
| -i | Specifica che il certificato deve essere importato da un file PFX (Personal Information Exchange). Questo parametro deve essere seguito dal nome del file. Quando si specifica questo parametro, è necessario specificare anche "-a" e "-c". | 
| -g | Specifica che l'accesso viene concesso a una chiave privata. Quando si specifica questo parametro, è necessario specificare anche "-a", "-c" e "-s". | 
| -r | Specifica che l'accesso viene rimosso per una chiave privata. Quando si specifica questo parametro, è necessario specificare anche "-a", "-c" e "-s". | 
| -l | Specifica che vengono elencati gli account con accesso a una chiave privata. Quando si specifica questo parametro, è necessario specificare anche "-c" e "-s". | 
| -a | Specifica l'account utente nel computer da configurare. Può trattarsi di un computer locale o di un account di dominio, ad esempio "IWAM_TESTMACHINE", "TESTUSER" o "TESTDOMAIN\DOMAINUSER". | 
| -c | Specifica il percorso e il nome <a href="glossary.md"><em>dell'archivio certificati</em></a>. Usare "LOCAL_MACHINE" o "CURRENT_USER" per designare il ramo del Registro di sistema da usare per il percorso. <em>L'archivio</em> certificati può essere qualsiasi installato nel computer. Esempi di nomi tipici sono "MY", "Root" e "TrustedPeople". Il percorso e il nome <em>dell'archivio</em> certificati sono separati da una barra rovesciata, ad esempio "LOCAL_MACHINE\Root".<blockquote>[!Note]<br />Anche se il ramo "CURRENT_USER" del Registro di sistema può essere specificato con questo parametro, l'estensione dell'accesso alle chiavi private è destinata principalmente ai certificati installati in un archivio certificati del <a href="glossary.md"><em>computer</em></a> locale a cui possono accedere più utenti.</blockquote><br /> | 
| -S | Specifica una stringa di ricerca senza distinzione tra maiuscole e minuscole per trovare il primo certificato enumerato con un nome soggetto che contiene questa sottostringa. | 
| -p | Specifica una password utilizzata per importare il certificato e la chiave privata. Viene usato solo con l'opzione import. | 




 

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

 

 




