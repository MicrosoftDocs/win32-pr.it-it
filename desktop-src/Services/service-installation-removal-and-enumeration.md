---
description: Un programma di configurazione utilizza la funzione CreateService per installare un nuovo servizio nel database SCM.
ms.assetid: 554b9983-4e49-4b11-b420-a4754123d854
title: Installazione, rimozione ed enumerazione del servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1069bba094205efd3257063a89c74326b2806455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751058"
---
# <a name="service-installation-removal-and-enumeration"></a><span data-ttu-id="45813-103">Installazione, rimozione ed enumerazione del servizio</span><span class="sxs-lookup"><span data-stu-id="45813-103">Service Installation, Removal, and Enumeration</span></span>

<span data-ttu-id="45813-104">Un programma di configurazione utilizza la funzione [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) per installare un nuovo servizio nel database SCM.</span><span class="sxs-lookup"><span data-stu-id="45813-104">A configuration program uses the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function to install a new service in the SCM database.</span></span> <span data-ttu-id="45813-105">Questa funzione specifica il nome del servizio e fornisce le informazioni di configurazione archiviate nel database.</span><span class="sxs-lookup"><span data-stu-id="45813-105">This function specifies the name of the service and provides configuration information that is stored in the database.</span></span> <span data-ttu-id="45813-106">Per una descrizione delle informazioni archiviate nel database per ogni servizio, vedere [database of installato Services](database-of-installed-services.md).</span><span class="sxs-lookup"><span data-stu-id="45813-106">For a description of the information stored in the database for each service, see [Database of Installed Services](database-of-installed-services.md).</span></span> <span data-ttu-id="45813-107">Per il codice di esempio, vedere [installazione di un servizio](installing-a-service.md).</span><span class="sxs-lookup"><span data-stu-id="45813-107">For sample code, see [Installing a Service](installing-a-service.md).</span></span>

<span data-ttu-id="45813-108">Un programma di configurazione utilizza la funzione [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) per rimuovere un servizio installato dal database.</span><span class="sxs-lookup"><span data-stu-id="45813-108">A configuration program uses the [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) function to remove an installed service from the database.</span></span> <span data-ttu-id="45813-109">Per ulteriori informazioni, vedere [eliminazione di un servizio](deleting-a-service.md).</span><span class="sxs-lookup"><span data-stu-id="45813-109">For more information, see [Deleting a Service](deleting-a-service.md).</span></span>

<span data-ttu-id="45813-110">Per ottenere il nome del servizio, chiamare la funzione [**GetServiceKeyName**](/windows/desktop/api/Winsvc/nf-winsvc-getservicekeynamea) .</span><span class="sxs-lookup"><span data-stu-id="45813-110">To obtain the service name, call the [**GetServiceKeyName**](/windows/desktop/api/Winsvc/nf-winsvc-getservicekeynamea) function.</span></span> <span data-ttu-id="45813-111">Il nome visualizzato del servizio, usato nell'applet del pannello di controllo dei servizi, può essere ottenuto chiamando la funzione [**GetServiceDisplayName**](/windows/desktop/api/Winsvc/nf-winsvc-getservicedisplaynamea) .</span><span class="sxs-lookup"><span data-stu-id="45813-111">The service display name, used in the Services control panel applet, can be obtained by calling the [**GetServiceDisplayName**](/windows/desktop/api/Winsvc/nf-winsvc-getservicedisplaynamea) function.</span></span>

<span data-ttu-id="45813-112">Un programma di configurazione del servizio può usare la funzione [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) per enumerare tutti i servizi e i relativi stati.</span><span class="sxs-lookup"><span data-stu-id="45813-112">A service configuration program can use the [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) function to enumerate all services and their statuses.</span></span> <span data-ttu-id="45813-113">Può inoltre utilizzare la funzione [**EnumDependentServices**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa) per enumerare i servizi che dipendono da un oggetto servizio specificato.</span><span class="sxs-lookup"><span data-stu-id="45813-113">It can also use the [**EnumDependentServices**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa) function to enumerate which services are dependent on a specified service object.</span></span>

 

 



