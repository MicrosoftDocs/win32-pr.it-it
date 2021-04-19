---
description: Un'applicazione può utilizzare la funzione MsiOpenDatabase per aprire un database di installazione nuovo o esistente (file con estensione msi) o un pacchetto di patch (file con estensione msp). L'applicazione verifica il valore restituito di MsiOpenDatabase prima di usare l'handle di database.
ms.assetid: 54a8d571-ebc3-42d5-bc34-8f29b245b4d8
title: Esempio di database e patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07ff5925fc409352b4c9ed8c1762ba1ad17b261f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311105"
---
# <a name="a-database-and-patch-example"></a><span data-ttu-id="2309d-103">Esempio di database e patch</span><span class="sxs-lookup"><span data-stu-id="2309d-103">A Database and Patch Example</span></span>

<span data-ttu-id="2309d-104">Un'applicazione può utilizzare la funzione [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) per aprire un database di installazione nuovo o esistente (file con estensione msi) o un pacchetto di patch (file con estensione msp). L'applicazione verifica il valore restituito di **MsiOpenDatabase** prima di usare l'handle di database.</span><span class="sxs-lookup"><span data-stu-id="2309d-104">An application can use the [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) function to open a new or existing installation database (.msi file) or patch package (.msp file.) The application checks the return value of **MsiOpenDatabase** before using the database handle.</span></span>

<span data-ttu-id="2309d-105">Negli esempi seguenti vengono usate le variabili di tipo **PMSIHANDLE** definite in MSI. h.</span><span class="sxs-lookup"><span data-stu-id="2309d-105">The following examples use the **PMSIHANDLE** type variables defined in msi.h.</span></span> <span data-ttu-id="2309d-106">È consigliabile usare il tipo **PMSIHANDLE** perché il programma di installazione chiude gli oggetti **PMSIHANDLE** mentre escono dall'ambito, mentre l'applicazione deve chiudere gli oggetti **MSIHANDLE** chiamando [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle).</span><span class="sxs-lookup"><span data-stu-id="2309d-106">It is recommended to use the **PMSIHANDLE** type because the installer closes **PMSIHANDLE** objects as they go out of scope, whereas your application must close **MSIHANDLE** objects by calling [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle).</span></span> <span data-ttu-id="2309d-107">Per ulteriori informazioni, vedere la sezione [utilizzare PMSIHANDLE anziché handle](windows-installer-best-practices.md) nell' [Windows Installer procedure consigliate](windows-installer-best-practices.md).</span><span class="sxs-lookup"><span data-stu-id="2309d-107">For more information see [Use PMSIHANDLE instead of HANDLE](windows-installer-best-practices.md) section in the [Windows Installer Best Practices](windows-installer-best-practices.md).</span></span>

<span data-ttu-id="2309d-108">Nell'esempio seguente viene aperto un database, sample.msi, solo per la lettura.</span><span class="sxs-lookup"><span data-stu-id="2309d-108">The following example opens a database, sample.msi, for reading only.</span></span> <span data-ttu-id="2309d-109">[**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) ha esito positivo solo se sample.msi esiste nella directory c: \\ test.</span><span class="sxs-lookup"><span data-stu-id="2309d-109">[**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) succeeds only if sample.msi exists in the c:\\test directory.</span></span> <span data-ttu-id="2309d-110">Al termine dell'operazione, è possibile usare l'handle di database restituito per eseguire query sui dati nel pacchetto di installazione usando [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) e [**MsiGetSummaryInformation**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsummaryinformationa).</span><span class="sxs-lookup"><span data-stu-id="2309d-110">Upon success, the returned database handle can be used to query the data in the installation package using [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) and [**MsiGetSummaryInformation**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsummaryinformationa).</span></span>


```C++
PMSIHANDLE hDbReadOnly = 0;
UINT uiStatus1 = MsiOpenDatabase(TEXT("c:\\test\\sample.msi"), MSIDBOPEN_READONLY, &hDbReadOnly);
if (ERROR_SUCCESS != uiStatus1)
{
    // process error
    return uiStatus1;
}
```



