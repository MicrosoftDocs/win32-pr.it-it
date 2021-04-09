---
description: Prima di poter usare un log di file, è necessario chiamare SetupInitializeFileLog per aprirlo o crearlo. Quando si chiama questa funzione, è possibile specificare i flag per creare o sovrascrivere un log di file, aprire il registro di sistema o aprire un log di file come di sola lettura.
ms.assetid: 7ab133f6-2088-4bca-bf24-d3dcb29376a1
title: Uso del file di log
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf7f1e3d27ba7d42d448a1eac48d60246c2b40db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968750"
---
# <a name="using-the-file-log"></a><span data-ttu-id="fb0c8-104">Uso del file di log</span><span class="sxs-lookup"><span data-stu-id="fb0c8-104">Using the File Log</span></span>

<span data-ttu-id="fb0c8-105">Prima di poter usare un log di file, è necessario chiamare [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga) per aprirlo o crearlo.</span><span class="sxs-lookup"><span data-stu-id="fb0c8-105">Before you can use a file log, you must call [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga) to open or create it.</span></span> <span data-ttu-id="fb0c8-106">Quando si chiama questa funzione, è possibile specificare i flag per creare o sovrascrivere un log di file, aprire il registro di sistema o aprire un log di file come di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="fb0c8-106">When you call this function, you can specify flags to create or overwrite a file log, open the system log, or open a file log as read-only.</span></span>

<span data-ttu-id="fb0c8-107">Dopo che [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga) restituisce un handle a un log file, è possibile aggiungere una voce chiamando [**SetupLogFile**](/windows/desktop/api/Setupapi/nf-setupapi-setuplogfilea), eliminare una voce chiamando [**SetupRemoveFileLogEntry**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefilelogentrya)o recuperare informazioni su un determinato file in un log file chiamando [**SetupQueryFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryfileloga).</span><span class="sxs-lookup"><span data-stu-id="fb0c8-107">After [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga) returns a handle to a file log, you can add an entry by calling [**SetupLogFile**](/windows/desktop/api/Setupapi/nf-setupapi-setuplogfilea), delete an entry by calling [**SetupRemoveFileLogEntry**](/windows/desktop/api/Setupapi/nf-setupapi-setupremovefilelogentrya), or retrieve information about a particular file in a file log by calling [**SetupQueryFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupqueryfileloga).</span></span>

<span data-ttu-id="fb0c8-108">Quando il log del file non è più necessario, [**SetupTerminateFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupterminatefilelog) deve essere chiamato per rilasciare le risorse allocate durante la chiamata a [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga).</span><span class="sxs-lookup"><span data-stu-id="fb0c8-108">When the file log is no longer needed, [**SetupTerminateFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupterminatefilelog) should be called to release the resources allocated during the call to [**SetupInitializeFileLog**](/windows/desktop/api/Setupapi/nf-setupapi-setupinitializefileloga).</span></span>

 

 



