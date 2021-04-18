---
description: L'interfaccia IUpdateServiceRegistration definisce le proprietà seguenti.
ms.assetid: 2bcde8b4-7bff-4887-8080-89da817afb5f
title: Proprietà di IUpdateServiceRegistration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 716c06f2fc8ed9a7ce12542a09440cf0ec0b5c49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305838"
---
# <a name="iupdateserviceregistration-properties"></a><span data-ttu-id="c9517-103">Proprietà di IUpdateServiceRegistration</span><span class="sxs-lookup"><span data-stu-id="c9517-103">IUpdateServiceRegistration Properties</span></span>

<span data-ttu-id="c9517-104">L'interfaccia **IUpdateServiceRegistration** definisce le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="c9517-104">The **IUpdateServiceRegistration** interface defines the following properties.</span></span>



| <span data-ttu-id="c9517-105">Proprietà</span><span class="sxs-lookup"><span data-stu-id="c9517-105">Property</span></span>                                                                                      | <span data-ttu-id="c9517-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9517-106">Description</span></span>                                                                                                                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c9517-107">**IsPendingRegistrationWithAU**</span><span class="sxs-lookup"><span data-stu-id="c9517-107">**IsPendingRegistrationWithAU**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateserviceregistration-get_ispendingregistrationwithau) | <span data-ttu-id="c9517-108">Ottiene un valore booleano che indica se il servizio verrà registrato anche con Aggiornamenti automatici, quando viene aggiunto.</span><span class="sxs-lookup"><span data-stu-id="c9517-108">Gets a Boolean value that indicates whether the service will also be registered with Automatic Updates, when added.</span></span>                                  |
| [<span data-ttu-id="c9517-109">**RegistrationState**</span><span class="sxs-lookup"><span data-stu-id="c9517-109">**RegistrationState**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateserviceregistration-get_registrationstate)                     | <span data-ttu-id="c9517-110">Ottiene un valore [**UpdateServiceRegistrationState**](/windows/win32/api/wuapi/ne-wuapi-updateserviceregistrationstate) che indica lo stato corrente della registrazione del servizio.</span><span class="sxs-lookup"><span data-stu-id="c9517-110">Gets an [**UpdateServiceRegistrationState**](/windows/win32/api/wuapi/ne-wuapi-updateserviceregistrationstate) value that indicates the current state of the service registration.</span></span> |
| [<span data-ttu-id="c9517-111">**Servizio**</span><span class="sxs-lookup"><span data-stu-id="c9517-111">**Service**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateserviceregistration-get_service)                                         | <span data-ttu-id="c9517-112">Ottiene un puntatore a un'interfaccia [**IUpdateService2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice2) .</span><span class="sxs-lookup"><span data-stu-id="c9517-112">Gets a pointer to an [**IUpdateService2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice2) interface.</span></span> <span data-ttu-id="c9517-113">Questa proprietà è la proprietà predefinita.</span><span class="sxs-lookup"><span data-stu-id="c9517-113">This property is the default property.</span></span>                                    |



 

 

 



