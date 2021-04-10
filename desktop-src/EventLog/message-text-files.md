---
description: I messaggi vengono definiti in un file di testo del messaggio. Il compilatore di messaggi assegna numeri a ogni messaggio e genera un file di inclusione C/C++ che può essere utilizzato dall'applicazione per accedere a un messaggio utilizzando una costante simbolica.
ms.assetid: 99fbb3d6-6fde-4162-b0b9-99a1cdf0b8f8
title: File di testo del messaggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e87547f44b0b556df4e3a2ffb67736b950321c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227065"
---
# <a name="message-text-files"></a>File di testo del messaggio

I messaggi vengono definiti in un file di testo del messaggio. Il compilatore di messaggi assegna numeri a ogni messaggio e genera un file di inclusione C/C++ che può essere utilizzato dall'applicazione per accedere a un messaggio utilizzando una costante simbolica.

La sintassi generale per le istruzioni in un file di testo del messaggio è la seguente:

*parola chiave* = *valore* di

Gli spazi intorno al segno di uguale vengono ignorati e il valore è delimitato da spazi vuoti (incluse le interruzioni di riga) dalla coppia parola chiave/valore successiva. Il caso viene ignorato quando si esegue il confronto con nomi di parole chiave. La parte relativa al *valore* può essere una costante Integer numerica usando la sintassi c/c++, un nome di simbolo che segue le regole per gli identificatori c/c++ o un nome file con 8 caratteri o meno, senza punti.

Per un file di messaggio di esempio, vedere [esempio di file di testo del messaggio](sample-message-text-file.md).

## <a name="comments"></a>Commenti

