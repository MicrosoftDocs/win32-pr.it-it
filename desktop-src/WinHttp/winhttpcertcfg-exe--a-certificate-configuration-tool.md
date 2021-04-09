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
# <a name="winhttpcertcfgexe-a-certificate-configuration-tool"></a>WinHttpCertCfg.exe, uno strumento di configurazione del certificato

Lo strumento di configurazione del certificato [Microsoft Windows HTTP Services (WinHTTP)](about-winhttp.md) , "WinHttpCertCfg.exe", consente agli amministratori di installare e configurare i certificati client in qualsiasi [*archivio certificati*](glossary.md) a cui è possibile accedere tramite l'account di gestione applicazioni Web (IWAM) di Internet Server. Lo strumento Elimina inoltre la necessità di eseguire operazioni speciali per gli account, ad esempio l'account IWAM, per ottenere l'accesso ai certificati quando si utilizza Active Server Pages (ASP).

Microsoft Management Console (MMC) consente agli amministratori di importare i certificati client in un computer locale. Tuttavia, l'importazione di un certificato non concede automaticamente l'accesso alla chiave privata per gli altri account. Questa chiave privata è obbligatoria per l'autenticazione del certificato client. Lo strumento di configurazione dei certificati Microsoft Windows HTTP Services (WinHTTP) offre la possibilità di concedere l'accesso ad altri account, ad esempio l'account IWAM, quando necessario.

-   [Utilizzo dello strumento di configurazione dei certificati](#using-the-certificate-configuration-tool)
-   [esempi](#examples)

## <a name="using-the-certificate-configuration-tool"></a>Utilizzo dello strumento di configurazione dei certificati

Lo strumento di configurazione dei certificati WinHTTP, WinHttpCertCfg.exe, è disponibile come download nel sito Web [Windows Server 2003 Resource Kit Tools](https://www.microsoft.com/downloads/details.aspx?familyid=9d467a69-57ff-4ae7-96ee-b18c4790cffd) . Il codice di esempio seguente mostra i parametri della riga di comando validi da usare con questo strumento.

``` syntax
winhttpcertcfg [-?]
 
winhttpcertcfg [-i PFXFile | -g | -r | -l]
               [-a Account] [-c CertStore] 
               [-s SubjectStr] [-p PFXPassword]
```

Nella tabella seguente sono elencati i parametri per lo strumento di configurazione di.



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
<td>Visualizza i dati di sintassi.</td>
</tr>
<tr class="even">
<td>-i</td>
<td>Specifica che il certificato deve essere importato da un file PFX (Personal Information Exchange). Questo parametro deve essere seguito dal nome del file. Quando si specifica questo parametro, è &quot; &quot; necessario specificare anche-a e &quot; -c &quot; .</td>
</tr>
<tr class="odd">
<td>-g</td>
<td>Specifica che l'accesso viene concesso a una chiave privata. Quando si specifica questo parametro, è &quot; &quot; &quot; necessario specificare anche-a,-c &quot; e &quot; -s &quot; .</td>
</tr>
<tr class="even">
<td>-r</td>
<td>Specifica che l'accesso viene rimosso per una chiave privata. Quando si specifica questo parametro, è &quot; &quot; &quot; necessario specificare anche-a,-c &quot; e &quot; -s &quot; .</td>
</tr>
<tr class="odd">
<td>-l</td>
<td>Specifica che sono elencati gli account con accesso a una chiave privata. Quando si specifica questo parametro, è &quot; &quot; necessario specificare anche-c e &quot; -s &quot; .</td>
</tr>
<tr class="even">
<td>-a</td>
<td>Specifica l'account utente nel computer che si sta configurando. Potrebbe trattarsi di un computer locale o di un account di dominio, ad esempio &quot; IWAM_TESTMACHINE &quot; , &quot; TESTUSER &quot; o &quot; TESTDOMAIN\DOMAINUSER &quot; .</td>
</tr>
<tr class="odd">
<td>-c</td>
<td>Specifica il percorso e il nome dell' <a href="glossary.md"><em>archivio certificati</em></a>. Utilizzare &quot; LOCAL_MACHINE &quot; o &quot; CURRENT_USER &quot; per definire il ramo del registro di sistema da utilizzare per la posizione. L' <em>archivio certificati</em> può essere installato nel computer. Esempi di nomi tipici sono &quot; My &quot; , &quot; root &quot; e &quot; TrustedPeople &quot; . Il percorso e il nome dell' <em>archivio certificati</em> sono separati da una barra rovesciata, ad esempio &quot; LOCAL_MACHINE \Directory principale &quot; .
<blockquote>
[!Note]<br />
Sebbene &quot; &quot; sia possibile specificare il ramo CURRENT_USER del registro di sistema con questo parametro, l'estensione dell'accesso alle chiavi private è destinata principalmente ai certificati installati in un <a href="glossary.md"><em>archivio certificati</em></a> del computer locale a cui possono accedere più utenti.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>-S</td>
<td>Specifica una stringa di ricerca senza distinzione tra maiuscole e minuscole per trovare il primo certificato enumerato con un nome soggetto che contiene la sottostringa.</td>
</tr>
<tr class="odd">
<td>-p</td>
<td>Specifica una password utilizzata per importare il certificato e la chiave privata. Viene utilizzato solo con l'opzione Import.</td>
</tr>
</tbody>
</table>



 

> [!NOTE]
> L'utente deve disporre di privilegi sufficienti per usare questo strumento, che richiede che l'utente sia un amministratore e lo stesso utente che ha installato il certificato client, se installato.
>
> Lo strumento "WinHttpCertCfg.exe" non è utile per configurare i certificati archiviati in un file system, ad esempio FAT32, che non supporta gli elenchi di controllo di accesso (ACL).

## <a name="examples"></a>Esempio

Negli esempi seguenti vengono illustrati alcuni dei modi in cui è possibile utilizzare lo strumento di configurazione.

1.  Questo comando elenca gli account che hanno accesso alla chiave privata per il certificato "certificato" nell' [*archivio certificati*](glossary.md) "radice" del ramo del computer locale \_ del registro di sistema.

    **Winhttpcertcfg-l-c \_ computer locale \\ radice-s certificato**

2.  Questo comando concede l'accesso alla chiave privata del certificato "certificato" nell' [*archivio certificati*](glossary.md) "My" per l'account TESTUSER.

    **Winhttpcertcfg-g-c \_ computer locale \\ My-s certificato-a TESTUSER**

3.  Questo comando importa un certificato e una chiave privata da un file PFX e estende l'accesso alla chiave privata a un altro account.

    **Winhttpcertcfg-i FilePFX-c LOCAL \_ computer \\ My-a IWAM \_ TESTMACHINE-p PFXPassword**

4.  Questo comando Nega l'accesso alla chiave privata per l'account IWAM \_ TESTMACHINE con il certificato specificato.

    **Winhttpcertcfg-r-c \_ computer locale \\ radice-s certificato-a IWAM \_ TESTMACHINE**

 

 




