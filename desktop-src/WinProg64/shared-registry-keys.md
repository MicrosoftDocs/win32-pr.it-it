---
title: Chiavi del registro di sistema interessate da WOW64
description: In WOW64 alcune chiavi del registro di sistema vengono reindirizzate.
ms.assetid: 7b3f4f11-24bc-44f7-837e-d61d853c7291
keywords:
- chiavi del registro di sistema a 64 bit programmazione Windows
- Programmazione Windows WOW64 a 64 bit, chiavi del registro di sistema
- chiavi del registro di sistema reindirizzate a 64 bit programmazione Windows
- chiavi del registro di sistema riflesse programmazione Windows a 64 bit
- chiavi del registro di sistema condivise a 64 bit programmazione Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48278bfd42656b05d0e1f2be4402496a873022d1
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "106320254"
---
# <a name="registry-keys-affected-by-windows-installations-that-include-windows-on-windows-wow-support-for-multiple-processor-architectures"></a>Chiavi del registro di sistema interessate dalle installazioni di Windows che includono il supporto di Windows su Windows (WOW) per le architetture a più processori

Nelle installazioni di Windows a 64 bit a partire da Windows XP e Windows Server 2003 e nell'architettura di processore ARM a 32 bit per le installazioni di Windows a partire da Windows RT (Windows 8) (in seguito a cui si fa riferimento come **installazioni di Windows interessate**), vengono *reindirizzate* determinate chiavi del registro di sistema.

Nelle installazioni di Windows interessate, quando un processo con un'architettura del processore diversa dall'architettura del processore del sistema operativo (denominato in seguito come **applicazione WOW**) esegue una chiamata del registro di sistema per una chiave reindirizzata, il redirector del registro di sistema intercetta la chiamata e ne esegue il mapping al percorso del registro di sistema fisico corrispondente della chiave. Ad esempio, un'applicazione Intel IA-32 x86 a 32 bit in \[  \] esecuzione in un'installazione di Windows **amd64** /Intel x86-x64 potrebbe essere interessata da una chiave del registro di sistema reindirizzata; quando questa applicazione x86 chiama una chiave reindirizzata, il redirector del registro di sistema intercetta la chiamata dell'applicazione e la reindirizza al percorso del registro di sistema fisico corrispondente della chiave. Per ulteriori informazioni, vedere [redirector del registro di sistema](registry-redirector.md).

Le altre chiavi del registro di sistema sono *condivise* dalle applicazioni con architetture di processori diverse nelle installazioni di Windows interessate. Le chiamate al registro di sistema dell'applicazione WOW alle chiavi condivise non vengono reindirizzate. Viene invece eseguito il mapping di una copia fisica della chiave in ogni visualizzazione logica del registro di sistema.

**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Viene anche *riflesso* un subset di chiavi del registro di sistema reindirizzate in modo da rendere sincronizzate le chiavi e i relativi valori tra le visualizzazioni a 32 bit e a 64 bit del registro di sistema. La reflection del registro di sistema è stata rimossa a partire da Windows 7 e Windows Server 2008 R2. Per altre informazioni, vedere [Reflection del registro di sistema](registry-reflection.md).

Questo argomento elenca le chiavi del registro di sistema reindirizzate, condivise o reindirizzate e riflesse in WOW. Vengono inoltre elencati i collegamenti simbolici che garantiscono la compatibilità per le applicazioni esistenti che possono usare percorsi di chiave del registro di sistema che contengono **Wow6432Node**, il percorso del registro di sistema reindirizzato per i processi x86 eseguiti sulle installazioni di Windows amd64 Per altre informazioni, vedere gli argomenti seguenti:

