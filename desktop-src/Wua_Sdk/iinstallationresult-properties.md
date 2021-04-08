---
description: L'interfaccia IInstallationResult definisce le proprietà seguenti.
ms.assetid: bd6cd5ae-2e43-4ac3-8ce7-ac80b7fc5cb8
title: Proprietà di IInstallationResult
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78783b6758ab30d6a77c07cd71111486f3a7343e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049546"
---
# <a name="iinstallationresult-properties"></a><span data-ttu-id="33705-103">Proprietà di IInstallationResult</span><span class="sxs-lookup"><span data-stu-id="33705-103">IInstallationResult Properties</span></span>

<span data-ttu-id="33705-104">L'interfaccia [**IInstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationresult) definisce le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="33705-104">The [**IInstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationresult) interface defines the following properties.</span></span>



| <span data-ttu-id="33705-105">Proprietà</span><span class="sxs-lookup"><span data-stu-id="33705-105">Property</span></span>                                                     | <span data-ttu-id="33705-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="33705-106">Description</span></span>                                                                                                                            |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="33705-107">**HResult**</span><span class="sxs-lookup"><span data-stu-id="33705-107">**HResult**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationresult-get_hresult)               | <span data-ttu-id="33705-108">Ottiene il valore **HRESULT** dell'eccezione, se presente, generato durante l'installazione.</span><span class="sxs-lookup"><span data-stu-id="33705-108">Gets the **HRESULT** of the exception, if any, that is raised during the installation.</span></span>                                                 |
| [<span data-ttu-id="33705-109">**RebootRequired**</span><span class="sxs-lookup"><span data-stu-id="33705-109">**RebootRequired**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationresult-get_rebootrequired) | <span data-ttu-id="33705-110">Ottiene un valore booleano che indica se è necessario riavviare il computer per completare l'installazione o la disinstallazione di un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="33705-110">Gets a Boolean value that indicates whether you must restart the computer to complete the installation or uninstallation of an update.</span></span> |
| [<span data-ttu-id="33705-111">**ResultCode**</span><span class="sxs-lookup"><span data-stu-id="33705-111">**ResultCode**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationresult-get_resultcode)         | <span data-ttu-id="33705-112">Ottiene un valore [**OperationResultCode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) che specifica il risultato di un'operazione su un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="33705-112">Gets an [**OperationResultCode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) value that specifies the result of an operation on an update.</span></span>               |



 

 

 



