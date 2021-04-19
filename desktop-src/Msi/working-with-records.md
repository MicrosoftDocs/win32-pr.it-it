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
# <a name="working-with-records"></a><span data-ttu-id="0ba7f-104">Utilizzo dei record</span><span class="sxs-lookup"><span data-stu-id="0ba7f-104">Working with Records</span></span>

<span data-ttu-id="0ba7f-105">Il programma di installazione fornisce funzioni che modificano i record in un database di installazione.</span><span class="sxs-lookup"><span data-stu-id="0ba7f-105">The installer supplies functions that manipulate the records in an installation database.</span></span> <span data-ttu-id="0ba7f-106">Queste funzioni possono essere utilizzate insieme alle funzioni descritte in utilizzo delle [query](working-with-queries.md) per apportare modifiche effettive in un database.</span><span class="sxs-lookup"><span data-stu-id="0ba7f-106">These functions can be used in conjunction with the functions described in [Working with Queries](working-with-queries.md) to make actual changes in a database.</span></span>

<span data-ttu-id="0ba7f-107">Le funzioni seguenti creano o rimuovono i record:</span><span class="sxs-lookup"><span data-stu-id="0ba7f-107">The following functions create or remove records:</span></span>

-   <span data-ttu-id="0ba7f-108">Per creare un nuovo record per un database, chiamare la funzione [**MsiCreateRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord) .</span><span class="sxs-lookup"><span data-stu-id="0ba7f-108">To create a new record for a database, call the [**MsiCreateRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord) function.</span></span>
-   <span data-ttu-id="0ba7f-109">Per cancellare i dati da un record, impostare ogni campo su null chiamando la funzione [**MsiRecordClearData**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordcleardata) .</span><span class="sxs-lookup"><span data-stu-id="0ba7f-109">To clear data from a record, set each field to null by calling the [**MsiRecordClearData**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordcleardata) function.</span></span>

<span data-ttu-id="0ba7f-110">Le funzioni seguenti riempiono i campi di record specificati:</span><span class="sxs-lookup"><span data-stu-id="0ba7f-110">The following functions fill specified fields of records:</span></span>

-   <span data-ttu-id="0ba7f-111">Per impostare un record su un numero intero, chiamare la funzione [**MsiRecordSetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetinteger) .</span><span class="sxs-lookup"><span data-stu-id="0ba7f-111">To set a record to an integer, call the [**MsiRecordSetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetinteger) function.</span></span>
-   <span data-ttu-id="0ba7f-112">Per impostare un record su una stringa, chiamare la funzione [**MsiRecordSetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa) .</span><span class="sxs-lookup"><span data-stu-id="0ba7f-112">To set a record to a string, call the [**MsiRecordSetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstringa) function.</span></span>
-   <span data-ttu-id="0ba7f-113">Per inserire un intero file in un campo del flusso, chiamare la funzione [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) .</span><span class="sxs-lookup"><span data-stu-id="0ba7f-113">To insert an entire file into a stream field, call the [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) function.</span></span>

<span data-ttu-id="0ba7f-114">Le funzioni seguenti leggono i valori dei campi di record specificati:</span><span class="sxs-lookup"><span data-stu-id="0ba7f-114">The following functions read values from specified fields of records:</span></span>

-   <span data-ttu-id="0ba7f-115">Per leggere un valore integer da un campo, chiamare la funzione [**MsiRecordGetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetinteger) .</span><span class="sxs-lookup"><span data-stu-id="0ba7f-115">To read an integer value from a field, call the [**MsiRecordGetInteger**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetinteger) function.</span></span>
-   <span data-ttu-id="0ba7f-116">Per recuperare un valore stringa, chiamare la funzione [**MsiRecordGetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetstringa) .</span><span class="sxs-lookup"><span data-stu-id="0ba7f-116">To retrieve a string value, call the [**MsiRecordGetString**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetstringa) function.</span></span>
-   <span data-ttu-id="0ba7f-117">Per ottenere un flusso, chiamare la funzione [**MsiRecordReadStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream) .</span><span class="sxs-lookup"><span data-stu-id="0ba7f-117">To obtain a stream, call the [**MsiRecordReadStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordreadstream) function.</span></span>
-   <span data-ttu-id="0ba7f-118">Per determinare se un determinato campo di un record è null, chiamare la funzione [**MsiRecordIsNull**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordisnull) .</span><span class="sxs-lookup"><span data-stu-id="0ba7f-118">To determine if a particular field of a record is null, call the [**MsiRecordIsNull**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordisnull) function.</span></span>

<span data-ttu-id="0ba7f-119">Le funzioni seguenti sono funzioni di record informativi:</span><span class="sxs-lookup"><span data-stu-id="0ba7f-119">The following functions are informational record functions:</span></span>

-   <span data-ttu-id="0ba7f-120">Per ottenere il numero di campi contenuti in un record, chiamare la funzione [**MsiRecordGetFieldCount**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetfieldcount) .</span><span class="sxs-lookup"><span data-stu-id="0ba7f-120">To get the number of fields a record contains, call the [**MsiRecordGetFieldCount**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetfieldcount) function.</span></span>
-   <span data-ttu-id="0ba7f-121">Per ottenere le dimensioni di un campo, chiamare la funzione [**MsiRecordDataSize**](/windows/desktop/api/Msiquery/nf-msiquery-msirecorddatasize) .</span><span class="sxs-lookup"><span data-stu-id="0ba7f-121">To get the size of a field, call the [**MsiRecordDataSize**](/windows/desktop/api/Msiquery/nf-msiquery-msirecorddatasize) function.</span></span> <span data-ttu-id="0ba7f-122">Il valore restituito di **MsiRecordDataSize** è sensibile al tipo di campo.</span><span class="sxs-lookup"><span data-stu-id="0ba7f-122">The return value of **MsiRecordDataSize** is sensitive to the field type.</span></span>

 

 



