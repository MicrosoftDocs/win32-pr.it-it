---
description: Il programma di installazione fornisce funzioni che modificano i record in un database di installazione. Queste funzioni possono essere utilizzate insieme alle funzioni descritte in utilizzo delle query per apportare modifiche effettive in un database.
ms.assetid: 5ea3fb1d-ddcb-4013-84dc-dd6f90c5751a
title: Utilizzo dei record
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3252dc29bf755d08494dbdc2326bf45a4afb1c91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313776"
---
# <a name="working-with-records"></a>Utilizzo dei record

Il programma di installazione fornisce funzioni che modificano i record in un database di installazione. Queste funzioni possono essere utilizzate insieme alle funzioni descritte in utilizzo delle [query](working-with-queries.md) per apportare modifiche effettive in un database.

Le funzioni seguenti creano o rimuovono i record:

-   Per creare un nuovo record per un database, chiamare la funzione [**MsiCreateRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord) .
-   Per cancellare i dati da un record, impostare ogni campo su null chiamando la funzione [**MsiRecordClearData**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordcleardata) .

Le funzioni seguenti riempiono i campi di record specificati:

-   Per impostare un record su un numero intero, chiamare la funzione [**MsiRecordSetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetinteger) .
-   Per impostare un record su una stringa, chiamare la funzione [**MsiRecordSetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa) .
-   Per inserire un intero file in un campo del flusso, chiamare la funzione [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) .

Le funzioni seguenti leggono i valori dei campi di record specificati:

-   Per leggere un valore integer da un campo, chiamare la funzione [**MsiRecordGetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetinteger) .
-   Per recuperare un valore stringa, chiamare la funzione [**MsiRecordGetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetstringa) .
-   Per ottenere un flusso, chiamare la funzione [**MsiRecordReadStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream) .
-   Per determinare se un determinato campo di un record è null, chiamare la funzione [**MsiRecordIsNull**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordisnull) .

Le funzioni seguenti sono funzioni di record informativi:

-   Per ottenere il numero di campi contenuti in un record, chiamare la funzione [**MsiRecordGetFieldCount**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetfieldcount) .
-   Per ottenere le dimensioni di un campo, chiamare la funzione [**MsiRecordDataSize**](/windows/desktop/api/Msiquery/nf-msiquery-msirecorddatasize) . Il valore restituito di **MsiRecordDataSize** è sensibile al tipo di campo.

 

 



