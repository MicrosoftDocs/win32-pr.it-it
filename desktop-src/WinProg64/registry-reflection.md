---
title: Reflection del registro di sistema
description: Il redirector del registro di sistema isola le applicazioni a 32 bit e a 64 bit fornendo viste logiche separate di determinate parti del registro di sistema in WOW64. Tuttavia, i valori di alcune chiavi del registro di sistema devono essere gli stessi nelle viste a 32 bit e a 64 bit.
ms.assetid: eac9038b-9f59-4ac7-8974-f94a4a62a257
keywords:
- Reflection del registro di sistema a 64 bit programmazione Windows
- Programmazione Windows Reflection a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 523041004d9570bbdf101050e30f5d9139031913
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300058"
---
# <a name="registry-reflection"></a>Reflection del registro di sistema

\[Le informazioni contenute in questo argomento si applicano a Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP. A partire da Windows 7 e Windows Server 2008 R2, WOW64 non usa più la reflection del registro di sistema e le chiavi precedentemente riflesse sono invece condivise. Per altre informazioni, vedere [chiavi del registro di sistema interessate da WOW64](shared-registry-keys.md).\]

Il [redirector del registro di sistema](registry-redirector.md) isola le applicazioni a 32 bit e a 64 bit fornendo viste logiche separate di determinate parti del registro di sistema in WOW64. Tuttavia, i valori di alcune chiavi del registro di sistema devono essere gli stessi nelle viste a 32 bit e a 64 bit.

Il processo di *Reflection del registro* di sistema copia le chiavi e i valori del registro di sistema tra due visualizzazioni del registro per mantenerle Sincronizza Ogni visualizzazione dispone di una copia fisica separata di ogni chiave del registro di sistema riflessa, una per la visualizzazione del registro di sistema a 32 bit e l'altra per la visualizzazione del registro di sistema a 64 bit.

Una chiave riflessa viene copiata quando una chiave viene chiusa chiamando [**RegCloseKey**](/windows/desktop/api/winreg/nf-winreg-regclosekey). Si noti che questa operazione consente di generare un possibile race condition: se più processi modificano la chiave riflessa, l'ultima chiamata **RegCloseKey** determina il valore finale della chiave.

Il riflettore copia i dati di attivazione COM per i server locali tra le visualizzazioni, ma non copia i dati in-process perché la combinazione di 32/64 di dati in-process non è consentita in Windows a 64 bit.

La reflection non è abilitata per chiavi del registro di sistema condivise o per chiavi del registro di sistema non reindirizzate. Ad esempio, la reflection non è abilitata per la chiave di **\_ \_ \\ sistema del computer locale HKEY** . Per un elenco delle chiavi del registro di sistema reindirizzate, condivise o riflesse, vedere le [chiavi del registro di sistema interessate da WOW64](shared-registry-keys.md).

La reflection del registro di sistema usa un criterio "ultimo writer wins", come illustrato nell'esempio seguente:

-   Dopo un'installazione pulita di Windows a 64 bit, viene registrato Wordpad.exe a 64 bit per gestire i file con estensione doc. Il riflettore copia la registrazione. doc dalla vista del registro di sistema a 64 bit nella visualizzazione del registro di sistema a 32 bit.
-   Un amministratore installa Office a 32 bit, che registra Winword.exe a 32 bit per gestire i file con estensione doc nella visualizzazione del registro di sistema a 32 bit. Il riflettore del registro di sistema copia queste informazioni nella visualizzazione del registro di sistema a 64 bit, pertanto le applicazioni a 32 bit e 64 bit avviano la versione a 32 bit di Winword.exe per i file con estensione doc.
-   Un amministratore installa Office a 64 bit, che registra Winword.exe a 64 bit per gestire i file con estensione doc nella visualizzazione del registro di sistema a 64 bit. Il riflettore del registro di sistema copia queste informazioni nel registro di sistema a 32 bit, pertanto le applicazioni a 32 bit e 64 bit avviano la versione a 64 bit di Winword.exe per i file con estensione doc.

Pertanto, le informazioni sull'associazione di file vengono conservate per l'applicazione installata più di recente.

