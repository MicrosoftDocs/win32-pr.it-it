---
description: La \_ tabella SummaryInformation è una tabella speciale utilizzata con il flusso di informazioni di riepilogo. È possibile ottenere o impostare il flusso di informazioni di riepilogo di un database di Windows Installer esportando o importando un file di archivio di testo denominato \_ SummaryInformation. IDT.
ms.assetid: b1b42e03-7a05-46d4-9c42-b87906535adb
title: _SummaryInformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 803b89223db8b6fc8074336109221a8300f7c1ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311114"
---
# <a name="_summaryinformation"></a><span data-ttu-id="eb2df-104">\_SummaryInformation</span><span class="sxs-lookup"><span data-stu-id="eb2df-104">\_SummaryInformation</span></span>

<span data-ttu-id="eb2df-105">La \_ tabella SummaryInformation è una tabella speciale utilizzata con il [flusso di informazioni di riepilogo](summary-information-stream.md).</span><span class="sxs-lookup"><span data-stu-id="eb2df-105">The \_SummaryInformation table is a special table used with the [Summary Information Stream](summary-information-stream.md).</span></span> <span data-ttu-id="eb2df-106">È possibile ottenere o impostare il flusso di informazioni di riepilogo di un database di Windows Installer esportando o importando un [file di archivio di testo](text-archive-files.md) denominato \_ SummaryInformation. IDT.</span><span class="sxs-lookup"><span data-stu-id="eb2df-106">You can get or set the Summary Information Stream of a Windows Installer database by exporting or importing a [text archive file](text-archive-files.md) named \_SummaryInformation.idt.</span></span>

<span data-ttu-id="eb2df-107">Il file con estensione IDT di una \_ tabella SummaryInformation esportata presenta il formato seguente.</span><span class="sxs-lookup"><span data-stu-id="eb2df-107">The .idt file of an exported \_SummaryInformation table has the following format.</span></span>

-   <span data-ttu-id="eb2df-108">La prima riga contiene i nomi delle colonne di tabella separati da tabulazioni: PropertyId e value.</span><span class="sxs-lookup"><span data-stu-id="eb2df-108">The first row contains the table column names separated by tabs: PropertyId and Value.</span></span> <span data-ttu-id="eb2df-109">Per un elenco delle proprietà e dei rispettivi ID (PID), vedere l'argomento relativo al [set di proprietà del flusso di informazioni di riepilogo](summary-information-stream-property-set.md) .</span><span class="sxs-lookup"><span data-stu-id="eb2df-109">See the [Summary Information Stream Property Set](summary-information-stream-property-set.md) topic for a list of the properties and their ids (PID).</span></span>
-   <span data-ttu-id="eb2df-110">La seconda riga contiene le definizioni di colonna separate da tabulazioni.</span><span class="sxs-lookup"><span data-stu-id="eb2df-110">The second row contains the column definitions separated by tabs.</span></span> <span data-ttu-id="eb2df-111">Le definizioni di colonna vengono specificate in modo analogo al formato del file di [Archivio](archive-file-format.md)Basic. IDT.</span><span class="sxs-lookup"><span data-stu-id="eb2df-111">The column definitions are specified in the same way as in the basic .idt [archive file format](archive-file-format.md).</span></span> <span data-ttu-id="eb2df-112">La colonna PropertyId può essere un valore short integer non nullable.</span><span class="sxs-lookup"><span data-stu-id="eb2df-112">The PropertyId column can be a non-nullable short integer.</span></span> <span data-ttu-id="eb2df-113">La colonna valore può essere una stringa localizzabile non nullable di 255 caratteri.</span><span class="sxs-lookup"><span data-stu-id="eb2df-113">The Value column can be a non-nullable localizable string 255 characters long.</span></span>
-   <span data-ttu-id="eb2df-114">La terza riga è il nome della tabella e il nome della colonna chiave primaria separati da tabulazioni: \_ SummaryInformation e PropertyId.</span><span class="sxs-lookup"><span data-stu-id="eb2df-114">The third row is the table name and the primary key column name separated by tabs: \_SummaryInformation and PropertyId.</span></span>
-   <span data-ttu-id="eb2df-115">Le righe rimanenti nel file rappresentano il PID e il valore associato, separati da tabulazioni.</span><span class="sxs-lookup"><span data-stu-id="eb2df-115">The remaining rows in the file represent the PID and associated value, separated by tabs.</span></span> <span data-ttu-id="eb2df-116">La data e l'ora in \_ SummaryInformation sono nel formato: aaaa/mm/gg hh:: mm:: SS.</span><span class="sxs-lookup"><span data-stu-id="eb2df-116">Date and time in\_SummaryInformation are in the format: YYYY/MM/DD hh::mm::ss.</span></span> <span data-ttu-id="eb2df-117">Ad esempio, 1999/03/22 15:25:45.</span><span class="sxs-lookup"><span data-stu-id="eb2df-117">For example, 1999/03/22 15:25:45.</span></span>

<span data-ttu-id="eb2df-118">Di seguito è riportato un esempio del [flusso di informazioni di riepilogo](summary-information-stream.md) di un database in formato IDT.</span><span class="sxs-lookup"><span data-stu-id="eb2df-118">The following is an example of the [Summary Information Stream](summary-information-stream.md) of a database in .idt format.</span></span>

``` syntax
PropertyId   Value
i2  l255
_SummaryInformation PropertyId
1   1252
2   Installation Database
3   Internal Quick Test
4   Microsoft Corporation
5   Installer,MSI,Database
6   Installer Internal Release Quick Test
7   Intel;1033
9   {00000002-0001-0000-0000-624474736554}
12  1999/06/21
14  110
15  1
18  Windows Installer
```

<span data-ttu-id="eb2df-119">Quando si utilizza [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) o il metodo [Import](database-import.md) dell'oggetto di [**database**](database-object.md) per importare una tabella di archivio di testo denominata \_ SummaryInformation in un database del programma di installazione, è necessario scrivere il flusso "05SummaryInformation" nel database.</span><span class="sxs-lookup"><span data-stu-id="eb2df-119">When you use [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta) or the [Import](database-import.md) method of the [**Database**](database-object.md) object to import a text archive table named \_SummaryInformation into an installer database, you write the "05SummaryInformation" stream in the database.</span></span>

 

 



