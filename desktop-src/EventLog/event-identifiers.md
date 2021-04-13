---
description: Gli identificatori di evento identificano in modo univoco un particolare evento.
ms.assetid: 83a84db4-572b-48bd-bc0f-071b2089a5ca
title: Identificatori evento (registrazione eventi)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 402337cb2c7e862785a88ec604c6382152736fd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527271"
---
# <a name="event-identifiers-event-logging"></a>Identificatori evento (registrazione eventi)

Gli identificatori di evento identificano in modo univoco un particolare evento. Ogni [origine evento](event-sources.md) può definire i propri eventi numerati e le stringhe di descrizione alle quali viene eseguito il mapping nel file di messaggio. I visualizzatori eventi possono presentare queste stringhe all'utente. Dovrebbero aiutare l'utente a capire cosa si è verificato un errore e suggerire quali azioni eseguire. Indirizzare la descrizione agli utenti che risolve i propri problemi, non agli amministratori o ai tecnici del supporto. Per ulteriori informazioni, vedere [linee guida](/windows/desktop/Debug/error-message-guidelines)per i messaggi di errore.

## <a name="format"></a>Formato

Il diagramma seguente illustra il formato di un identificatore di evento.

``` syntax
  3 3 2 2 2 2 2 2 2 2 2 2 1 1 1 1 1 1 1 1 1 1
  1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0
 +---+-+-+-----------------------+-------------------------------+
 |Sev|C|R|     Facility          |               Code            |
 +---+-+-+-----------------------+-------------------------------+
```

<dl> <dt>

<span id="Sev"></span><span id="sev"></span><span id="SEV"></span>Gravità
</dt> <dd>

Gravità. Il livello di gravità viene definito nel modo seguente:

<dl> <dd>00-operazione riuscita</dd> <dd>01-informativo</dd> <dd>10-avviso</dd> <dd>11-errore</dd> </dl> </dd> <dt>

<span id="C"></span><span id="c"></span>C
</dt> <dd>

Bit del cliente. Questo bit è definito come segue:

<dl> <dd>0-codice di sistema</dd> <dd>1-codice cliente</dd> </dl> </dd> <dt>

<span id="R"></span><span id="r"></span>R
</dt> <dd>

Bit riservati.

</dd> <dt>

<span id="Facility"></span><span id="facility"></span><span id="FACILITY"></span>Struttura
</dt> <dd>

Codice della struttura. Questo valore può essere null per la funzionalità \_ .

</dd> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Codice
</dt> <dd>

Codice di stato per la struttura.

</dd> </dl>

## <a name="message-definitions"></a>Definizioni dei messaggi

I messaggi vengono definiti nel file di messaggio dell'evento. Le stringhe di descrizione nel file dei messaggi di evento vengono indicizzate in base all'identificatore dell'evento, consentendo Visualizzatore eventi di visualizzare il testo specifico dell'evento per qualsiasi evento in base all'identificatore dell'evento. Tutte le descrizioni sono localizzate e dipendenti dalla lingua. Per ulteriori informazioni sulla compilazione di un file di messaggio, vedere [file di testo del messaggio](message-text-files.md).

Le stringhe di descrizione possono contenere segnaposto di stringa di inserimento, nel formato%*n*, dove %1 indica la prima stringa di inserimento e così via. Ad esempio, di seguito è riportata una voce di esempio nel file con estensione MC:

``` syntax
MessageId=0x4
Severity=Error
Facility=System
SymbolicName=MSG_CMD_DELETE
Language=English
File %1 contains %2, which is in error.
.
```

In questo caso, il buffer restituito da [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) contiene stringhe di inserimento. Il membro **NumStrings** della struttura [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) indica il numero di stringhe di inserimento. Il membro **StringOffset** della struttura **EVENTLOGRECORD** indica la posizione della prima stringa di inserimento nel buffer. È possibile passare una matrice di \_ PTRS DWORD che puntano all'indirizzo ogni stringa nel buffer quando si chiama la funzione [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) e le stringhe vengono inserite nel messaggio.

La stringa di descrizione può inoltre contenere segnaposto per le stringhe di parametri del file di messaggio dei parametri. Il formato dei segnaposto è%%*n*, dove% %1 viene sostituito dalla stringa del parametro con l'identificatore 1 e così via. Tuttavia, spetta all'utente inserire le stringhe dei parametri nella stringa di messaggio restituita da [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) . In genere, si chiama **FormatMessage** per ottenere la stringa di messaggio per l'evento. Viene quindi analizzata la stringa di messaggio per%%*n* parametri. Se il messaggio contiene uno o più parametri, caricare il valore del registro di sistema **ParameterMessageFile** per l'origine. Per ogni parametro nella stringa del messaggio, ottenere l'identificatore e passarlo a **FormatMessage** per ottenere la stringa di parametro. Sostituire il parametro nella stringa del messaggio con la stringa di parametro restituita da **FormatMessage** .

## <a name="insertion-strings"></a>Stringhe di inserimento

Le stringhe di inserimento sono stringhe indipendenti dal linguaggio facoltative utilizzate per inserire i valori per i segnaposto nelle stringhe di descrizione. Poiché le stringhe non sono localizzate, è fondamentale che questi segnaposto vengano utilizzati solo per rappresentare stringhe indipendenti dalla lingua, ad esempio valori numerici, nomi file, nomi utente e così via. La lunghezza della stringa non deve superare 32 kilobyte-1 caratteri.

Evitare di usare più stringhe per creare una descrizione più ampia. Una stringa di inserimento deve essere considerata come dati, non come testo. Nell'esempio seguente, ad esempio, pszString1 e pszString2 non devono essere usati come stringhe di inserimento per pszDescription.

``` syntax
LPSTR pszString1 = "successfully"; 
LPSTR pszString2 = "not"; 
LPSTR pszDescription = "The user was %1 added to the database.";
```

Nell'esempio seguente è opportuno usare pszString1 o pszString2 per la stringa di inserimento in pszDescription.

``` syntax
LPSTR pszString1 = "c:\\testapp1.c"; 
LPSTR pszString2 = "c:\\testapp2.c"; 
LPSTR pszDescription = "Access denied. Attempted to open the file %1."
```

 

 
