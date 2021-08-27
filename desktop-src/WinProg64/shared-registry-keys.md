---
title: Chiavi del Registro di sistema interessate da WOW64
description: In WOW64 alcune chiavi del Registro di sistema vengono reindirizzate.
ms.assetid: 7b3f4f11-24bc-44f7-837e-d61d853c7291
keywords:
- chiavi del Registro di sistema a 64 bit Windows programmazione
- WOW64 64-bit Windows Programming , chiavi del Registro di sistema
- chiavi del Registro di sistema reindirizzate a 64 bit Windows programmazione
- reflected registry keys 64-bit Windows Programming
- chiavi del Registro di sistema condivise a 64 bit Windows programmazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5193d4aa64848d132aca446c6d1e4a50777614725b69cae637da65aebfe94c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071611"
---
# <a name="registry-keys-affected-by-windows-installations-that-include-windows-on-windows-wow-support-for-multiple-processor-architectures"></a>Chiavi del Registro di sistema interessate Windows installazioni che includono Windows in Windows (WOW) per architetture a più processori

Nelle installazioni di Windows a 64 bit a partire da Windows XP e Windows Server 2003 e nelle installazioni dell'architettura del processore ARM a 32 bit Windows a partire da Windows RT (Windows 8) (successivamente indicato come installazioni **Windows** interessate), alcune chiavi del Registro di sistema vengono *reindirizzate.*

Nelle installazioni Windows interessate, quando un processo con un'architettura del processore diversa dall'architettura del processore del sistema operativo (definita successivamente applicazione **WOW)** effettua una chiamata al Registro di sistema per una chiave reindirizzata, il redirector del Registro di sistema intercetta la chiamata ed esegue il mapping alla posizione del registro fisico corrispondente della chiave. Ad esempio, un'applicazione Intel IA-32 x86 a 32 bit in esecuzione in un'installazione del \[  \] Windows **AMD64/Intel** x86-x64 è interessata da una chiave del Registro di sistema reindirizzata. Quando questa applicazione x86 chiama una chiave reindirizzata, il redirector del Registro di sistema intercetta la chiamata dell'applicazione e la reindirizza al percorso del registro fisico corrispondente della chiave. Per altre informazioni, vedere [Redirector del Registro di sistema.](registry-redirector.md)

Altre chiavi del Registro di *sistema vengono* condivise da applicazioni con architetture del processore diverse nelle installazioni Windows interessate. Le chiamate del Registro di sistema dell'applicazione WOW alle chiavi condivise non vengono reindirizzate. Viene invece eseguito il mapping di una copia fisica della chiave in ogni vista logica del Registro di sistema.

**Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Si riflette anche un subset  di chiavi del Registro di sistema reindirizzate per mantenere le chiavi e i relativi valori sincronizzati tra le visualizzazioni a 32 bit e a 64 bit del Registro di sistema. La reflection del Registro di sistema è stata rimossa a partire da Windows 7 e Windows Server 2008 R2. Per altre informazioni, vedere Reflection [del Registro di sistema.](registry-reflection.md)

Questo argomento elenca le chiavi del Registro di sistema reindirizzate, condivise o reindirizzate e riflesse in WOW. Elenca anche i collegamenti simbolici che forniscono compatibilità per le applicazioni esistenti che possono usare percorsi di chiavi del Registro di sistema hardcoded contenenti **Wow6432Node**, il percorso del Registro di sistema reindirizzato per i processi x86 in esecuzione nelle installazioni di Windows AMD64. Per altre informazioni, vedere gli argomenti seguenti:

- [Chiavi reindirizzate, condivise e riflesse in WOW](#redirected-shared-and-reflected-keys-under-wow)
- [Windows collegamenti simbolici Windows 64 (WOW64)](#windows-on-windows-64-wow64-symbolic-links)

## <a name="redirected-shared-and-reflected-keys-under-wow"></a>Chiavi reindirizzate, condivise e riflesse in WOW

Per le applicazioni WOW nelle installazioni Windows interessate, nella tabella seguente sono elencate le chiavi del Registro di sistema reindirizzate, condivise o reindirizzate e riflesse. Se non diversamente specificato, le sottochiavi delle chiavi in questa tabella ereditano il comportamento della chiave padre. Se in questa tabella non è elencato alcun elemento padre, la chiave viene condivisa.

| Chiave | Windows Server 2008 R2, Windows 7 e versione più recente | Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP |
|-|-|-|
| **HKEY \_ LOCAL \_ MACHINE** | Condiviso | Condiviso |
| **HKEY \_ LOCAL \_ MACHINE\SOFTWARE** | Redirected | Redirected |
| **HKEY \_ Classi \_ LOCAL MACHINE\SOFTWARE** \\  | Condiviso | Reindirizzato e riflesso |
| **HKEY \_ LOCAL \_ MACHINE\SOFTWARE** \\ **Classes** \\ **Appid** | Condiviso | Reindirizzati e riflessi con un'eccezione: i valori [dllSurrogate](../com/dllsurrogate.md) e [DllSurrogateExecutable]( ../com/dllsurrogateexecutable.md) del Registro di sistema non vengono riflessi se il relativo valore è una stringa vuota. |
| **HKEY \_ \_CLSID** classi \\ **SOFTWARE** \\  \\ **LOCAL** MACHINE | Redirected | Reindirizzato e riflesso solo per i CLSID che non specificano InprocServer32 o InprocHandler32. |
| **HKEY \_ Classi \_** SOFTWARE LOCAL MACHINE \\  \\  \\ **DirectShow** | Redirected | Reindirizzato e riflesso |
| **HKEY \_ Local \_ MACHINE** \\ **SOFTWARE** \\ **Classes** \\ **HCP** | Condiviso | Condiviso |
| **HKEY \_ Interfaccia \_ delle classi** \\ **SOFTWARE** \\ **LOCAL** \\  MACHINE | Redirected | Reindirizzato e riflesso |
| **HKEY \_ Local \_ MACHINE\SOFTWARE** \\ **Classes** \\ **Tipo di supporto** | Redirected | Reindirizzato e riflesso |
| **HKEY \_ Classi \_** SOFTWARE LOCAL MACHINE \\  \\  \\ **MediaFoundation** | Redirected | Reindirizzato e riflesso |
| **HKEY \_ CLIENT \_** \\ **SOFTWARE DEL COMPUTER** \\ **LOCALE** | Condiviso | Redirected |
| **HKEY \_ SOFTWARE \_ DEL COMPUTER** \\ **LOCALE** \\ **Microsoft** \\ **COM3** | Condiviso | Reindirizzato e riflesso |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **CryptographyTrais** \\  \\ **Current** | Condiviso | Condiviso |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Lettori di Crittografia** \\  \\ **Microsoft** \\  | Condiviso | Condiviso |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Cryptography** \\ **Services** | Condiviso | Condiviso |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **CTF** \\ **SystemShared** | Condiviso | Condiviso |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **CTF** \\ **TIP** | Condiviso | Condiviso |
| **HKEY \_ SOFTWARE \_ DEL COMPUTER** \\ **LOCALE** \\ **Microsoft** \\ **DFS** | Condiviso | Condiviso |
| **HKEY \_ SOFTWARE \_ DEL COMPUTER** \\ **LOCALE** Firma \\ **del** \\ **driver** Microsoft | Condiviso | Condiviso |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **EnterpriseCertificates** | Condiviso | Condiviso |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **EventSystem** | Condiviso | Reindirizzato e riflesso |
| **HKEY \_ SOFTWARE \_ DEL COMPUTER** \\ **LOCALE** \\ **Microsoft** \\ **MSMQ** | Condiviso | Condiviso |
| **HKEY \_ SOFTWARE \_ DEL COMPUTER** \\ **LOCALE** \\ **Firma microsoft** non \\ **driver** | Condiviso | Condiviso |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Blocco note** \\ **DefaultFonts** | Condiviso | Redirected |
| **HKEY \_ SOFTWARE \_ DEL COMPUTER** \\ **LOCALE** \\ **Microsoft** \\ **OLE** | Condiviso | Reindirizzato e riflesso |
| **HKEY \_ SOFTWARE \_ DEL COMPUTER** \\ **LOCALE** \\ **Microsoft** \\ **RAS** | Condiviso | Condiviso |
| **HKEY \_ SOFTWARE \_ DEL COMPUTER** \\ **LOCALE** \\ **RPC Microsoft** \\  | Condiviso | Reindirizzato e riflesso |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\  \\  \\ **Shared Tools** \\ **MSInfo** | Condiviso | Condiviso |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **SystemCertificates** | Condiviso | Condiviso |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **TermServLicensing** | Condiviso | Condiviso |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **TransactionServer** | Condiviso | Condiviso |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **App Paths** | Condiviso | Redirected |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Pannello di controllo** \\ **cursori** \\  | Condiviso | Condiviso |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** \\ **AutoplayHandlers** | Condiviso | Redirected |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** \\ **DriveIcons** | Condiviso | Redirected |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** \\ **KindMap** | Condiviso | Redirected |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Criteri di gruppo** | Condiviso | Condiviso |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Policies** | Condiviso | Condiviso |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **PreviewHandlers** | Condiviso | Redirected |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Setup** | Condiviso | Condiviso |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** \\ **Località di telefonia CurrentVersion** \\  \\  | Condiviso | Condiviso |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Console**| Condiviso | Redirected |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **FontDpi** | Condiviso | Condiviso |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **FontLink** | Condiviso | Redirected |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **FontMapper** | Condiviso | Condiviso |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE Microsoft** \\ **Windows NT** \\  \\ **CurrentVersion** \\ **Fonts** | Condiviso | Condiviso |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **FontSubstitutes** | Condiviso | Condiviso |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Gre \_ Initialize** | Condiviso | Redirected |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE Microsoft** \\ **Windows NT** \\  \\ opzioni di esecuzione del file di immagine **CurrentVersion** \\  | Condiviso | Redirected |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Language Pack** | Condiviso | Redirected |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **NetworkCards** | Condiviso | Condiviso |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Perflib** | Condiviso | Condiviso |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Ports** | Condiviso | Condiviso |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Print** | Condiviso | Condiviso |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **ProfileList** | Condiviso | Condiviso |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Time Zones** | Condiviso | Condiviso |
| **HKEY \_ Criteri \_** \\ **SOFTWARE DEL COMPUTER** \\ **LOCALE** | Condiviso | Condiviso |
| **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **RegisteredApplications** | Condiviso | Condiviso; **Windows Server 2003 e Windows XP:** Questa chiave è stata aggiunta in Windows Vista. |
| **HKEY \_ CURRENT \_ USER** | Condiviso | Condiviso |
| **HKEY \_ SOFTWARE \_ UTENTE** \\ **CORRENTE** | Condiviso | Condiviso |
| **HKEY \_ Classi \_** \\ **SOFTWARE** \\  CURRENT USER | Condiviso | Reindirizzato e riflesso |
| **HKEY \_ CURRENT \_ USER** \\ **SOFTWARE** \\ **Classes** \\ **Appid** | Condiviso | Reindirizzati e riflessi con un'eccezione: i valori [dllSurrogate](../com/dllsurrogate.md) e [DllSurrogateExecutable]( ../com/dllsurrogateexecutable.md) del Registro di sistema non vengono riflessi se il relativo valore è una stringa vuota. |
| **HKEY \_ CURRENT \_ USER** \\ **SOFTWARE** \\ **Classes** \\ **CLSID** | Redirected | Reindirizzato e riflesso |
| **HKEY \_ Classi SOFTWARE CURRENT \_ USER** \\  \\  \\ **DirectShow** | Redirected | Reindirizzato e riflesso |
| **HKEY \_ Interfaccia \_ delle classi** \\ **SOFTWARE** \\  \\  CURRENT USER | Redirected | Reindirizzato e riflesso |
| **HKEY \_ Current \_ USER** \\ **SOFTWARE** \\ **Classes** \\ **Media Type** | Redirected | Reindirizzato e riflesso |
| **HKEY \_ Classi \_** SOFTWARE CURRENT USER \\  \\  \\ **MediaFoundation** | Redirected | Reindirizzato e riflesso |

**HKEY \_ CURRENT \_ USER** è un collegamento simbolico al SID **\_** \\ **\[ \]** di HKEY USERS in cui SID indica una corrispondenza per l'ID di sicurezza \[ \] (SID) dell'utente corrente. **HKEY \_ USERS** \\ **\[ SID \]** \\ **SOFTWARE** \\ **Classes è** un collegamento simbolico alle classi **\_ SID HKEY USERS** \\ **\[ \] \_**.

**HKEY \_ CLASSES \_ ROOT** è una visualizzazione unita delle classi SOFTWARE **HKEY LOCAL \_ \_ MACHINE** \\  \\  e **HKEY \_ CURRENT \_ USER** \\ **SOFTWARE** \\ **Classes**. Le chiavi reindirizzate in questi percorsi del Registro di sistema vengono reindirizzate in modo efficace **anche per HKEY \_ CLASSES \_ ROOT.** Questo vale anche per le chiavi riflesse nei sistemi che le supportano.

## <a name="windows-on-windows-64-wow64-symbolic-links"></a>Windows collegamenti simbolici Windows 64 (WOW64)

WOW64 definisce i collegamenti simbolici seguenti solo per la compatibilità con le applicazioni esistenti che possono usare percorsi di chiavi del Registro di sistema hardcoded contenenti Wow6432Node. Le nuove applicazioni devono evitare l'uso di Wow6432Node nei percorsi delle chiavi del Registro di sistema.

- **HKEY \_ Local \_ MACHINE \\ SOFTWARE \\ Wow6432Node \\ Classes is** linked to **HKEY LOCAL MACHINE SOFTWARE \_ Classes \_ \\ \\ \\ Wow6432Node**
- **HKEY \_ Local \_ MACHINE SOFTWARE Classes \\ \\ \\ Wow6432Node \\ AppId** is linked to **HKEY LOCAL MACHINE SOFTWARE Classes \_ \_ \\ \\ \\ AppId**
- **HKEY \_ Local \_ MACHINE SOFTWARE Classes \\ \\ \\ Wow6432Node \\ PROTOCOLS è** collegato a **HKEY LOCAL MACHINE SOFTWARE \_ Classes \_ \\ \\ \\ PROTOCOLS**
- **HKEY \_ Local \_ MACHINE SOFTWARE Classes \\ \\ \\ Wow6432Node \\ Typelib** è collegato a **HKEY LOCAL MACHINE SOFTWARE Classes \_ \_ \\ \\ \\ Typelib**

**Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP: HKEY \_ Local \_ MACHINE \\ SOFTWARE \\ Wow6432Node \\ Classes is** linked to **HKEY LOCAL MACHINE SOFTWARE \_ Classes \_ \\ \\ \\ Wow6432Node**. Altri collegamenti simbolici sono stati aggiunti in Windows 7 e Windows Server 2008 R2.
