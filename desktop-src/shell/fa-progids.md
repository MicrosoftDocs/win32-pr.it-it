---
description: La shell usa una sottochiave del registro di sistema ProgID (Programmatic Identifier) per associare un tipo di file a un'applicazione e per controllare il comportamento dell'associazione.
ms.assetid: f2b666d6-bf22-47b5-87e1-8de5ff51c152
title: Identificatori a livello di codice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67720fed1ad4b8401d11f6532cdc79836911e7cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993709"
---
# <a name="programmatic-identifiers"></a>Identificatori a livello di codice

La shell usa una sottochiave del registro di sistema ProgID (Programmatic Identifier) per associare un tipo di file a un'applicazione e per controllare il comportamento dell'associazione. Le voci ProgID usate per le associazioni di file si trovano in **HKEY \_ classi \_ radice** nel registro di sistema.

Questo argomento è organizzato nel modo seguente:

-   [Elementi identificatore a livello di codice usati dalle associazioni di file](#programmatic-identifier-elements-used-by-file-associations)
-   [Utilizzo di identificatori a livello di codice con versione](#using-versioned-programmatic-identifiers)
-   [Argomenti correlati](#related-topics)

Per ulteriori informazioni, vedere [come registrare un tipo di file per una nuova applicazione](how-to-register-a-file-type-for-a-new-application.md)

## <a name="programmatic-identifier-elements-used-by-file-associations"></a>Elementi identificatore a livello di codice usati dalle associazioni di file

Il formato corretto del nome di una chiave ProgID è \[ *vendor o Application* \] . \[ *Componente* \] . \[ *Versione* \] , separata da punti e senza spazi, come in Word.Document. 6. La parte relativa alla *versione* è facoltativa ma fortemente consigliata. Per ulteriori informazioni, vedere [utilizzo di identificatori a livello di codice con versione](#using-versioned-programmatic-identifiers).

Una sottochiave ProgID deve includere gli elementi seguenti. Si noti che alcuni dati stringa in questa chiave richiedono una formattazione specifica.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Predefinita</strong></td>
<td>Impostare la voce predefinita della sottochiave ProgID su un nome descrittivo per il ProgID, adatto per la visualizzazione all'utente. L'uso di questa voce per conservare il nome descrittivo è deprecato dalla voce FriendlyTypeName nei sistemi che eseguono Windows 2000 o versioni successive. Tuttavia, è necessario impostare questo valore per la compatibilità con le versioni precedenti.<br/></td>
</tr>
<tr class="even">
<td><strong>AllowSilentDefaultTakeOver</strong> (introdotta in Windows 8)</td>
<td>Impostare questa voce facoltativa per segnalare che Windows deve ignorare questo ProgID quando si determina un gestore predefinito per un tipo di file pubblico. Indipendentemente dall'impostazione di questo valore, il ProgID continuerà a essere visualizzato nel menu di scelta rapida e nella finestra di dialogo OpenWith. Si tratta di un valore REG_NONE.</td>
</tr>
<tr class="odd">
<td><strong>AppUserModelID</strong> (introdotta in Windows 7)</td>
<td>Impostare questa voce facoltativa sull'ID del modello utente dell'applicazione esplicita dell'applicazione (AppUserModelID) se l'applicazione usa un AppUserModelID esplicito e usa gli elenchi di salto <strong>recenti</strong> o <strong>frequenti</strong> generati automaticamente dal sistema oppure fornisce una Jump List personalizzata. Se un'applicazione usa un AppUserModelID esplicito e non imposta questo valore, gli elementi non verranno visualizzati nelle Jump List dell'applicazione. Si tratta di una stringa REG_SZ. Per ulteriori informazioni, vedere <a href="appids.md">ID modello utente applicazione (AppUserModelIDs)</a>.<br/></td>
</tr>
<tr class="even">
<td><strong>EditFlags</strong></td>
<td>Impostare questa voce facoltativa utilizzando i flag dell'enumerazione <a href="/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags"><strong>FILETYPEATTRIBUTEFLAGS</strong></a> . La voce flag controlla alcuni aspetti della gestione della shell dei tipi di file collegati a questo ProgID. È anche possibile usare la voce flag per limitare la quantità di dati che l'utente può modificare per determinati aspetti di questi tipi di file usando la finestra delle proprietà di un file. I valori <strong>FILETYPEATTRIBUTEFLAGS</strong> usati per flag sono valori binari progettati in modo da poter combinare più attributi in un singolo valore in un'operazione OR bit per bit. Si tratta di un valore REG_DWORD o REG_BINARY.<br/></td>
</tr>
<tr class="odd">
<td><strong>FriendlyTypeName</strong></td>
<td>Impostare questa voce su un nome descrittivo per il ProgID, adatto per la visualizzazione all'utente. Per coerenza, questa stringa deve contenere gli stessi dati della voce predefinita per la chiave ProgID. Questa voce può essere una stringa REG_SZ o REG_EXPAND_SZ, ma deve essere formattata come stringa indiretta (un nome file completo e un valore di risorsa preceduto dal simbolo @), ad esempio <em>@% systemroot% \shell32.dll,-154</em>.<br/></td>
</tr>
<tr class="even">
<td><strong>InfoTip</strong></td>
<td>Impostare questa voce su un breve messaggio della Guida visualizzato dalla Shell per questo ProgID. La voce InfoTip viene visualizzata in una finestra di dialogo del passaggio del mouse. Questo valore può essere una stringa REG_SZ o REG_EXPAND_SZ ma, ad esempio FriendlyTypeName, deve essere formattata come stringa indiretta.<br/></td>
</tr>
<tr class="odd">
<td><strong>CurVer</strong></td>
<td>Impostare la voce (impostazione predefinita) di questa sottochiave sulla versione più recente di questo ProgID.<br/>
<blockquote>
[!Note]<br />
A meno che non si disponga di versioni dell'applicazione side-by-Side, ovvero più versioni installate nello stesso sistema, è consigliabile evitare di utilizzare <strong>Curver</strong>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>DefaultIcon</strong>.</td>
<td>Impostare la voce (impostazione predefinita) di questa sottochiave sull'icona predefinita che si desidera visualizzare per i tipi di file associati a questo ProgID. Questo valore può essere una stringa REG_SZ o REG_EXPAND_SZ, ma deve essere specificato come nome di file completo con il relativo valore di risorsa di supervisore, ad esempio <em>% systemroot% \shell32.dll,-154</em>.<br/></td>
</tr>
</tbody>
</table>



 

Nell'esempio di chiave del registro di sistema seguente viene illustrato un nodo chiave ProgID di associazione file:

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

## <a name="using-versioned-programmatic-identifiers"></a>Utilizzo di identificatori a livello di codice con versione

Un ProgID con versione è uno la cui versione è indicata nel nome. Questa operazione viene in genere eseguita aggiungendo un punto e il numero di versione al nome. Ad esempio:

-   Word.Document. 6
-   Word.Document. 8

Si tratta di ProgID con versione, rispettivamente con le versioni 6 e 8. Se si dispone di un'applicazione side-by-Side, ovvero una che supporta più versioni dell'applicazione installate contemporaneamente, utilizzare i ProgID di curvar e della versione indipendenti. In caso contrario, è consigliabile evitare i ProgID indipendenti dalla curva e dalla versione perché comporteranno un'inefficienza.

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

[Visualizzazione contenuto per tipo di file o tipo](prophand-content-view.md)
</dt> <dt>

[Tipo di file Verifier](file-type-verifier.md)
</dt> <dt>

[Gestori di tipi di file](fa-file-extensions.md)
</dt> <dt>

[Tipi percepiti](fa-perceivedtypes.md)
</dt> <dt>

[Matrici di associazione](fa-associationarray.md)
</dt> </dl>

 

 




