---
description: Il programma di installazione fornisce funzioni che modificano i record in un database di installazione. Queste funzioni possono essere usate in combinazione con le funzioni descritte in Utilizzo delle query per apportare modifiche effettive in un database.
ms.assetid: 5ea3fb1d-ddcb-4013-84dc-dd6f90c5751a
title: Uso dei record
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12f83159688ec106b8e3cea3021e4352c851620d0e2f89661cee823c1439c120
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498381"
---
# <a name="working-with-records"></a>Uso dei record

Il programma di installazione fornisce funzioni che modificano i record in un database di installazione. Queste funzioni possono essere usate in combinazione con le funzioni descritte in [Utilizzo delle](working-with-queries.md) query per apportare modifiche effettive in un database.

Le funzioni seguenti creano o rimuovono record:

-   Per creare un nuovo record per un database, chiamare la [**funzione MsiCreateRecord.**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord)
-   Per cancellare i dati da un record, impostare ogni campo su Null chiamando la [**funzione MsiRecordClearData.**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordcleardata)

Le funzioni seguenti compilano i campi di record specificati:

-   Per impostare un record su un numero intero, chiamare [**la funzione MsiRecordSetInteger.**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetinteger)
-   Per impostare un record su una stringa, chiamare la [**funzione MsiRecordSetString.**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa)
-   Per inserire un intero file in un campo di flusso, chiamare la [**funzione MsiRecordSetStream.**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama)

Le funzioni seguenti leggono i valori dai campi di record specificati:

-   Per leggere un valore intero da un campo, chiamare la [**funzione MsiRecordGetInteger.**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetinteger)
-   Per recuperare un valore stringa, chiamare [**la funzione MsiRecordGetString.**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetstringa)
-   Per ottenere un flusso, chiamare la [**funzione MsiRecordReadStream.**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream)
-   Per determinare se un determinato campo di un record è Null, chiamare la [**funzione MsiRecordIsNull.**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordisnull)

Le funzioni seguenti sono funzioni di record in informazioni:

-   Per ottenere il numero di campi contenuti in un record, chiamare la [**funzione MsiRecordGetFieldCount.**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetfieldcount)
-   Per ottenere le dimensioni di un campo, chiamare la [**funzione MsiRecordDataSize.**](/windows/desktop/api/Msiquery/nf-msiquery-msirecorddatasize) Il valore restituito di **MsiRecordDataSize** è sensibile al tipo di campo.

 

 



