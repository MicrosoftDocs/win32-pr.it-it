---
description: Elenco di risorse protette
ms.assetid: 70413c13-3db0-4af0-b584-259cce70f084
title: Elenco di risorse protette
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c221068d9185c289d601f53c6b76df9677d8bc213b44f3dc13dbf5b66a0df446
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119760121"
---
# <a name="protected-resource-list"></a>Elenco di risorse protette

L'autorizzazione per l'accesso completo per modificare le risorse protette da WRP è limitata a TrustedInstaller. Le risorse protette da WRP [](supported-file-replacement-mechanisms.md) possono essere modificate solo usando i meccanismi di sostituzione delle risorse supportati con il Windows del programma di installazione dei moduli.

WRP protegge i file con le estensioni seguenti installate da Windows Server 2008 o Windows Vista: .dll, .exe, OCX e .sys.

WRP protegge i file critici installati da Windows Server 2008 o Windows Vista con le estensioni seguenti: .acm, .ade, .adp, .app, .asa, .asp, .aspx, .ax, .bas, .bat, .bin, .cer, .chm, .clb, .cmd, .cnt, .cnv, .com, .cpl, .cpx, .crt, .csh, .dll, .drv, .dtd, .exe, .fxp, .grp, .h1s, .hlp, .hta, .ime, .inf, .ins, .isp, .its, .js, .jse, .ksh, .lnk, .mad, .maf, .mag, .mam, .man, .maq, .mar, .mas, .mat, .mau, .mav, .maw, .mda, .mdb, .mde, .mdt, .mdw, .mdz, .msc, .msi, .msp, .mst, .mui, .nls, .ocx, .ops, .pal, .pcd, .pif, .prf, .prg, .pst, .reg, .scf, .scr, .sct, .shb, .shs, .sys, .tlb, .tsp, .url, .vb, .vbe, .vbs, .vsmacros, .vss, .vst, .vsw, .ws, .wsc, .wsf, .wsh,  xsd e xsl.

WRP protegge le cartelle critiche. Una cartella contenente solo file protetti da WRP può essere bloccata in modo che solo il Windows di installazione attendibile sia in grado di creare file o sottocartelle nella cartella. Una cartella può essere parzialmente bloccata per consentire agli amministratori di creare file e sottocartelle nella cartella.

WRP protegge le chiavi del Registro di sistema essenziali installate da Windows Server 2008 e Windows Vista. Se una chiave è protetta da WRP, è possibile proteggere tutte le relative sottochiavi e valori.

WRP copia i file necessari per riavviare Windows nella *directory della cache* disponibile in %Windir% \\ winsxs \\ Backup. I file critici che non sono necessari per riavviare Windows non vengono copiati nella directory della cache. Non è possibile modificare le dimensioni della directory della cache e l'elenco di file copiati nella cache.

**Windows Server 2003 e Windows XP: **

Windows Protezione file (WFP) ha preceduto WRP.

WFP protegge i file installati da Windows con le estensioni seguenti: .dll, .exe, ocx e .sys. Sono inoltre protetti i tipi di carattere TrueType Micross.ttf, Tahoma.ttf e Tahomabd.ttf.

Al termine dell'Windows, WFP esegue un'analisi di tutti i file protetti per assicurarsi che non siano stati modificati dalle applicazioni installate tramite l'installazione automatica. Wfp copia anche le versioni verificate di questi file di sistema nella directory della cache. Quando un'applicazione tenta di sostituire un file protetto, WFP può ripristinare il file originale dalla directory della cache.

Il valore predefinito è %systemroot% \\ system32 \\ dllcache. Per specificare un percorso diverso per la cache, creare il valore del Registro di sistema **seguente: HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows NT \_ \\ \\ \\ \\ CurrentVersion \\ Winlogon \\ SFCDllCacheDir**

Deve trattarsi di un percorso locale. L'uso di un percorso di rete crea una singola origine di rete condivisa per i file di cache, purché tutti i client che usano la condivisione esere gli stessi Service Pack e gli stessi hotfix.

Le dimensioni predefinite della cache sono illimitate. Per modificare le dimensioni della cache, usare l'impostazione del Registro di sistema **seguente: HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows NT \_ \\ \\ \\ \\ CurrentVersion \\ Winlogon \\ SFCQuota**

Se il valore è SFC QUOTA ALL FILES, tutti i file di sistema \_ verranno \_ \_ memorizzati nella cache nella directory della cache.

A causa di considerazioni relative allo spazio su disco, potrebbe non essere consigliabile mantenere le versioni memorizzate nella cache di tutti i file di sistema nella directory della cache. A seconda delle dimensioni della cache, WFP archivierà le versioni di file verificate nella directory della cache sul disco rigido del sistema. WFP aggiungerà file alla cache fino a quando le dimensioni della directory della cache non raggiungono il limite specificato.

Quando un'applicazione tenta di sostituire un file protetto non presente nella cache, WFP tenta di ripristinare il file originale dall'origine di installazione, richiedendo all'utente se necessario.

 

 



