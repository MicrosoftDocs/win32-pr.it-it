---
description: In Gestione autorizzazioni un'operazione è una funzione o un metodo di basso livello di un'applicazione.
ms.assetid: 6b35d25e-150c-4760-b358-fa517a00dd79
title: Definizione di operazioni nello script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ef1337bc8e5c44ccce25e3f6d87f7cf6240d2d2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350576"
---
# <a name="defining-operations-in-script"></a>Definizione di operazioni nello script

In Gestione autorizzazioni un'operazione è una funzione o un metodo di basso livello di un'applicazione. Queste operazioni sono raggruppate come attività. Gli utenti dell'applicazione richiedono l'autorizzazione per completare le attività. Un'operazione è rappresentata da un oggetto [**IAzOperation**](/windows/desktop/api/Azroles/nn-azroles-iazoperation) . Per ulteriori informazioni sulle operazioni, vedere [operazioni e attività](operations-and-tasks.md).

Nell'esempio seguente viene illustrato come definire le operazioni in un archivio dei criteri di autorizzazione. Nell'esempio si presuppone l'esistenza di un archivio criteri XML denominato MyStore.xml nella directory radice dell'unità C e che l'archivio contenga un'applicazione denominata Expense.


```VB
'  Create the AzAuthorizationStore object.
Dim AzManStore
Set AzManStore = CreateObject("AzRoles.AzAuthorizationStore")

'  Initialize the authorization store.
AzManStore.Initialize 2, "msxml://C:\MyStore.xml"

'  Open the application object in the store.
Dim expenseApp
Set expenseApp= AzManStore.OpenApplication("Expense")

'  Create operations.

'  Create first operation.
Dim Op1
Set Op1 = expenseApp.CreateOperation("RetrieveForm")

'  Set the OperationID property.
Op1.OperationID = 1

'  Save the operation to the store.
Op1.Submit

'  Create second operation.
Dim Op2
Set Op2 = expenseApp.CreateOperation("EnqueRequest")

'  Set the OperationID property.
Op2.OperationID = 2

'  Save the operation to the store.
Op2.Submit

'  Create third operation.
Dim Op3
Set Op3 = expenseApp.CreateOperation("DequeRequest")

'  Set the OperationID property.
Op3.OperationID = 3

'  Save the operation to the store.
Op3.Submit

'  Create fourth operation.
Dim Op4
Set Op4 = expenseApp.CreateOperation("UseFormControl")

'  Set the OperationID property.
Op4.OperationID = 4

'  Save the operation to the store.
Op4.Submit

'  Create fifth operation.
Dim Op5
Set Op5 = expenseApp.CreateOperation("MarkFormApproved")

'  Set the OperationID property.
Op5.OperationID = 5

'  Save the operation to the store.
Op5.Submit

'  Create sixth operation.
Dim Op6
Set Op6 = expenseApp.CreateOperation("SendApprovalNotify")

'  Set the OperationID property.
Op6.OperationID = 6

'  Save the operation to the store.
Op6.Submit
```



 

 