Può essere utile per le applicazioni a 32 bit e a 64 bit per condividere valori di chiave del registro di sistema specifici che in genere vengono scritti in visualizzazioni del registro di sistema separate. Ad esempio, un server OLE a 32 bit che può gestire le richieste da client sia a 32 bit che a 64 bit potrebbe rendere disponibili i dati del registro di sistema a 32 bit per la visualizzazione a 64 bit del registro di sistema.

Quando un componente scrive i dati nel registro di sistema, WOW64 analizza le informazioni ed esegue una copia dei dati nella visualizzazione alternativa del registro di sistema quando appropriato. In genere, questo processo mantiene due copie fisiche separate delle stesse chiavi del registro di sistema in entrambe le visualizzazioni del registro di sistema e viene chiamata Reflection del registro di sistema o mirroring del registro di sistema.

La maggior parte delle chiavi sotto la radice delle classi si trova in questa categoria. Gli aggiornamenti alle chiavi vengono riflessi quando l'aggiornamento viene completato e l'handle per la chiave si chiude. In casi specifici, le Scritture in una chiave non vengono riflesse se la chiave ha una dipendenza bit. Ad esempio, la chiave InprocServer32 a 32 bit non è pertinente per le applicazioni a 64 bit, quindi la chiave InprocServer32 non viene riflessa nella visualizzazione del registro di sistema a 64 bit. Tuttavia, le applicazioni a 64 bit possono utilizzare la chiave LocalServer32 a 32 bit e viene riflessa la chiave LocalServer32.

Per **\_ \_ \\ \\ le classi \\ software del computer locale HKEY CLSID** e **HKEY \_ \_ \\ classi software utente correnti \\ \\ CLSID**, vengono riflessi solo i CLSID che non specificano InprocServer32 o InprocHandler32. Solo i CLSID LocalServer32 vengono riflessi perché sono in esecuzione out-of-process e possono essere attivati da applicazioni 32 o 64 bit. I CLSID InProcServer32 non vengono riflessi perché non è possibile caricare una DLL a 32 bit per l'esecuzione in un processo a 64 bit o una DLL a 64 bit per l'esecuzione in un processo a 32 bit.

Per le classi **\_ software del computer locale HKEY \_ \\ \\ \\ AppID** e **HKEY le \_ \_ \\ classi software utente correnti \\ \\ AppID**, i valori del registro di sistema [DllSurrogate](../com/dllsurrogate.md) e [DllSurrogateExecutable]( ../com/dllsurrogateexecutable.md) non vengono riflessi se il relativo valore è una stringa vuota.

Per disabilitare e abilitare la reflection del registro di sistema per una particolare chiave riflessa, usare le funzioni [**RegDisableReflectionKey**](/windows/desktop/api/winreg/nf-winreg-regdisablereflectionkey) e [**RegEnableReflectionKey**](/windows/desktop/api/winreg/nf-winreg-regenablereflectionkey) . Queste funzioni non influiscono sulle chiavi che non sono presenti nell'elenco di chiavi riflesse più indietro in questo argomento. Le applicazioni devono disabilitare la reflection solo per le chiavi del registro di sistema create e non tentare di disabilitare la reflection per le chiavi predefinite, ad esempio il **\_ \_ computer locale HKEY** o l' **\_ \_ utente corrente di HKEY**. Per determinare se le chiavi nell'elenco Reflection sono state disabilitate, utilizzare la funzione [**RegQueryReflectionKey**](/windows/desktop/api/winreg/nf-winreg-regqueryreflectionkey) .

Le chiavi riflesse non devono essere utilizzate nelle operazioni del registro di sistema transazionali. La scrittura di chiavi riflesse durante una transazione può causare l'esito negativo della transazione. Per ulteriori informazioni sulle transazioni, vedere [gestione transazioni kernel](/windows/desktop/Ktm/kernel-transaction-manager-portal).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Redirector del registro di sistema](registry-redirector.md)
</dt> <dt>

[Reflection del registro di sistema in Windows](/windows-hardware/drivers/display/microsoft-windows-vista-display-driver-64-bit-issues)
</dt> <dt>

[Chiavi del registro di sistema interessate da WOW64](shared-registry-keys.md)
</dt> </dl>

 

 