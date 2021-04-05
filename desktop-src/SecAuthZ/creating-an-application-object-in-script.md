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
# <a name="creating-an-application-object-in-script"></a>Creazione di un oggetto applicazione nello script

Un archivio dei criteri di autorizzazione contiene informazioni sui criteri di autorizzazione per una o più applicazioni. Per ogni applicazione che usa un archivio criteri di autorizzazione, è necessario creare un oggetto [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) e salvarlo in un archivio criteri.

Nell'esempio seguente viene illustrato come creare un oggetto [**IAzApplication**](/windows/desktop/api/Azroles/nn-azroles-iazapplication) che rappresenta un'applicazione e come aggiungere l'oggetto **IAzApplication** all'archivio dei criteri di autorizzazione utilizzato dall'applicazione. Nell'esempio si presuppone l'esistenza di un archivio criteri XML denominato MyStore.xml nella directory radice dell'unità C.


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



 

 



