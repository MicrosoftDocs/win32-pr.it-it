---
description: I messaggi sono definiti in un file di testo del messaggio. Il compilatore di messaggi assegna numeri a ogni messaggio e genera un file di inclusione C/C++ che l'applicazione può usare per accedere a un messaggio usando una costante simbolica.
ms.assetid: 99fbb3d6-6fde-4162-b0b9-99a1cdf0b8f8
title: File di testo dei messaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 818210cfe58fb8eafe939c70a2a57b358e306bb9bc072a64abebbec5ca41c266
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118151477"
---
# <a name="message-text-files"></a>File di testo dei messaggi

I messaggi sono definiti in un file di testo del messaggio. Il compilatore di messaggi assegna numeri a ogni messaggio e genera un file di inclusione C/C++ che l'applicazione può usare per accedere a un messaggio usando una costante simbolica.

La sintassi generale per le istruzioni in un file di testo del messaggio è la seguente:

*parola chiave* = *value*

Gli spazi intorno al segno di uguale vengono ignorati e il valore è delimitato da spazi vuoti (incluse le interruzioni di riga) dalla coppia parola chiave/valore successiva. La distinzione tra maiuscole e minuscole viene ignorata durante il confronto con i nomi delle parole chiave. La  parte del valore può essere una costante integer numerica che usa la sintassi C/C++, un nome di simbolo che segue le regole per gli identificatori C/C++ o un nome file con un massimo di 8 caratteri, senza punti.

Per un file di messaggio di esempio, vedere [File di testo del messaggio di esempio](sample-message-text-file.md).

## <a name="comments"></a>Commenti

