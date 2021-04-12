---
description: Elenco delle risorse protette
ms.assetid: 70413c13-3db0-4af0-b584-259cce70f084
title: Elenco delle risorse protette
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 316a9bf9233283a7c0aba11f0d5fe8a09f38f1e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233824"
---
# <a name="protected-resource-list"></a>Elenco delle risorse protette

L'autorizzazione per l'accesso completo per modificare le risorse protette con WRP è limitata a TrustedInstaller. È possibile modificare le risorse protette con WRP solo usando i [meccanismi di sostituzione delle risorse supportati](supported-file-replacement-mechanisms.md) con il servizio moduli di installazione di Windows.

WRP protegge i file con le seguenti estensioni installate da Windows Server 2008 o Windows Vista:. dll,. exe,. ocx e. sys.

WRP protegge i file critici installati da Windows Server 2008 o Windows Vista con le estensioni seguenti:. ACM,. Ade,. adp,. app,. asa,. asp,. aspx,. ax,. Bas,. bat,. bin,. cer,. chm,. CLB,. cmd,. cnt,. cnv,. com,. cpl,. CPX,. CRT,. csh,. dll,. drv,. DTD,. exe,. fxp,. GRP,. H1S,. hlp,. HTA,.,. inf,. ins,. ISP,. its,. js,. jse,. ksh,. lnk,. Mad,. maf,. mag , Mam,. Man,. maq,. Mar,. Mas,. mat,. Mau,. MAV,. Maw,. MDA,. mdb,. mde,. MDT,. mdw,. mdz,. msc,. msi,. msp,. MST,. mui,. NLS,. ocx,. ops,. PAL,. PCD,. PIF,. prf,. prg,. pst,. reg,. SCF,. SCR,. SCT,. SHB,. SHS,. sys,. tlb,. tsp,. URL,. vb,. vbe,. vbs,. vsmacros,. VSS,. VST,. vsw,. ws,. WSC,. wsf,. WSH,. xsd e. Xsl.

WRP protegge le cartelle critiche. Una cartella contenente solo file protetti da WRP può essere bloccata in modo che solo il programma di installazione attendibile di Windows sia in grado di creare file o sottocartelle nella cartella. Una cartella può essere bloccata parzialmente per consentire agli amministratori di creare file e sottocartelle nella cartella.

WRP protegge le chiavi del registro di sistema essenziali installate da Windows Server 2008 e Windows Vista. Se una chiave è protetta da WRP, è possibile proteggere tutte le sottochiavi e i valori.

WRP copia i file necessari per riavviare Windows nella directory della *cache* che si trova in% windir% \\ WinSxS \\ backup. I file critici non necessari per riavviare Windows non vengono copiati nella directory della cache. Non è possibile modificare la dimensione della directory della cache e l'elenco dei file copiati nella cache.

* * Windows Server 2003 e Windows XP: * *

Protezione file di Windows (WFP) preceduta da WRP.

Pam protegge i file installati da Windows con le estensioni seguenti:. dll,. exe,. ocx e. sys. Inoltre, i tipi di carattere TrueType MICROS. ttf, Tahoma. ttf e TahomaBD. ttf sono protetti.

Al termine dell'installazione di Windows, PAM esegue un'analisi di tutti i file protetti per assicurarsi che non siano stati modificati dalle applicazioni installate tramite installazione automatica. Pam copia inoltre le versioni verificate di questi file di sistema nella directory della cache. Quando un'applicazione tenta di sostituire un file protetto, PAM può ripristinare il file originale dalla directory della cache.

Il valore predefinito è% SystemRoot% \\ system32 \\ dllcache. Per specificare un percorso diverso per la cache, creare il valore del registro di sistema seguente: **HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon \\ SFCDllCacheDir**

Deve trattarsi di un percorso locale. L'utilizzo di un percorso di rete crea un'unica origine di rete condivisa per i file di cache, purché tutti i client che utilizzano la condivisione eseguano gli stessi Service Pack e gli stessi hotfix.

Le dimensioni predefinite della cache sono illimitate. Per modificare le dimensioni della cache, usare l'impostazione del registro di sistema seguente: **HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon \\ SFCQuota**

Se il valore è SFC \_ quota \_ tutti \_ i file, tutti i file di sistema verranno memorizzati nella cache nella directory della cache.

A causa di considerazioni sullo spazio su disco, potrebbe non essere consigliabile mantenere le versioni memorizzate nella cache di tutti i file di sistema nella directory della cache. A seconda delle dimensioni della cache, Pam archivia le versioni dei file verificate nella directory della cache sul disco rigido del sistema. Pam aggiungerà i file alla cache fino a quando le dimensioni della directory della cache non raggiungono il limite specificato.

Quando un'applicazione tenta di sostituire un file protetto che non si trova nella cache, WFP tenta di ripristinare il file originale dall'origine dell'installazione, se necessario.

 

 



