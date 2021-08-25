---
title: Reflection del Registro di sistema
description: Il redirector del Registro di sistema isola le applicazioni a 32 bit e a 64 bit fornendo visualizzazioni logiche separate di determinate parti del Registro di sistema in WOW64. Tuttavia, i valori di alcune chiavi del Registro di sistema devono essere gli stessi nelle viste a 32 bit e a 64 bit.
ms.assetid: eac9038b-9f59-4ac7-8974-f94a4a62a257
keywords:
- reflection del Registro di sistema programmazione Windows a 64 bit
- Reflection 64-bit Windows Programmazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9104ba6bf4d537a597a2a45bfd9034379ed1781dd893e23633c08e9e9c1149b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899041"
---
# <a name="registry-reflection"></a>Reflection del Registro di sistema

\[Le informazioni contenute in questo argomento si applicano a Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP. A partire da Windows 7 e Windows Server 2008 R2, WOW64 non usa più la reflection del Registro di sistema e le chiavi precedentemente riflesse vengono invece condivise. Per altre informazioni, vedere [Chiavi del Registro di sistema interessate da WOW64.](shared-registry-keys.md)\]

Il [redirector del](registry-redirector.md) Registro di sistema isola le applicazioni a 32 bit e a 64 bit fornendo visualizzazioni logiche separate di determinate parti del Registro di sistema in WOW64. Tuttavia, i valori di alcune chiavi del Registro di sistema devono essere gli stessi nelle viste a 32 bit e a 64 bit.

Il processo di *reflection del Registro di sistema* copia le chiavi e i valori del Registro di sistema tra due viste del Registro di sistema per mantenerle sincronizzate. Ogni vista ha una copia fisica separata di ogni chiave del Registro di sistema riflessa, una per la visualizzazione del Registro di sistema a 32 bit e l'altra per la visualizzazione del Registro di sistema a 64 bit.

Una chiave riflessa viene copiata quando una chiave viene chiusa chiamando [**RegCloseKey.**](/windows/desktop/api/winreg/nf-winreg-regclosekey) Si noti che ciò dà origine a una possibile race condition: se più processi modificano la chiave riflessa, l'ultima chiamata **RegCloseKey** determina il valore finale della chiave.

Il reflector copia i dati di attivazione COM per i server locali tra le visualizzazioni, ma non copia i dati in-process perché la combinazione di dati in-process 32/64 non è consentita in un Windows a 64 bit.

La reflection non è abilitata per le chiavi del Registro di sistema condivise o per le chiavi del Registro di sistema non reindirizzate. Ad esempio, la reflection non è abilitata per la **chiave di sistema \_ HKEY LOCAL \_ MACHINE. \\** Per un elenco delle chiavi del Registro di sistema reindirizzate, condivise o riflesse, vedere Chiavi del Registro di sistema [interessate da WOW64.](shared-registry-keys.md)

La reflection del Registro di sistema usa un criterio "last writer wins" come illustrato nell'esempio seguente:

-   Dopo un'installazione pulita di file Windows a 64 bit, i file Wordpad.exe a 64 bit vengono registrati per gestire .doc file. Il reflector copia la registrazione .doc dalla visualizzazione del Registro di sistema a 64 bit nella visualizzazione del Registro di sistema a 32 bit.
-   Un amministratore installa un Office a 32 bit, che registra Winword.exe a 32 bit per gestire i file .doc nella visualizzazione del Registro di sistema a 32 bit. Il riflettore del Registro di sistema copia queste informazioni nella visualizzazione del Registro di sistema a 64 bit, quindi sia le applicazioni a 32 bit che a 64 bit avviano la versione a 32 bit di Winword.exe per i file .doc.
-   Un amministratore installa un Office a 64 bit, che registra Winword.exe a 64 bit per gestire i file .doc nella visualizzazione del Registro di sistema a 64 bit. Il reflector del Registro di sistema copia queste informazioni nel Registro di sistema a 32 bit, quindi le applicazioni a 32 bit e a 64 bit avviano la versione a 64 bit di Winword.exe per i file .doc.

Di conseguenza, le informazioni sull'associazione di file vengono mantenute per l'applicazione installata più di recente.