Le righe di commento sono consentite nel file di testo del messaggio. Punto e virgola (;) inizia un commento che termina alla fine della riga. Seguire il punto e virgola con un indicatore di commento a riga singola C/C++ (//) in modo che il file di intestazione generato dal compilatore di messaggi venga compilato nell'applicazione.

``` syntax
;// This is a single-line comment.
```

Per un commento di blocco, iniziare ogni riga con un punto e virgola, quindi inserire un indicatore di commento di blocco aperto C/C++ (/ ) dopo il punto e virgola nella prima riga e l'indicatore di commento del blocco di chiusura ( /) dopo il punto e virgola \* \* nell'ultima riga.

``` syntax
;/* This is a block comment.
;   It spans multiple lines.
;*/
```

## <a name="header-section"></a>Sezione di intestazione

Il file di testo del messaggio contiene un'intestazione che definisce i nomi e gli identificatori di lingua che possono essere utilizzati dalle definizioni dei messaggi nel corpo del file. L'intestazione contiene zero o più delle istruzioni seguenti.



| Sintassi dell'istruzione                           | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MessageIdTypedef=*type*                    | Tipo da utilizzare nella definizione del messaggio come segue: \# define *name* ((*type*)0x *nnnnnnnn*)<br/> Il tipo deve essere sufficientemente grande da contenere l'intero codice del messaggio, ad esempio **un valore DWORD**. Il tipo può anche essere un tipo definito nel codice sorgente dell'applicazione. Il valore predefinito per *type* è vuoto, quindi non viene usato alcun cast di tipo. <br/> Questa istruzione può essere specificata nell'intestazione e con la frequenza necessaria nella sezione relativa alla definizione del messaggio.<br/>                                                                                                                  |
| SeverityNames=(*name* = *number* \[ :*name* \] ) | Set di nomi consentiti per la gravità in una definizione di messaggio. Associato a ogni nome di gravità è un numero che, se spostato a sinistra di 30 bit, fornisce il modello di bit a OR logico con i valori di struttura e ID messaggio per formare il codice del messaggio. Qualsiasi valore di gravità che non rientra in 2 bit è un errore. Ai codici di gravità possono essere dati anche nomi simbolici. Il valore predefinito è definito come segue: SeverityNames=( Success=0x0 Informational=0x1 Warning=0x2 Error=0x3)<br/>                                                                      |
| FacilityNames=(*name* = *number* \[ :*name* \] ) | Set di nomi consentiti per i valori della struttura in una definizione di messaggio. Associato a ogni nome di struttura è un numero che, se spostato a sinistra di 16 bit, fornisce il modello di bit a OR logico con i valori di gravità e ID messaggio per formare il codice del messaggio. Qualsiasi valore della struttura che non rientra in 12 bit è un errore. Ciò consente codici di struttura 4096. i primi 256 codici sono riservati all'uso del sistema. Ai codici di struttura possono essere dati anche nomi simbolici. Il valore predefinito è definito come segue: FacilityNames=( System=0x0FF Application=0xFFF)<br/> |
| LanguageNames=(*name* = *number*:*filename*) | Set di nomi consentiti per i valori della lingua in una definizione di messaggio. Il numero viene usato come identificatore di lingua nella tabella delle risorse. Il file specificato contiene i messaggi per tale lingua. Si tratta in genere di un file bin generato dal compilatore di messaggi.<br/> Un valore di esempio è: LanguageNames=(English=0x409:MSG00409)<br/> Per un elenco di identificatori di lingua, vedere <https://go.microsoft.com/fwlink/p/?linkid=190280> .<br/>                                                                                                                    |
| OutputBase=*number*                        | Radice di output per le costanti del messaggio che il compilatore di messaggi scrive nel file di intestazione. Se presente, questo valore esegue l'override dell'opzione -d. Questo numero può essere 10 (decimale) o 16 (esadecimale).                                                                                                                                                                                                                                                                                                                                                                                   |



 

## <a name="message-definitions"></a>Definizioni dei messaggi

Un file di testo del messaggio contiene zero o più definizioni di messaggio dopo la sezione dell'intestazione. Nella tabella seguente vengono descritte le istruzioni di definizione del messaggio. L'istruzione MessageId contrassegna l'inizio della definizione del messaggio. Le istruzioni Severity e Facility sono facoltative.



| Sintassi dell'istruzione                  | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MessageId= \[ *numero* \| + \] | Identificatore per il messaggio. Questa istruzione è obbligatoria, anche se il valore è facoltativo. Se non viene specificato alcun valore, il valore usato è il valore precedente per la struttura, più uno. Se il valore viene specificato con un segno più, il valore usato è il valore precedente per la struttura, più il numero dopo il segno più. Qualsiasi valore specificato deve essere compreso in 16 bit. Per altre informazioni sul formato del valore del messaggio a partire dalla gravità, dalla struttura e dall'ID del messaggio, vedere il diagramma in Winerror.h. Questo file di intestazione definisce i codici di errore per il sistema.<br/> |
| Severity=*name*                   | Uno dei valori specificati da SeverityNames nell'intestazione. Questa istruzione è facoltativa. Se non viene specificato alcun valore, il valore utilizzato è l'ultimo valore specificato per una definizione di messaggio. Il valore predefinito per la prima definizione del messaggio è `Severity=Success`<br/>                                                                                                                                                                                                                                                                                               |
| Facility=*name*                   | Uno dei valori specificati da FacilityNames nell'intestazione. Questa istruzione è facoltativa. Se non viene specificato alcun valore, il valore utilizzato è l'ultimo valore specificato per una definizione di messaggio. Il valore predefinito per la prima definizione del messaggio è `Facility=Application`<br/>                                                                                                                                                                                                                                                                                           |
| SymbolicName=*name*               | Associa una costante simbolica C/C++ al codice del messaggio. Viene usato nella definizione del messaggio come segue: \# define *name* ((*type*)0x *nnnnnnnn*)<br/>                                                                                                                                                                                                                                                                                                                                                                                                     |
| OutputBase={*number*}             | Radice di output per le costanti del messaggio che il compilatore di messaggi scrive nel file di intestazione. Se presente, questo valore esegue l'override dell'opzione -d. Questo numero può essere 10 (decimale) o 16 (esadecimale).                                                                                                                                                                                                                                                                                                                                                                 |
| Language=*name*                   | Uno dei valori specificati da LanguageNames nell'intestazione. Questa istruzione è facoltativa. Se non viene specificato alcun valore, il valore utilizzato è l'ultimo valore specificato per una definizione di messaggio. L'impostazione predefinita per la prima definizione del messaggio è la seguente: `Language=English`<br/>                                                                                                                                                                                                                                                                                   |
| *testo del messaggio*                    | Testo per il messaggio. È incluso nel file binario dei messaggi. È incluso anche nel file di intestazione nel blocco di commento che precede direttamente la definizione del messaggio.                                                                                                                                                                                                                                                                                                                                                                                        |
| .                                 | Il testo del messaggio viene terminato da una nuova riga contenente un singolo punto all'inizio della riga.                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



 

Se la definizione del messaggio include il testo del messaggio per più di una lingua, ogni lingua richiede la propria istruzione Language, il testo del messaggio e la terminazione di una nuova riga con un punto. Esempio:

``` syntax
MessageId=0x1
Severity=Error
Facility=Runtime
SymbolicName=MSG_BAD_COMMAND
Language=English
You have chosen an incorrect command.
.

Language=Japanese
<Japanese message string goes here>
.
```

È possibile specificare le sequenze di escape seguenti per la formattazione del testo del messaggio per l'uso da parte del visualizzatore eventi o dell'applicazione. Il carattere di segno di percentuale (%) inizia tutte le sequenze di escape. Qualsiasi altro carattere che segue un segno di percentuale viene visualizzato senza il segno di percentuale.

<dl> <dt>

<span id="_n__format_specifier__"></span><span id="_N__FORMAT_SPECIFIER__"></span>%*n* \[ ! *Identificatore \_ di formato*!\]
</dt> <dd>

Descrive un inserimento. Ogni inserimento è una voce nella matrice Arguments nella [**funzione FormatMessage.**](/windows/desktop/api/winbase/nf-winbase-formatmessage) Il valore *di n* può essere un numero compreso tra 1 e 99. L'identificatore di formato è facoltativo. Se non viene specificato alcun valore, il valore predefinito è !s!. Per informazioni sull'identificatore di formato, vedere [**wsprintf**](/windows/win32/api/winuser/nf-winuser-wsprintfa).

L'identificatore di formato può \* essere utilizzato per la precisione o la larghezza. Se specificato, vengono utilizzati gli inserimenti *numerati n*+1 *e n*+2.

</dd> <dt>

<span id="_0"></span>%0
</dt> <dd>

Termina una riga di testo del messaggio senza un carattere di nuova riga finale. Può essere usato per compilare una riga lunga o terminare un messaggio di richiesta senza un carattere di nuova riga finale.

</dd> <dt>

<span id="_."></span>%.
</dt> <dd>

Genera un singolo punto. Può essere usato per visualizzare un punto all'inizio di una riga, che altrimenti terminerebbe il testo del messaggio.

</dd> <dt>

<span id="__"></span>%!
</dt> <dd>

Genera un singolo punto esclamativo. Può essere usato per specificare un punto esclamativo immediatamente dopo un inserimento.

</dd> <dt>

<span id="__"></span>%%
</dt> <dd>

Genera un segno di percentuale singolo.

</dd> <dt>

<span id="_n"></span><span id="_N"></span>%n
</dt> <dd>

Genera un'interruzione di riga quando si verifica alla fine di una riga. Può essere usato con [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) per garantire che il messaggio si adatti a una determinata larghezza.

</dd> <dt>

<span id="_b"></span><span id="_B"></span>%b
</dt> <dd>

Genera uno spazio. Può essere usato per garantire un numero appropriato di spazi finali in una riga.

</dd> <dt>

<span id="_r"></span><span id="_R"></span>%r
</dt> <dd>

Genera un ritorno a capo rigido senza un carattere di nuova riga finale.

</dd> </dl>

 

