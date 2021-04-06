---
description: "Se si usa l'API COM per WMI per recuperare o archiviare le informazioni sulle classi localizzate, specificare le impostazioni locali nel parametro strLocale per l'interfaccia IWbemLocator:: ConnectServer."
ms.assetid: 940a7bd9-c2ea-4deb-b5d8-207a0ce7a616
ms.tgt_platform: multiple
title: Recupero di classi modificate tramite l'API COM per WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0178b0b99de2b666e2f497074a02b02c49ba400
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759761"
---
# <a name="retrieving-amended-classes-using-the-com-api-for-wmi"></a><span data-ttu-id="08dec-103">Recupero di classi modificate tramite l'API COM per WMI</span><span class="sxs-lookup"><span data-stu-id="08dec-103">Retrieving Amended Classes Using the COM API for WMI</span></span>

<span data-ttu-id="08dec-104">Se si usa l'API COM per WMI per recuperare o archiviare le informazioni sulle classi localizzate, specificare le impostazioni locali nel parametro *strLocale* per l'interfaccia [**IWbemLocator:: ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) .</span><span class="sxs-lookup"><span data-stu-id="08dec-104">If you are using the COM API for WMI to retrieve or store localized class information, specify the locale in the *strLocale* parameter to the [**IWbemLocator::ConnectServer**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) interface.</span></span> <span data-ttu-id="08dec-105">Durante la lettura o la scrittura di classi modificate, indicare che si desidera utilizzare le definizioni di classe localizzate specificando \_ il flag WBEM \_ utilizzare \_ \_ i qualificatori modificati come flag per il parametro *iFlags* .</span><span class="sxs-lookup"><span data-stu-id="08dec-105">When reading or writing amended classes, indicate that you want to use localized class definitions by specifying WBEM\_FLAG\_USE\_AMENDED\_QUALIFIERS as a flag for the *iFlags* parameter.</span></span>

<span data-ttu-id="08dec-106">Nella tabella seguente sono elencate le versioni sincrone e asincrone dei metodi che usano il flag WBEM usare il flag di \_ \_ \_ \_ qualificatori modificati.</span><span class="sxs-lookup"><span data-stu-id="08dec-106">The following table lists the synchronous and asynchronous versions of the methods that use the WBEM\_FLAG\_USE\_AMENDED\_QUALIFIERS flag.</span></span>



| <span data-ttu-id="08dec-107">Metodo sincrono</span><span class="sxs-lookup"><span data-stu-id="08dec-107">Synchronous Method</span></span>                                                            | <span data-ttu-id="08dec-108">Metodo asincrono</span><span class="sxs-lookup"><span data-stu-id="08dec-108">Asynchronous Method</span></span>                                                                     |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="08dec-109">**IWbemServices:: CreateClassEnum**</span><span class="sxs-lookup"><span data-stu-id="08dec-109">**IWbemServices::CreateClassEnum**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum)       | [<span data-ttu-id="08dec-110">**IWbemServices:: CreateClassEnumAsync**</span><span class="sxs-lookup"><span data-stu-id="08dec-110">**IWbemServices::CreateClassEnumAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)       |
| [<span data-ttu-id="08dec-111">**IWbemServices:: CreateInstanceEnum**</span><span class="sxs-lookup"><span data-stu-id="08dec-111">**IWbemServices::CreateInstanceEnum**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) | [<span data-ttu-id="08dec-112">**IWbemServices:: CreateInstanceEnumAsync**</span><span class="sxs-lookup"><span data-stu-id="08dec-112">**IWbemServices::CreateInstanceEnumAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) |
| [<span data-ttu-id="08dec-113">**IWbemServices:: ExecQuery**</span><span class="sxs-lookup"><span data-stu-id="08dec-113">**IWbemServices::ExecQuery**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)                   | [<span data-ttu-id="08dec-114">**IWbemServices:: ExecQueryAsync**</span><span class="sxs-lookup"><span data-stu-id="08dec-114">**IWbemServices::ExecQueryAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)                   |
| [<span data-ttu-id="08dec-115">**IWbemServices:: GetObject**</span><span class="sxs-lookup"><span data-stu-id="08dec-115">**IWbemServices::GetObject**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)                   | [<span data-ttu-id="08dec-116">**IWbemServices:: GetObjectAsync**</span><span class="sxs-lookup"><span data-stu-id="08dec-116">**IWbemServices::GetObjectAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)                   |
| [<span data-ttu-id="08dec-117">**IWbemServices::P utClass**</span><span class="sxs-lookup"><span data-stu-id="08dec-117">**IWbemServices::PutClass**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass)                     | [<span data-ttu-id="08dec-118">**IWbemServices::P utClassAsync**</span><span class="sxs-lookup"><span data-stu-id="08dec-118">**IWbemServices::PutClassAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync)                     |
| [<span data-ttu-id="08dec-119">**IWbemServices::P utInstance**</span><span class="sxs-lookup"><span data-stu-id="08dec-119">**IWbemServices::PutInstance**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance)               | [<span data-ttu-id="08dec-120">**IWbemServices::P utInstanceAsync**</span><span class="sxs-lookup"><span data-stu-id="08dec-120">**IWbemServices::PutInstanceAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)               |



 

 

 



