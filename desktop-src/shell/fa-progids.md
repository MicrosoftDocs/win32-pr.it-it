---
description: Shell usa una sottochiave del Registro di sistema ProgID (Programmatic Identifier) per associare un tipo di file a un'applicazione e per controllare il comportamento dell'associazione.
ms.assetid: f2b666d6-bf22-47b5-87e1-8de5ff51c152
title: Identificatori a livello di codice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf982f865fa8b856bc29c00a9b2371b88b34615b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467288"
---
# <a name="programmatic-identifiers"></a>Identificatori a livello di codice

Shell usa una sottochiave del Registro di sistema ProgID (Programmatic Identifier) per associare un tipo di file a un'applicazione e per controllare il comportamento dell'associazione. Le voci ProgID usate per le associazioni di file si trovano in **HKEY \_ CLASSES \_ ROOT** nel Registro di sistema.

Questo argomento è organizzato come segue:

-   [Elementi identificatore a livello di codice utilizzati dalle associazioni di file](#programmatic-identifier-elements-used-by-file-associations)
-   [Uso di identificatori a livello di codice con controllo delle versioni](#using-versioned-programmatic-identifiers)
-   [Argomenti correlati](#related-topics)

Per altre informazioni, vedere [Come registrare un tipo di file per una nuova applicazione](how-to-register-a-file-type-for-a-new-application.md)

## <a name="programmatic-identifier-elements-used-by-file-associations"></a>Elementi identificatore a livello di codice utilizzati dalle associazioni di file

Il formato corretto di un nome di chiave ProgID è \[ *Vendor o Application.* \] \[ *Componente* \] . \[ *Versione*, separata da punti e senza spazi, come \] Word.Document.6. La *parte Versione* è facoltativa ma fortemente consigliata. Per altre informazioni, vedere [Uso di identificatori a livello di codice con controllo delle versioni](#using-versioned-programmatic-identifiers).

Una sottochiave ProgID deve includere gli elementi seguenti. Si noti che alcuni dati stringa in questa chiave richiedono una formattazione specifica.




| Elemento | Descrizione | 
|---------|-------------|
| <strong>(Impostazione predefinita)</strong> | Impostare la voce predefinita della sottochiave ProgID su un nome descrittivo per progID, adatto per la visualizzazione all'utente. L'uso di questa voce per contenere il nome descrittivo è deprecato dalla voce FriendlyTypeName nei sistemi che eseguono Windows 2000 o versioni successive. Tuttavia, è necessario impostare questo valore per la compatibilità con le versioni precedenti.<br /> | 
| <strong>AllowSilentDefaultTakeOver</strong> (introdotto in Windows 8) | Impostare questa voce facoltativa per segnalare Windows questo ProgID quando si determina un gestore predefinito per un tipo di file pubblico. Indipendentemente dal fatto che questo valore sia impostato, progID continua a essere visualizzato nel menu di scelta rapida OpenWith e nella finestra di dialogo. Si tratta di un REG_NONE predefinito. | 
| <strong>AppUserModelID</strong> (introdotto in Windows 7) | Impostare questa voce facoltativa sull'ID modello utente dell'applicazione esplicito (AppUserModelID) se l'applicazione usa un <strong></strong> AppUserModelID esplicito e usa le Jump List recenti o <strong>frequenti</strong> generate automaticamente dal sistema o fornisce un Jump List. Se un'applicazione usa un AppUserModelID esplicito e non imposta questo valore, gli elementi non verranno visualizzati nelle Jump List dell'applicazione. Si tratta di una REG_SZ stringa. Per altre informazioni, vedere <a href="appids.md">ID modello utente applicazione (AppUserModelIDs)</a>.<br /> | 
| <strong>EditFlags</strong> | Impostare questa voce facoltativa usando i flag <a href="/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags"><strong>dell'enumerazione FILETYPEATTRIBUTEFLAGS.</strong></a> La voce EditFlags controlla alcuni aspetti della gestione della shell dei tipi di file collegati a questo ProgID. È anche possibile usare la voce EditFlags per limitare quanto l'utente può modificare determinati aspetti di questi tipi di file usando la finestra delle proprietà di un file. I <strong>valori FILETYPEATTRIBUTEFLAGS</strong> usati per EditFlags sono valori binari progettati in modo che sia possibile combinare più attributi in un singolo valore in un'operazione OR bit per bit. Si tratta di un REG_DWORD o REG_BINARY valore.<br /> | 
| <strong>FriendlyTypeName</strong> | Impostare questa voce su un nome descrittivo per ProgID, adatto per la visualizzazione all'utente. Per coerenza, questa stringa deve contenere gli stessi dati della voce Default per questa chiave ProgID. Questa voce può essere una stringa REG_SZ o REG_EXPAND_SZ, ma deve essere formattata come stringa indiretta (un nome di file completo e un valore di risorsa preceduto dal simbolo @), ad esempio <em>@%SystemRoot%\shell32.dll,-154</em>.<br /> | 
| <strong>InfoTip</strong> | Impostare questa voce su un breve messaggio della Guida visualizzato da Shell per questo ProgID. La voce InfoTip viene visualizzata in una finestra di dialogo con il mouse. Questo valore può essere una REG_SZ o REG_EXPAND_SZ stringa, ma, ad esempio FriendlyTypeName, deve essere formattato come stringa indiretta.<br /> | 
| <strong>CurVer</strong> | Impostare la voce (Predefinita) di questa sottochiave sulla versione più recente di questo ProgID.<br /><blockquote>[!Note]<br />A meno che non si dispone di versioni side-by-side dell'applicazione, cio' più versioni installate nello stesso sistema, è consigliabile evitare di usare <strong>CurVer</strong>.</blockquote><br /> | 
| <strong>DefaultIcon</strong>. | Impostare la voce (Predefinita) di questa sottochiave sull'icona predefinita che si vuole visualizzare per i tipi di file associati a questo ProgID. Questo valore può essere una stringa REG_SZ o REG_EXPAND_SZ, ma deve essere fornito come nome di file completo con il relativo valore di risorsa di supporto, ad esempio <em>%SystemRoot%\shell32.dll,-154</em>.<br /> | 




 

L'esempio di chiave del Registro di sistema seguente illustra un nodo chiave ProgID di associazione di file:

```
HKEY_CLASSES_ROOT
   Vendor.App.1
      (Default) = My Friendly Name
      AllowSilentDefaultTakeOver
      AppUserModelID = Vendor.Application
      EditFlags = 0x00000001
      FriendlyTypeName = @%SystemRoot%\shell32.dll,-154
      InfoTip = @%SystemRoot%\shell32.dll,-54
      CurVer
         (Default) = Vendor.App.1
      DefaultIcon
         (Default) = %SystemRoot%\shell32.dll,-1
```

## <a name="using-versioned-programmatic-identifiers"></a>Uso di identificatori a livello di codice con controllo delle versioni

Un ProgID con controllo delle versioni è quello la cui versione è indicata nel nome. A tale scopo, in genere si aggiunge un punto e il numero di versione al nome. Ad esempio:

-   Word.Document.6
-   Word.Document.8

Si tratta di ProgID con versione, rispettivamente con le versioni 6 e 8. Se si dispone di un'applicazione side-by-side, cio' che supporta più versioni dell'applicazione installate contemporaneamente, usare CurVer e ProgID indipendenti dalla versione. In caso contrario, è consigliabile evitare i progID CurVer e Version Independent perché causano inefficienze.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come registrare un tipo di file per una nuova applicazione](how-to-register-a-file-type-for-a-new-application.md)
</dt> <dt>

[Registrazione dell'applicazione](app-registration.md)
</dt> <dt>

[Tipi di file](fa-file-types.md)
</dt> <dt>

[Funzionamento delle associazioni di file](fa-how-work.md)
</dt> <dt>

[Visualizzazione contenuto per tipo o tipo di file](prophand-content-view.md)
</dt> <dt>

[Verifica del tipo di file](file-type-verifier.md)
</dt> <dt>

[Gestori dei tipi di file](fa-file-extensions.md)
</dt> <dt>

[Tipi percepiti](fa-perceivedtypes.md)
</dt> <dt>

[Matrici di associazioni](fa-associationarray.md)
</dt> </dl>

 

 




