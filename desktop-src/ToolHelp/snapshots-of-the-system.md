---
title: Snapshot del sistema
description: Gli snapshot sono alla base delle funzioni della Guida dello strumento. Uno snapshot è una copia di sola lettura dello stato corrente di uno o più degli elenchi seguenti che risiedono in processi, thread, moduli e heap della memoria di sistema.
ms.assetid: a8122960-f078-4efb-8e01-bf6fb69ee0dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30dde3a4383bf56bdef46c59c55611ffe9b22a7a201abb4f0f11af85594c4f0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137414"
---
# <a name="snapshots-of-the-system"></a>Snapshot del sistema

Gli snapshot sono alla base delle funzioni della Guida dello strumento. Uno snapshot è una copia di sola lettura dello stato corrente di uno o più degli elenchi seguenti che risiedono nella memoria di sistema: processi, thread, moduli e heap.

I processi che usano lo strumento consentono alle funzioni di accedere a questi elenchi dagli snapshot anziché direttamente dal sistema operativo. Gli elenchi nella memoria di sistema cambiano quando i processi vengono avviati e terminati, i thread vengono creati ed distrutti, i moduli eseguibili vengono caricati e scaricati dalla memoria di sistema e gli heap vengono creati ed distrutti. L'uso di informazioni da uno snapshot impedisce incoerenze. In caso contrario, le modifiche a un elenco potrebbero causare un thread che attraversa in modo errato l'elenco o causa una violazione di accesso (un errore di Criteri di gruppo). Ad esempio, se un'applicazione attraversa l'elenco di thread mentre altri thread vengono creati o terminati, le informazioni che l'applicazione usa per attraversare l'elenco di thread potrebbero diventare obsolete e potrebbero causare un errore per l'applicazione che attraversa l'elenco.

Per creare uno snapshot della memoria di sistema, usare la [**funzione CreateToolhelp32Snapshot.**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) È possibile controllare il contenuto di uno snapshot specificando uno o più dei valori seguenti quando si chiama questa funzione:

-   **TH32CS \_ SNAPHEAPLIST**
-   **TH32CS \_ SNAPMODULE**
-   **TH32CS \_ SNAPPROCESS**
-   **TH32CS \_ SNAPTHREAD**

I **valori TH32CS \_ SNAPHEAPLIST** e **TH32CS \_ SNAPMODULE** sono specifici del processo. Quando questi valori vengono specificati, gli elenchi di heap e moduli del processo specificato vengono inclusi nello snapshot. Se si specifica zero come identificatore di processo, viene usato il processo corrente. Il **valore TH32CS \_ SNAPTHREAD** crea sempre uno snapshot a livello di sistema anche se viene passato un identificatore di processo a [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot).

Per enumerare lo stato dell'heap o del modulo per tutti i processi, specificare il **valore \_ SNAPALL TH32CS** e l'identificatore del processo corrente. Quindi, per ogni processo aggiuntivo nello snapshot, chiamare di nuovo [**CreateToolhelp32Snapshot,**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) specificando il relativo identificatore di processo e il valore **TH32CS \_ SNAPHEAPLIST** o **TH32CS \_ SNAPMODULE.**

È possibile recuperare un codice di stato di errore esteso [**per CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) usando la [**funzione GetLastError.**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)

Quando il processo termina con uno snapshot, eliminarlo usando la [**funzione CloseHandle.**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) Se non si elimina uno snapshot, il processo perderà memoria fino alla chiusura del processo, in cui il sistema recupera la memoria.

> [!Note]  
> L'handle di snapshot agisce come un handle di file ed è soggetto alle stesse regole relative ai processi e ai thread in cui può essere usato. Per specificare che l'handle è ereditabile, creare lo snapshot usando il valore **TH32CS \_ INHERIT.**

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di uno snapshot e visualizzazione dei processi](taking-a-snapshot-and-viewing-processes.md)
</dt> </dl>

 

 