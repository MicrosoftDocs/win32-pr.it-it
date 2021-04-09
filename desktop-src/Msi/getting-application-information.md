---
description: Il database del prodotto contiene informazioni su un prodotto. Per ulteriori informazioni su come ottenere informazioni sui prodotti con funzioni di enumerazione, vedere Inizializzazione di un'applicazione.
ms.assetid: 528c915c-296c-4620-8105-0b5d543e56a5
title: Recupero delle informazioni sull'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2dce842f057efb65b6d0db3ad0407a19bf08435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967021"
---
# <a name="getting-application-information"></a><span data-ttu-id="441ca-104">Recupero delle informazioni sull'applicazione</span><span class="sxs-lookup"><span data-stu-id="441ca-104">Getting Application Information</span></span>

<span data-ttu-id="441ca-105">Il database del prodotto contiene informazioni su un prodotto.</span><span class="sxs-lookup"><span data-stu-id="441ca-105">The product database contains information about a product.</span></span> <span data-ttu-id="441ca-106">Per ulteriori informazioni su come ottenere informazioni sui prodotti con funzioni di enumerazione, vedere [inizializzazione di un'applicazione](initializing-an-application.md).</span><span class="sxs-lookup"><span data-stu-id="441ca-106">For more information on obtaining product information with enumeration functions, see [Initializing an Application](initializing-an-application.md).</span></span>

<span data-ttu-id="441ca-107">**Per ottenere informazioni sul prodotto**</span><span class="sxs-lookup"><span data-stu-id="441ca-107">**To get product information**</span></span>

1.  <span data-ttu-id="441ca-108">Verificare che un prodotto sia installato chiamando la funzione [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea) .</span><span class="sxs-lookup"><span data-stu-id="441ca-108">Verify that a product is installed by calling the [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea) function.</span></span>
2.  <span data-ttu-id="441ca-109">Aprire il database e ottenere un handle per esso chiamando la funzione [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) .</span><span class="sxs-lookup"><span data-stu-id="441ca-109">Open the database and obtain a handle to it by calling the [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) function.</span></span>

    <span data-ttu-id="441ca-110">Se il database è incluso in un pacchetto di installazione, chiamare la funzione [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea) .</span><span class="sxs-lookup"><span data-stu-id="441ca-110">If the database is contained in an installation package, call the [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea) function.</span></span>

3.  <span data-ttu-id="441ca-111">Utilizzare l'handle aperto per ottenere le proprietà del prodotto con la funzione [**MsiGetProductProperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya) e per ottenere informazioni descrittive sulle funzionalità con la funzione [**MsiGetFeatureInfo**](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa) .</span><span class="sxs-lookup"><span data-stu-id="441ca-111">Use the open handle to obtain product properties with the [**MsiGetProductProperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya) function, and to obtain descriptive feature information with the [**MsiGetFeatureInfo**](/windows/desktop/api/Msi/nf-msi-msigetfeatureinfoa) function.</span></span>

    <span data-ttu-id="441ca-112">Se si desidera ottenere informazioni sul prodotto utilizzando il codice del prodotto, anziché utilizzare l'handle di database aperto, chiamare la funzione [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa) anziché [**MsiGetProductProperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya).</span><span class="sxs-lookup"><span data-stu-id="441ca-112">If you want to obtain product information using the product code, rather than using the open database handle, call the [**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa) function instead of [**MsiGetProductProperty**](/windows/desktop/api/Msi/nf-msi-msigetproductpropertya).</span></span>

4.  <span data-ttu-id="441ca-113">Chiudere un handle di installazione aperto chiamando la funzione [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle) .</span><span class="sxs-lookup"><span data-stu-id="441ca-113">Close an open installation handle by calling the [**MsiCloseHandle**](/windows/desktop/api/Msi/nf-msi-msiclosehandle) function.</span></span>

    <span data-ttu-id="441ca-114">La funzione [**MsiCloseAllHandles**](/windows/desktop/api/Msi/nf-msi-msicloseallhandles) è una funzione di diagnostica e non deve essere usata per chiudere gli handle che si sa essere aperti.</span><span class="sxs-lookup"><span data-stu-id="441ca-114">The [**MsiCloseAllHandles**](/windows/desktop/api/Msi/nf-msi-msicloseallhandles) function is a diagnostic function and should not be used to close handles you know to be open.</span></span> <span data-ttu-id="441ca-115">È accettabile chiamare la funzione **MsiCloseAllHandles** quando l'applicazione viene chiusa per assicurarsi che tutti gli handle siano stati chiusi.</span><span class="sxs-lookup"><span data-stu-id="441ca-115">It is acceptable to call the **MsiCloseAllHandles** function when the application closes to ensure that all handles have been closed.</span></span>

 

 