<span data-ttu-id="2309d-111">Nell'esempio seguente viene aperto il database per la lettura e la scrittura.</span><span class="sxs-lookup"><span data-stu-id="2309d-111">The following example opens the database for reading and writing.</span></span> <span data-ttu-id="2309d-112">Se l'applicazione chiama [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit), vengono salvate tutte le modifiche apportate al database.</span><span class="sxs-lookup"><span data-stu-id="2309d-112">If the application calls [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit), all changes made to the database are saved.</span></span> <span data-ttu-id="2309d-113">Se l'applicazione non chiama **MsiDatabaseCommit**, non viene apportata alcuna modifica al database.</span><span class="sxs-lookup"><span data-stu-id="2309d-113">If the application does not call **MsiDatabaseCommit**, no changes are made to the database.</span></span>


```C++
PMSIHANDLE hDbTransact = 0;
UINT uiStatus2 = MsiOpenDatabase(TEXT("c:\\test\\example.msi"), MSIDBOPEN_TRANSACT, &hDbTransact);
if (ERROR_SUCCESS != uiStatus2)
{
    // process error
    return uiStatus2;
}
```



<span data-ttu-id="2309d-114">Nell'esempio seguente viene preso un database esistente, text.msi e viene creato un nuovo database, newtest.msi.</span><span class="sxs-lookup"><span data-stu-id="2309d-114">The following example takes an existing database, text.msi, and creates a new database, newtest.msi.</span></span> <span data-ttu-id="2309d-115">Tutte le modifiche apportate possono essere salvate nel nuovo database chiamando [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).</span><span class="sxs-lookup"><span data-stu-id="2309d-115">Any changes that are made can be saved in the new database by calling [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).</span></span> <span data-ttu-id="2309d-116">Il database esistente specificato nel parametro *szDatabasePath* è invariato.</span><span class="sxs-lookup"><span data-stu-id="2309d-116">The existing database specified in the *szDatabasePath* parameter is unchanged.</span></span>


```C++
PMSIHANDLE hDbOutput = 0;
UINT uiStatus3 = MsiOpenDatabase(TEXT("c:\\test\\test.msi"), TEXT("c:\\test\\newtest.msi"), &hDbOutput);
if (ERROR_SUCCESS != uiStatus3)
{
    // process error
    return uiStatus3;
}
```



<span data-ttu-id="2309d-117">Nell'esempio seguente viene aperto un pacchetto di patch Windows Installer (file con estensione msp) per la sola lettura.</span><span class="sxs-lookup"><span data-stu-id="2309d-117">The following example opens a Windows Installer patch package (.msp file) for reading only.</span></span> <span data-ttu-id="2309d-118">L'handle di patch restituito può essere usato per determinare gli armadi e trasformare le sottoarchiviazioni incluse nel pacchetto di patch dalle query sulle tabelle [ \_ Streams](-streams-table.md) e [ \_ Storages](-storages-table.md) .</span><span class="sxs-lookup"><span data-stu-id="2309d-118">The returned patch handle can be used to determine the cabinets and transform substorages included in the patch package by queries on the [\_Streams](-streams-table.md) and [\_Storages](-storages-table.md) tables.</span></span>

<span data-ttu-id="2309d-119">**Windows Installer 2,0:** Non supportato.</span><span class="sxs-lookup"><span data-stu-id="2309d-119">**Windows Installer 2.0:** Not supported.</span></span> <span data-ttu-id="2309d-120">A partire da Windows Installer 3,0, l'applicazione può eseguire una query sulla [tabella MsiPatchSequence](msipatchsequence-table.md) presente in un pacchetto di patch che usa le nuove informazioni di sequenziazione delle patch.</span><span class="sxs-lookup"><span data-stu-id="2309d-120">Beginning with Windows Installer 3.0, the application can query the [MsiPatchSequence table](msipatchsequence-table.md) present in a patch package that uses the new patch sequencing information.</span></span>


```C++
PMSIHANDLE hDbPatch = 0;
LPCTSTR szPersistMode = MSIDBOPEN_READONLY + MSIDBOPEN_PATCHFILE;
UINT uiStatus4 = MsiOpenDatabase(TEXT("c:\\test\\sample.msp"), szPersistMode, &hDbPatch);
if (ERROR_SUCCESS != uiStatus4)
{
    // process error
    return uiStatus4;
}
```



 

 



