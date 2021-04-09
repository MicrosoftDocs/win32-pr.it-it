---
description: '\\Client HKLM Software \\ Microsoft \\ MSSQLSERVER \\ .'
ms.assetid: d6eb774b-d7ae-4f51-9947-90fb176e9acf
title: ConnectTo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 581b1f77fc90bca467e90a3c3b7f407b8ba6d33d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049161"
---
# <a name="connectto"></a><span data-ttu-id="c3f4a-103">ConnectTo</span><span class="sxs-lookup"><span data-stu-id="c3f4a-103">ConnectTo</span></span>

<span data-ttu-id="c3f4a-104">**\\Client HKLM Software \\ Microsoft \\ MSSQLSERVER \\**</span><span class="sxs-lookup"><span data-stu-id="c3f4a-104">**HKLM\\SOFTWARE\\Microsoft\\MSSQLServer\\Client**</span></span>

## <a name="description"></a><span data-ttu-id="c3f4a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c3f4a-105">Description</span></span>

<span data-ttu-id="c3f4a-106">La sottochiave **ConnectTo** archivia le informazioni di connessione per i client basati su Windows che si connettono alle istanze del motore di database Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c3f4a-106">The **ConnectTo** subkey stores connection information for Windows-based clients that connect to instances of the Microsoft SQL Server database engine.</span></span> <span data-ttu-id="c3f4a-107">Le voci del registro di sistema in questa sottochiave sono di tipo di dati REG \_ SZ e i relativi valori specificano il Net-Library da usare per la connessione all'istanza di, nonché qualsiasi parametro specifico della rete.</span><span class="sxs-lookup"><span data-stu-id="c3f4a-107">Registry entries in this subkey are of data type REG\_SZ, and their values specify the Net-Library to use for connecting to the instance, as well as any network-specific parameters.</span></span>

<span data-ttu-id="c3f4a-108">Le informazioni di connessione archiviate in questa sottochiave vengono lette dal provider OLE DB per SQL Server, dal driver ODBC SQL Server o dal SQL Server DB-Library libreria a collegamento dinamico (DLL).</span><span class="sxs-lookup"><span data-stu-id="c3f4a-108">The connection information stored in this subkey is read by the OLE DB Provider for SQL Server, the SQL Server ODBC driver, or the SQL Server DB-Library dynamic-link library (DLL).</span></span>

## <a name="change-method"></a><span data-ttu-id="c3f4a-109">Cambia metodo</span><span class="sxs-lookup"><span data-stu-id="c3f4a-109">Change Method</span></span>

<span data-ttu-id="c3f4a-110">Non è necessario modificare le voci in questa sottochiave utilizzando l'editor del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="c3f4a-110">You should not modify entries in this subkey by using the registry editor.</span></span> <span data-ttu-id="c3f4a-111">Utilizzare l'utilità di rete client di SQL Server per configurare il nome del server e le informazioni di connessione.</span><span class="sxs-lookup"><span data-stu-id="c3f4a-111">Use the SQL Server Client Network Utility to configure server name and connection information.</span></span> <span data-ttu-id="c3f4a-112">Per altre istruzioni, vedere SQL Server Guida dell'utilità di rete client.</span><span class="sxs-lookup"><span data-stu-id="c3f4a-112">See SQL Server Client Network Utility Help for further instructions.</span></span>

## <a name="notes"></a><span data-ttu-id="c3f4a-113">Note</span><span class="sxs-lookup"><span data-stu-id="c3f4a-113">Notes</span></span>

-   <span data-ttu-id="c3f4a-114">La sottochiave **ConnectTo** viene utilizzata dal provider OLE DB per SQL Server, dal Driver ODBC SQL Server e dalla DLL di DB-Library SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c3f4a-114">The **ConnectTo** subkey is used by the OLE DB Provider for SQL Server, the SQL Server ODBC Driver, and the SQL Server DB-Library DLL.</span></span> <span data-ttu-id="c3f4a-115">Le voci della sottochiave identificano i Net-Library questi componenti API (Data Access Application Programming Interface) chiamano.</span><span class="sxs-lookup"><span data-stu-id="c3f4a-115">Entries in this subkey identify which Net-Library these data access application programming interface (API) components call.</span></span>
-   <span data-ttu-id="c3f4a-116">Net-Libraries sono componenti SQL Server che proteggono i componenti dell'API di accesso ai dati dai dettagli dell'utilizzo di metodi di comunicazione interprocesso (IPC) diversi per comunicare con un'istanza del motore di database SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c3f4a-116">Net-Libraries are SQL Server components that shield the data access API components from the details of using different Interprocess Communication (IPC) methods to communicate with an instancess of the SQL Server database engine.</span></span>
-   <span data-ttu-id="c3f4a-117">L'aggiornamento errato della sottochiave **ConnectTo** potrebbe impedire la corretta connessione delle applicazioni a un'istanza del motore di database SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c3f4a-117">Improperly updating the **ConnectTo** subkey might prevent applications from successfully connecting to an instance of the SQL Server database engine.</span></span>

 

 