Può essere utile per le applicazioni a 32 bit e a 64 bit condividere valori di chiave del Registro di sistema specifici che vengono normalmente scritti in visualizzazioni separate del Registro di sistema. Ad esempio, un server OLE a 32 bit in grado di gestire le richieste da client a 32 bit e a 64 bit potrebbe rendere disponibili i dati del Registro di sistema a 32 bit per la visualizzazione a 64 bit del Registro di sistema.

Quando un componente scrive dati nel Registro di sistema, WOW64 analizza le informazioni e crea una copia dei dati nella visualizzazione alternativa del Registro di sistema, se appropriato. In genere, questo processo mantiene due copie fisiche separate delle stesse chiavi del Registro di sistema in entrambe le viste del Registro di sistema e viene chiamato reflection del Registro di sistema o mirroring del Registro di sistema.

La maggior parte delle chiavi nella radice delle classi è in questa categoria. Gli aggiornamenti delle chiavi si riflettono quando l'aggiornamento viene completato e l'handle per la chiave si chiude. In casi specifici, le scritture in una chiave non vengono riflesse se la chiave presenta una dipendenza dal numero di bit. Ad esempio, la chiave InprocServer32 a 32 bit non è rilevante per le applicazioni a 64 bit, quindi la chiave InprocServer32 non viene riflessa nella visualizzazione del Registro di sistema a 64 bit. Tuttavia, le applicazioni a 64 bit possono usare la chiave LocalServer32 a 32 bit e la chiave LocalServer32 viene riflessa.

Per le classi software **\_ HKEY LOCAL \_ MACHINE \\ \\ \\ CLSID** e HKEY CURRENT USER Classi software CLSID , vengono riflessi solo i **\_ \_ \\ \\ \\ CLSID** che non specificano InprocServer32 o InprocHandler32. Vengono riflessi solo i CLSID LocalServer32 perché vengono eseguiti out-of-process e possono essere attivati da applicazioni a 32 o a 64 bit. I CLSID InProcServer32 non vengono riflessi perché non è possibile caricare una DLL a 32 bit per l'esecuzione in un processo a 64 bit o una DLL a 64 bit per l'esecuzione in un processo a 32 bit.

Per le classi software **HKEY \_ LOCAL MACHINE \_ \\ \\ \\ Appid** e **HKEY CURRENT USER \_ \_ \\ \\ \\ Appid**, i valori [dllSurrogate](../com/dllsurrogate.md) e [DllSurrogateExecutable]( ../com/dllsurrogateexecutable.md) del Registro di sistema non vengono riflessi se il relativo valore è una stringa vuota.

Per disabilitare e abilitare la reflection del Registro di sistema per una chiave riflessa specifica, usare le funzioni [**RegDisableReflectionKey**](/windows/desktop/api/winreg/nf-winreg-regdisablereflectionkey) e [**RegEnableReflectionKey.**](/windows/desktop/api/winreg/nf-winreg-regenablereflectionkey) Queste funzioni non influiscono sulle chiavi che non sono presenti nell'elenco delle chiavi riflesse più indietro in questo argomento. Le applicazioni devono disabilitare la reflection solo per le chiavi del Registro di sistema create e non tentare di disabilitare la reflection per le chiavi predefinite, ad esempio **HKEY \_ LOCAL \_ MACHINE** o **HKEY \_ CURRENT \_ USER.** Per determinare se le chiavi nell'elenco di reflection sono state disabilitate, usare la [**funzione RegQueryReflectionKey.**](/windows/desktop/api/winreg/nf-winreg-regqueryreflectionkey)

Le chiavi riflesse non devono essere usate nelle operazioni del Registro di sistema transazionate. La scrittura nelle chiavi riflesse durante una transazione può causare l'esito negativo della transazione. Per altre informazioni sulle transazioni, vedere [Gestione transazioni kernel.](/windows/desktop/Ktm/kernel-transaction-manager-portal)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Redirector del Registro di sistema](registry-redirector.md)
</dt> <dt>

[Reflection del Registro di sistema in Windows](/windows-hardware/drivers/display/microsoft-windows-vista-display-driver-64-bit-issues)
</dt> <dt>

[Chiavi del Registro di sistema interessate da WOW64](shared-registry-keys.md)
</dt> </dl>

 

 