- [Chiavi reindirizzate, condivise e riflesse in WOW](#redirected-shared-and-reflected-keys-under-wow)
- [Collegamenti simbolici di Windows su Windows 64 (WOW64)](#windows-on-windows-64-wow64-symbolic-links)

## <a name="redirected-shared-and-reflected-keys-under-wow"></a>Chiavi reindirizzate, condivise e riflesse in WOW

Per le applicazioni WOW sulle installazioni di Windows interessate, nella tabella seguente sono elencate le chiavi del registro di sistema reindirizzate, condivise o reindirizzate e riflesse. Le sottochiavi delle chiavi in questa tabella ereditano il comportamento della chiave padre se non diversamente specificato. Se in questa tabella non è presente un elemento padre, la chiave viene condivisa.

| Chiave | Windows Server 2008 R2, Windows 7 e versioni successive | Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP |
|-|-|-|
| **\_computer locale \_ HKEY** | Condiviso | Condiviso |
| **\_MACHINE\SOFTWARE locale \_ HKEY** | Redirected | Redirected |
| **HKEY \_ Classi \_ MACHINE\SOFTWARE locali** \\  | Condiviso | Reindirizzato e riflesso |
| **HKEY \_ Classe \_ MACHINE\SOFTWARE locale** \\  \\ **AppID** | Condiviso | Reindirizzato e riflesso con un'eccezione: i valori del registro di sistema [DllSurrogate](../com/dllsurrogate.md) e [DllSurrogateExecutable]( ../com/dllsurrogateexecutable.md) non vengono riflessi se il relativo valore è una stringa vuota. |
| **HKEY \_ Classi software del \_ computer locale** \\  \\  \\ **CLSID** | Redirected | Reindirizzato e riflesso solo per CLSID che non specificano InprocServer32 o InprocHandler32. |
| **HKEY \_ Classi software del \_ computer locale** \\  \\  \\ **DirectShow** | Redirected | Reindirizzato e riflesso |
| **HKEY \_ Classi software del \_ computer locale** \\  \\  \\ **HPC** | Condiviso | Condiviso |
| **HKEY \_ \_** \\  \\  \\ **Interfaccia** classi software del computer locale | Redirected | Reindirizzato e riflesso |
| **HKEY \_ \_** Tipo di \\  \\ **supporto** classi MACHINE\SOFTWARE locali | Redirected | Reindirizzato e riflesso |
| **HKEY \_ Classi software del \_ computer locale** \\  \\  \\ **MediaFoundation** | Redirected | Reindirizzato e riflesso |
| **HKEY \_ Client software del \_ computer locale** \\  \\  | Condiviso | Redirected |
| **HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **COM3** | Condiviso | Reindirizzato e riflesso |
| **HKEY \_ \_Computer locale** \\ **software** \\ **Microsoft** \\ **Cryptography** \\ **Calais** \\ **Current** | Condiviso | Condiviso |
| **HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **Cryptography** \\ **Calais** \\ **Readers** | Condiviso | Condiviso |
| **HKEY \_ \_Computer locale** \\ **software** \\ **Microsoft** \\ **Cryptography** \\ **Services** | Condiviso | Condiviso |
| **HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **CTF** \\ **SystemShared** | Condiviso | Condiviso |
| **HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **CTF** \\ **Tip** | Condiviso | Condiviso |
| **HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **DFS** | Condiviso | Condiviso |
| **HKEY \_ Firma \_ del** \\  \\  \\ **driver** Microsoft del software del computer locale | Condiviso | Condiviso |
| **HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **EnterpriseCertificates** | Condiviso | Condiviso |
| **HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **EventSystem** | Condiviso | Reindirizzato e riflesso |
| **HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **MSMQ** | Condiviso | Condiviso |
| **HKEY \_ Firma \_ del** \\ **software** \\  \\ **non driver** Microsoft per il computer locale | Condiviso | Condiviso |
| **HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **notepad** \\ **DefaultFonts** | Condiviso | Redirected |
| **HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **OLE** | Condiviso | Reindirizzato e riflesso |
| **HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **RAS** | Condiviso | Condiviso |
| **HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **RPC** | Condiviso | Reindirizzato e riflesso |
| **HKEY \_ Software per \_ computer locale** \\  \\ **Microsoft** \\ **software** Microsoft \\  \\ **Shared Tools** \\ **MSInfo** | Condiviso | Condiviso |
| **HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **SystemCertificates** | Condiviso | Condiviso |
| **HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **TermServLicensing** | Condiviso | Condiviso |
| **HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **TransactionServer** | Condiviso | Condiviso |
| **HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **percorsi delle app** | Condiviso | Redirected |
| **HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** strumenti del \\ **Pannello di controllo** \\ **cursori** \\  | Condiviso | Condiviso |
| **HKEY \_ \_Computer locale** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** \\ **AutoplayHandlers** | Condiviso | Redirected |
| **HKEY \_ \_Computer locale** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** \\ **DriveIcons** | Condiviso | Redirected |
| **HKEY \_ \_Computer locale** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** \\ **KindMap** | Condiviso | Redirected |
| **HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **criteri di gruppo** | Condiviso | Condiviso |
| **HKEY \_ \_Computer locale** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **criteri** | Condiviso | Condiviso |
| **HKEY \_ \_Computer locale** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **PreviewHandlers** | Condiviso | Redirected |
| **HKEY \_ Installazione del software del \_ computer locale** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\  | Condiviso | Condiviso |
| **HKEY \_ \_Computer locale** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ località di **telefonia** \\  | Condiviso | Condiviso |
| **HKEY \_ \_Computer locale** \\ **software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **console**| Condiviso | Redirected |
| **HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **FontDpi** | Condiviso | Condiviso |
| **HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **FontLink** | Condiviso | Redirected |
| **HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **FontMapper** | Condiviso | Condiviso |
| **HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Fonts** | Condiviso | Condiviso |
| **HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **FontSubstitutes** | Condiviso | Condiviso |
| **HKEY \_ \_Computer locale** \\ **software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **GRE \_ Initialize** | Condiviso | Redirected |
| **HKEY \_ SOFTWARE del \_ computer locale** opzioni di \\  \\  \\  \\  \\ **esecuzione file di immagine** Microsoft Windows NT CurrentVersion | Condiviso | Redirected |
| **HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Language Pack** | Condiviso | Redirected |
| **HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **NetworkCards** | Condiviso | Condiviso |
| **HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Perflib** | Condiviso | Condiviso |
| **HKEY \_ \_Macchine locali** \\ **software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **porte** | Condiviso | Condiviso |
| **HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Print** | Condiviso | Condiviso |
| **HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Profiler** | Condiviso | Condiviso |
| **HKEY \_ \_Computer locale** \\ **software** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **fusi orari** | Condiviso | Condiviso |
| **HKEY \_ Criteri software del \_ computer locale** \\  \\  | Condiviso | Condiviso |
| **HKEY \_ RegisteredApplications software del \_ computer locale** \\  \\  | Condiviso | Condiviso **Windows Server 2003 e Windows XP:** Questa chiave è stata aggiunta in Windows Vista. |
| **HKEY \_ \_ utente corrente** | Condiviso | Condiviso |
| **HKEY \_ SOFTWARE \_ utente corrente** \\  | Condiviso | Condiviso |
| **HKEY \_ \_** \\  \\ **Classi** software utente corrente | Condiviso | Reindirizzato e riflesso |
| **HKEY \_ Classi \_ software utente correnti** \\  \\  \\ **AppID** | Condiviso | Reindirizzato e riflesso con un'eccezione: i valori del registro di sistema [DllSurrogate](../com/dllsurrogate.md) e [DllSurrogateExecutable]( ../com/dllsurrogateexecutable.md) non vengono riflessi se il relativo valore è una stringa vuota. |
| **HKEY \_ Classi \_ software utente corrente** \\  \\  \\ **CLSID** | Redirected | Reindirizzato e riflesso |
| **HKEY \_ Classi \_ software utente correnti** \\  \\  \\ **DirectShow** | Redirected | Reindirizzato e riflesso |
| **HKEY \_ \_** \\  \\  \\ **Interfaccia** classi software utente corrente | Redirected | Reindirizzato e riflesso |
| **HKEY \_ \_** Tipo di \\  \\  \\ **supporto** classi software utente corrente | Redirected | Reindirizzato e riflesso |
| **HKEY \_ Classi \_ software utente correnti** \\  \\  \\ **MediaFoundation** | Redirected | Reindirizzato e riflesso |

**HKEY \_ L' \_ utente corrente** è un collegamento simbolico al SID **\_** \\ **\[ \]** degli utenti di HKEY in cui \[ SID \] indica una corrispondenza per l'ID di sicurezza (SID) dell'utente corrente. **HKEY \_ Utenti** \\ **\[ SID \]** \\  \\ **classi** software è un collegamento simbolico alle **\_** \\ **\[ \] \_ classi SID** degli utenti HKEY.

**HKEY \_ La \_ radice delle classi** è una visualizzazione unita delle classi software del **\_ \_ computer locale HKEY** \\  \\  e delle classi software **\_ \_ utente correnti di HKEY** \\  \\ . Le chiavi reindirizzate in questi percorsi del registro di sistema vengono effettivamente reindirizzate anche per **\_ le \_ classi HKEY** . Questo vale anche per le chiavi riflesse nei sistemi che le supportano.

## <a name="windows-on-windows-64-wow64-symbolic-links"></a>Collegamenti simbolici di Windows su Windows 64 (WOW64)

WOW64 definisce i collegamenti simbolici seguenti solo per la compatibilità con le applicazioni esistenti che possono usare percorsi della chiave del registro di sistema hardcoded contenenti Wow6432Node. Le nuove applicazioni devono evitare di usare Wow6432Node nei percorsi delle chiavi del registro di sistema.

- **HKEY \_ Il \_ software del computer locale \\ \\ Wow6432Node \\ classi** è collegato alle **\_ \_ classi software del computer locale HKEY \\ \\ \\ Wow6432Node**
- **HKEY \_ \_Classi software del computer locale \\ \\ \\ Wow6432Node \\ AppID** è collegato **alle \_ \_ classi software del computer locale HKEY \\ \\ \\ AppID**
- **HKEY \_ \_Classi software del computer locale i \\ \\ \\ \\ protocolli Wow6432Node** sono collegati ai **\_ \_ \\ \\ \\ protocolli delle classi software del computer locale HKEY**
- **HKEY \_ \_Classi software del computer locale \\ \\ \\ Wow6432Node \\ typelib** è collegato a **HKEY \_ Local \_ Machine \\ software \\ classi \\ typelib**

**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP: HKEY \_ Il \_ software del computer locale \\ \\ Wow6432Node \\ classi** è collegato alle **\_ \_ classi software del computer locale HKEY \\ \\ \\ Wow6432Node**. In Windows 7 e Windows Server 2008 R2 sono stati aggiunti altri collegamenti simbolici.
