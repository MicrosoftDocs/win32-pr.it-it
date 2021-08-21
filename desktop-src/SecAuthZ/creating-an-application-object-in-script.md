---
description: Per ogni applicazione che usa un archivio criteri di autorizzazione, è necessario creare un oggetto IAzApplication e quindi salvarlo in un archivio criteri.
ms.assetid: 5df964de-e5b6-427e-b859-efb5866f1578
title: Creazione di un oggetto applicazione nello script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 02a5ada4a8a79244cc454d9efc88e69a5d9a205241119b5dda371699f0c86552
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117782547"
---
# <a name="creating-an-application-object-in-script"></a>Creazione di un oggetto applicazione nello script

Un archivio dei criteri di autorizzazione contiene informazioni sui criteri di autorizzazione per una o più applicazioni. Per ogni applicazione che usa un archivio criteri di autorizzazione, è necessario creare un oggetto [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) e salvarlo in un archivio criteri.

L'esempio seguente illustra come creare un oggetto [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) che rappresenta un'applicazione e come aggiungere **l'oggetto IAzApplication** all'archivio dei criteri di autorizzazione utilizzato dall'applicazione. Nell'esempio si presuppone che sia presente un archivio criteri XML esistente denominato MyStore.xml nella directory radice dell'unità C.


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



 

 



