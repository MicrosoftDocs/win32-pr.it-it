---
description: Per ogni applicazione che usa un archivio criteri di autorizzazione, è necessario creare un oggetto IAzApplication e salvarlo in un archivio criteri.
ms.assetid: 5df964de-e5b6-427e-b859-efb5866f1578
title: Creazione di un oggetto applicazione nello script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0a4852ef0c06d721f9409c000989895f6767eb9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753495"
---
# <a name="creating-an-application-object-in-script"></a><span data-ttu-id="80649-103">Creazione di un oggetto applicazione nello script</span><span class="sxs-lookup"><span data-stu-id="80649-103">Creating an Application Object in Script</span></span>

<span data-ttu-id="80649-104">Un archivio dei criteri di autorizzazione contiene informazioni sui criteri di autorizzazione per una o più applicazioni.</span><span class="sxs-lookup"><span data-stu-id="80649-104">An authorization policy store contains authorization policy information for one or more applications.</span></span> <span data-ttu-id="80649-105">Per ogni applicazione che usa un archivio criteri di autorizzazione, è necessario creare un oggetto [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) e salvarlo in un archivio criteri.</span><span class="sxs-lookup"><span data-stu-id="80649-105">For each application that uses an authorization policy store, you must create an [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) object and save it to a policy store.</span></span>

<span data-ttu-id="80649-106">Nell'esempio seguente viene illustrato come creare un oggetto [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) che rappresenta un'applicazione e come aggiungere l'oggetto **IAzApplication** all'archivio dei criteri di autorizzazione utilizzato dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="80649-106">The following example shows how to create an [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) object that represents an application and how to add the **IAzApplication** object to the authorization policy store the application uses.</span></span> <span data-ttu-id="80649-107">Nell'esempio si presuppone l'esistenza di un archivio criteri XML denominato MyStore.xml nella directory radice dell'unità C.</span><span class="sxs-lookup"><span data-stu-id="80649-107">The example assumes that there is an existing XML policy store named MyStore.xml in the root directory of drive C.</span></span>


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Create an application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.CreateApplication("Expense")

'  Save changes to the store.
expenseApp.Submit
```



 

 



