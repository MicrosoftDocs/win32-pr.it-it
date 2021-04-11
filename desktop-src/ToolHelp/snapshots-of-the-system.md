---
title: Snapshot del sistema
description: Gli snapshot sono alla base delle funzioni della guida dello strumento. Uno snapshot è una copia di sola lettura dello stato corrente di uno o più degli elenchi seguenti che si trovano in processi di memoria di sistema, thread, moduli e heap.
ms.assetid: a8122960-f078-4efb-8e01-bf6fb69ee0dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ab6f9a45ad2e12eda53d3143e43c9234c20aae3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872713"
---
# <a name="snapshots-of-the-system"></a>Snapshot del sistema

Gli snapshot sono alla base delle funzioni della guida dello strumento. Uno snapshot è una copia di sola lettura dello stato corrente di uno o più degli elenchi seguenti che si trovano nella memoria di sistema: processi, thread, moduli e heap.

I processi che usano funzioni della Guida degli strumenti accedono a questi elenchi da snapshot anziché direttamente dal sistema operativo. Gli elenchi in memoria di sistema cambiano quando i processi vengono avviati e terminati, i thread vengono creati ed eliminati, i moduli eseguibili vengono caricati e scaricati dalla memoria di sistema e gli heap vengono creati ed eliminati. L'utilizzo di informazioni da uno snapshot impedisce le incoerenze. In caso contrario, le modifiche apportate a un elenco potrebbero causare l'attraversamento non corretto dell'elenco da parte di un thread o la causa di una violazione di accesso (un errore di GP). Se, ad esempio, un'applicazione attraversa l'elenco dei thread mentre vengono creati o terminati altri thread, le informazioni che l'applicazione usa per attraversare l'elenco dei thread potrebbero diventare obsolete e causare un errore per l'applicazione che attraversa l'elenco.

Per eseguire uno snapshot della memoria di sistema, usare la funzione [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) . Quando si chiama questa funzione, è possibile controllare il contenuto di uno snapshot specificando uno o più dei valori seguenti:

-   **\_SNAPHEAPLIST TH32CS**
-   **\_SNAPMODULE TH32CS**
-   **\_SNAPPROCESS TH32CS**
-   **\_SNAPTHREAD TH32CS**

I valori **TH32CS \_ SNAPHEAPLIST** e **TH32CS \_ SNAPMODULE** sono specifici del processo. Quando si specificano questi valori, gli elenchi di heap e moduli del processo specificato vengono inclusi nello snapshot. Se si specifica zero come identificatore del processo, viene usato il processo corrente. Il **valore \_ SNAPTHREAD di TH32CS** crea sempre uno snapshot a livello di sistema anche se un identificatore di processo viene passato a [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot).

Per enumerare lo stato dell'heap o del modulo per tutti i processi, specificare il valore **\_ SNAPALL di TH32CS** e l'identificatore del processo corrente. Quindi, per ogni processo aggiuntivo nello snapshot, chiamare di nuovo [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) , specificando il relativo identificatore di processo e il valore **TH32CS \_ SNAPHEAPLIST** o **TH32CS \_ SNAPMODULE** .

È possibile recuperare un codice di stato di errore esteso per [**CreateToolhelp32Snapshot**](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot) usando la funzione [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .

Quando il processo termina utilizzando uno snapshot, eliminarlo utilizzando la funzione [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) . Se non si elimina definitivamente uno snapshot, il processo perderà memoria fino a quando non si chiude, a quel punto il sistema recupera la memoria.

> [!Note]  
> L'handle di snapshot funge da handle di file ed è soggetto alle stesse regole relative ai processi e ai thread in cui è possibile utilizzarlo. Per specificare che l'handle è ereditabile, creare lo snapshot usando il **valore \_ ereditato TH32CS** .

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di uno snapshot e visualizzazione dei processi](taking-a-snapshot-and-viewing-processes.md)
</dt> </dl>

 

 