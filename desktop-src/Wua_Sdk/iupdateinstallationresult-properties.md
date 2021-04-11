---
description: L'interfaccia IUpdateInstallationResult definisce le proprietà seguenti.
ms.assetid: 7e8f7125-f89b-416f-bcc5-422eecabe0c4
title: Proprietà di IUpdateInstallationResult
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27b2e2792215d8d927d6e6157c82e37193e74d2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226224"
---
# <a name="iupdateinstallationresult-properties"></a><span data-ttu-id="590c8-103">Proprietà di IUpdateInstallationResult</span><span class="sxs-lookup"><span data-stu-id="590c8-103">IUpdateInstallationResult Properties</span></span>

<span data-ttu-id="590c8-104">L'interfaccia [**IUpdateInstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstallationresult) definisce le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="590c8-104">The [**IUpdateInstallationResult**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateinstallationresult) interface defines the following properties.</span></span>



| <span data-ttu-id="590c8-105">Proprietà</span><span class="sxs-lookup"><span data-stu-id="590c8-105">Property</span></span>                                                           | <span data-ttu-id="590c8-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="590c8-106">Description</span></span>                                                                                                                       |
|--------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="590c8-107">**HResult**</span><span class="sxs-lookup"><span data-stu-id="590c8-107">**HResult**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_hresult)               | <span data-ttu-id="590c8-108">Ottiene il valore dell'eccezione **HRESULT** generato durante l'operazione su un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="590c8-108">Gets the **HRESULT** exception value that is raised during the operation on an update.</span></span>                                            |
| [<span data-ttu-id="590c8-109">**RebootRequired**</span><span class="sxs-lookup"><span data-stu-id="590c8-109">**RebootRequired**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_rebootrequired) | <span data-ttu-id="590c8-110">Ottiene un valore booleano che indica se è necessario riavviare il sistema in un computer per completare l'installazione di un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="590c8-110">Gets a Boolean value that indicates whether a system restart is required on a computer to complete the installation of an update.</span></span> |
| [<span data-ttu-id="590c8-111">**ResultCode**</span><span class="sxs-lookup"><span data-stu-id="590c8-111">**ResultCode**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdateinstallationresult-get_resultcode)         | <span data-ttu-id="590c8-112">Ottiene un valore [**OperationResultCode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) che specifica il risultato di un'operazione su un aggiornamento.</span><span class="sxs-lookup"><span data-stu-id="590c8-112">Gets an [**OperationResultCode**](/windows/win32/api/wuapi/ne-wuapi-operationresultcode) value that specifies the result of an operation on an update.</span></span>          |



 

 

 



