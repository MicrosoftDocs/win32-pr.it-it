---
description: Gli identificatori di evento identificano in modo univoco un evento specifico.
ms.assetid: 83a84db4-572b-48bd-bc0f-071b2089a5ca
title: Identificatori di evento (registrazione eventi)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 933ef3fafe77a2d0fbc2e62b5b11dd499eb850dc5cb6b2ecdc6c952fe1a3f205
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951440"
---
# <a name="event-identifiers-event-logging"></a>Identificatori di evento (registrazione eventi)

Gli identificatori di evento identificano in modo univoco un evento specifico. Ogni [origine evento](event-sources.md) può definire i propri eventi numerati e le stringhe di descrizione a cui vengono mappati nel relativo file di messaggio. I visualizzatori di eventi possono presentare queste stringhe all'utente. Devono aiutare l'utente a comprendere cosa è andato storto e suggerire le azioni da intraprendere. Indirizzare la descrizione agli utenti per risolvere i propri problemi, non agli amministratori o ai tecnici del supporto tecnico. Per altre informazioni, vedere [Linee guida per i messaggi di errore](/windows/desktop/Debug/error-message-guidelines).

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

<span id="Sev"></span><span id="sev"></span><span id="SEV"></span>Sev
</dt> <dd>

Gravità. La gravità è definita nel modo seguente:

<dl> <dd>00 - Operazione riuscita</dd> <dd>01 - Informativo</dd> <dd>10 - Avviso</dd> <dd>11 - Errore</dd> </dl> </dd> <dt>

<span id="C"></span><span id="c"></span>C
</dt> <dd>

Bit del cliente. Questo bit viene definito nel modo seguente:

<dl> <dd>0 - Codice di sistema</dd> <dd>1 - Codice cliente</dd> </dl> </dd> <dt>

<span id="R"></span><span id="r"></span>R
</dt> <dd>

Bit riservati.

</dd> <dt>

<span id="Facility"></span><span id="facility"></span><span id="FACILITY"></span>Struttura
</dt> <dd>

Codice della struttura. Questo valore può essere FACILITY \_ NULL.

</dd> <dt>

<span id="Code"></span><span id="code"></span><span id="CODE"></span>Codice
</dt> <dd>

Codice di stato per la struttura.

</dd> </dl>

## <a name="message-definitions"></a>Definizioni dei messaggi

I messaggi vengono definiti nel file dei messaggi di evento. Le stringhe di descrizione nel file del messaggio di evento vengono indicizzate in base all'identificatore dell'evento, consentendo Visualizzatore eventi di visualizzare il testo specifico dell'evento per qualsiasi evento in base all'identificatore dell'evento. Tutte le descrizioni sono localizzate e dipendono dalla lingua. Per altre informazioni sulla compilazione di un file di messaggio, vedere [File di testo dei messaggi](message-text-files.md).

Le stringhe di descrizione possono contenere segnaposto della stringa di inserimento, nel formato %*n*, dove %1 indica la prima stringa di inserimento e così via. Ad esempio, di seguito è riportata una voce di esempio nel file con estensione mc:

``` syntax
MessageId=0x4
Severity=Error
Facility=System
SymbolicName=MSG_CMD_DELETE
Language=English
File %1 contains %2, which is in error.
.
```

In questo caso, il buffer restituito da [**ReadEventLog contiene**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) stringhe di inserimento. Il **membro NumStrings** della struttura [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) indica il numero di stringhe di inserimento. Il **membro StringOffset** della **struttura EVENTLOGRECORD** indica la posizione della prima stringa di inserimento nel buffer. È possibile passare una matrice di DWORD PTR che puntano all'indirizzo di ogni stringa nel buffer quando si chiama la funzione FormatMessage e inserirà le stringhe \_ nel messaggio. [](/windows/desktop/api/winbase/nf-winbase-formatmessage)

La stringa di descrizione può contenere anche segnaposto per le stringhe di parametro dal file di messaggio del parametro. I segnaposto sono nel formato %%*n*, dove %%1 viene sostituito dalla stringa di parametro con l'identificatore 1 e così via. Tuttavia, è necessario inserire le stringhe dei parametri nella stringa di messaggio restituita [**da FormatMessage.**](/windows/desktop/api/winbase/nf-winbase-formatmessage) In genere, si chiama **FormatMessage** per ottenere la stringa di messaggio per l'evento. Analizzare quindi la stringa di messaggio per %%*n* parametri. Se il messaggio contiene uno o più parametri, caricare il **valore del Registro di sistema ParameterMessageFile** per l'origine. Per ogni parametro nella stringa del messaggio, ottenere l'identificatore e passarlo a **FormatMessage** per ottenere la stringa del parametro. Sostituire il parametro nella stringa del messaggio con la stringa di parametro **restituita da FormatMessage.**

## <a name="insertion-strings"></a>Stringhe di inserimento

Le stringhe di inserimento sono stringhe facoltative indipendenti dalla lingua usate per compilare i valori per i segnaposto nelle stringhe di descrizione. Poiché le stringhe non sono localizzate, è fondamentale che questi segnaposto siano usati solo per rappresentare stringhe indipendenti dalla lingua, ad esempio valori numerici, nomi di file, nomi utente e così via. La lunghezza della stringa non deve superare i 32 kilobyte - 1 caratteri.

Evitare di usare più stringhe per creare una descrizione più ampia. Una stringa di inserimento deve essere considerata come dati, non come testo. Nell'esempio seguente, ad esempio, pszString1 e pszString2 non devono essere usati come stringhe di inserimento per pszDescription.

``` syntax
LPSTR pszString1 = "successfully"; 
LPSTR pszString2 = "not"; 
LPSTR pszDescription = "The user was %1 added to the database.";
```

Nell'esempio seguente è appropriato usare pszString1 o pszString2 per la stringa di inserimento in pszDescription.

``` syntax
LPSTR pszString1 = "c:\\testapp1.c"; 
LPSTR pszString2 = "c:\\testapp2.c"; 
LPSTR pszDescription = "Access denied. Attempted to open the file %1."
```

 

 