Nel file di testo del messaggio sono consentite righe di commento. Punto e virgola (;) inizia un commento che termina alla fine della riga. Seguire il punto e virgola con un indicatore di commento a riga singola C/C++ (//), in modo che il file di intestazione generato dal compilatore di messaggi venga compilato nell'applicazione.

``` syntax
;// This is a single-line comment.
```

Per un commento di blocco, iniziare ogni riga con un punto e virgola, quindi posizionare un indicatore di commento di blocco aperto C/C++ (/ \* ) dopo il punto e virgola sulla prima riga e l'indicatore di commento di blocco di chiusura ( \* /) dopo il punto e virgola sull'ultima riga.

``` syntax
;/* This is a block comment.
;   It spans multiple lines.
;*/
```

## <a name="header-section"></a>Sezione di intestazione

Il file di testo del messaggio contiene un'intestazione che definisce i nomi e gli identificatori di lingua usati dalle definizioni dei messaggi nel corpo del file. L'intestazione contiene zero o più delle istruzioni seguenti.



| Sintassi dell'istruzione                           | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MessageIdTypedef =*tipo*                    | Tipo da utilizzare nella definizione del messaggio come segue: \# define *Name* ((*Type*) 0x *nnnnnnnn*)<br/> Il tipo deve essere sufficientemente grande da contenere l'intero codice del messaggio, ad esempio un **valore DWORD**. Il tipo può essere anche un tipo definito nel codice sorgente dell'applicazione. Il valore predefinito per il *tipo* è vuoto, pertanto non viene utilizzato alcun cast di tipo. <br/> Questa istruzione può essere specificata nell'intestazione e nel modo più frequente necessario nella sezione definizione messaggio.<br/>                                                                                                                  |
| SeverityNames = ( = *numero* nome \[ :*nome* \] ) | Set di nomi consentiti per la gravità in una definizione del messaggio. Associato a ogni nome di gravità è un numero che, se spostato a sinistra di 30 bit, assegna allo schema di bit i valori logici o con la struttura e l'ID del messaggio per formare il codice del messaggio. Qualsiasi valore di gravità che non si adatta a 2 bit è un errore. Ai codici di gravità possono essere assegnati anche nomi simbolici. Il valore predefinito è definito nel modo seguente: SeverityNames = (Success = 0x0 Informational = 0x1 Warning = 0x2 Error = 0x3)<br/>                                                                      |
| FacilityNames = ( = *numero* nome \[ :*nome* \] ) | Set di nomi consentiti per i valori della struttura in una definizione del messaggio. Associato a ogni nome di struttura è un numero che, quando viene spostato a sinistra di 16 bit, fornisce lo schema di bit a Logical-OR con i valori di gravità e ID del messaggio per formare il codice del messaggio. Qualsiasi valore di struttura che non si adatta a 12 bit è un errore. Questo consente i codici di struttura 4096; i primi 256 codici sono riservati per l'utilizzo da parte del sistema. Ai codici di struttura è possibile assegnare anche nomi simbolici. Il valore predefinito è definito nel modo seguente: FacilityNames = (System = 0x0FF Application = 0xFFF)<br/> |
| LanguageNames = ( = *numero* nome:*nomefile*) | Set di nomi consentiti per i valori della lingua nella definizione di un messaggio. Il numero viene usato come identificatore della lingua nella tabella delle risorse. Il file specificato contiene i messaggi per tale lingua. Si tratta in genere di un file con estensione bin generato dal compilatore di messaggi.<br/> Un valore di esempio è: LanguageNames = (English = 0x409: MSG00409)<br/> Per un elenco degli identificatori di lingua, vedere <https://go.microsoft.com/fwlink/p/?linkid=190280> .<br/>                                                                                                                    |
| OutputBase =*numero*                        | Radice di output per le costanti del messaggio scritte dal compilatore del messaggio nel file di intestazione. Se presente, questo valore sostituisce l'opzione-d. Questo numero può essere 10 (decimale) o 16 (esadecimale).                                                                                                                                                                                                                                                                                                                                                                                   |



 

## <a name="message-definitions"></a>Definizioni dei messaggi

Un file di testo del messaggio contiene zero o più definizioni di messaggio che seguono la sezione dell'intestazione. Nella tabella seguente vengono descritte le istruzioni per la definizione del messaggio. L'istruzione MessageId contrassegna l'inizio della definizione del messaggio. Il livello di gravità e le istruzioni della funzione sono facoltativi.



| Sintassi dell'istruzione                  | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MessageId = \[ numero numero \| + \] | Identificatore del messaggio. Questa istruzione è obbligatoria, anche se il valore è facoltativo. Se non viene specificato alcun valore, il valore usato è il valore precedente per la struttura, più uno. Se il valore viene specificato con un segno più, il valore usato è il valore precedente per la struttura, più il numero dopo il segno di addizione. Qualsiasi valore specificato deve rientrare in 16 bit. Per ulteriori informazioni sulla forma del valore del messaggio in base alla gravità, alla funzionalità e all'ID del messaggio, vedere il diagramma in Winerror. h. Questo file di intestazione definisce i codici di errore per il sistema.<br/> |
| Gravità =*nome*                   | Uno dei valori specificati da SeverityNames nell'intestazione. Questa istruzione è facoltativa. Se non viene specificato alcun valore, il valore usato è il valore dell'ultima volta specificato per la definizione di un messaggio. Il valore predefinito per la prima definizione di messaggio è `Severity=Success`<br/>                                                                                                                                                                                                                                                                                               |
| Funzione =*nome*                   | Uno dei valori specificati da FacilityNames nell'intestazione. Questa istruzione è facoltativa. Se non viene specificato alcun valore, il valore usato è il valore dell'ultima volta specificato per la definizione di un messaggio. Il valore predefinito per la prima definizione di messaggio è `Facility=Application`<br/>                                                                                                                                                                                                                                                                                           |
| *Nome* simbolico =               | Associa una costante simbolica C/C++ al codice del messaggio. Viene usato nella definizione del messaggio come segue: \# define *Name* ((*Type*) 0x *nnnnnnnn*)<br/>                                                                                                                                                                                                                                                                                                                                                                                                     |
| OutputBase = {*Number*}             | Radice di output per le costanti di messaggio scritte dal compilatore del messaggio nel file di intestazione. Se presente, questo valore sostituisce l'opzione-d. Questo numero può essere 10 (decimale) o 16 (esadecimale).                                                                                                                                                                                                                                                                                                                                                                 |
| Lingua =*nome*                   | Uno dei valori specificati da LanguageNames nell'intestazione. Questa istruzione è facoltativa. Se non viene specificato alcun valore, il valore usato è il valore dell'ultima volta specificato per la definizione di un messaggio. Il valore predefinito per la prima definizione di messaggio è il seguente: `Language=English`<br/>                                                                                                                                                                                                                                                                                   |
| *testo del messaggio*                    | Testo per il messaggio. È incluso nel file binario del messaggio. Viene anche incluso nel file di intestazione nel blocco di commento che precede direttamente la definizione del messaggio.                                                                                                                                                                                                                                                                                                                                                                                        |
| .                                 | Il testo del messaggio viene terminato da una nuova riga contenente un singolo punto all'inizio della riga.                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



 

Se la definizione del messaggio include il testo del messaggio per più di una lingua, ogni lingua richiede la propria istruzione language, il testo del messaggio e la nuova riga che termina con un punto. Ad esempio:

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

È possibile specificare le sequenze di escape seguenti per formattare il testo del messaggio per l'uso da parte del Visualizzatore eventi o dell'applicazione. Carattere del segno di percentuale (%) inizia tutte le sequenze di escape. Qualsiasi altro carattere che segue un segno di percentuale viene visualizzato senza il segno di percentuale.

<dl> <dt>

<span id="_n__format_specifier__"></span><span id="_N__FORMAT_SPECIFIER__"></span>%*n* \[ ! *\_ identificatore di formato*.\]
</dt> <dd>

Descrive un'istruzione INSERT. Ogni inserimento è una voce nella matrice arguments della funzione [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) . Il valore di *n* può essere un numero compreso tra 1 e 99. L'identificatore di formato è facoltativo. Se non viene specificato alcun valore, il valore predefinito è! s!. Per informazioni sull'identificatore di formato, vedere [**wsprintf**](/windows/win32/api/winuser/nf-winuser-wsprintfa).

L'identificatore di formato può \* essere utilizzato per la precisione o la larghezza. Quando specificato, vengono utilizzati inserimenti numerati *n*+ 1 e *n*+ 2.

</dd> <dt>

<span id="_0"></span>%0
</dt> <dd>

Termina una riga di testo del messaggio senza un carattere di nuova riga finale. Questa operazione può essere utilizzata per compilare una riga estesa o terminare un messaggio di richiesta senza un carattere di nuova riga finale.

</dd> <dt>

<span id="_."></span>%.
</dt> <dd>

Genera un singolo punto. Questa operazione può essere utilizzata per visualizzare un punto all'inizio di una riga, che altrimenti terminerebbe il testo del messaggio.

</dd> <dt>

<span id="__"></span>%!
</dt> <dd>

Genera un singolo punto esclamativo. Questa operazione può essere utilizzata per specificare un punto esclamativo immediatamente dopo un inserimento.

</dd> <dt>

<span id="__"></span>%%
</dt> <dd>

Genera un solo segno di percentuale.

</dd> <dt>

<span id="_n"></span><span id="_N"></span>% n
</dt> <dd>

Genera un'interruzioni di riga rigido quando si verifica alla fine di una riga. Questa operazione può essere utilizzata con [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) per garantire che il messaggio corrisponda a una determinata larghezza.

</dd> <dt>

<span id="_b"></span><span id="_B"></span>% b
</dt> <dd>

Genera uno spazio. Questa operazione può essere utilizzata per garantire un numero appropriato di spazi finali su una riga.

</dd> <dt>

<span id="_r"></span><span id="_R"></span>% r
</dt> <dd>

Genera un ritorno a capo rigido senza un carattere di nuova riga finale.

</dd> </dl>

 

