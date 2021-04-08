---
title: Trasferimento di oggetti
description: Trasferimento di oggetti
ms.assetid: 3afdf480-a7ee-4b7b-99f6-4a8e8cb2096c
ms.tgt_platform: multiple
keywords:
- Esempi di Active Directory Active Directory, trasferimento di oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7019904d0de42492b98ddd297ab007a6f4e52f6a
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046501"
---
# <a name="moving-objects"></a><span data-ttu-id="589ab-104">Trasferimento di oggetti</span><span class="sxs-lookup"><span data-stu-id="589ab-104">Moving Objects</span></span>

<span data-ttu-id="589ab-105">Per spostare un oggetto all'interno di un dominio, usare il metodo [**IADsContainer. MoveHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere) .</span><span class="sxs-lookup"><span data-stu-id="589ab-105">To move an object within a domain, use the [**IADsContainer.MoveHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere) method.</span></span>

<span data-ttu-id="589ab-106">**Per spostare un oggetto all'interno di un dominio**</span><span class="sxs-lookup"><span data-stu-id="589ab-106">**To move an object within a domain**</span></span>

1.  <span data-ttu-id="589ab-107">Eseguire l'associazione all'interfaccia [**IADs**](/windows/desktop/api/iads/nn-iads-iads) dell'oggetto da spostare.</span><span class="sxs-lookup"><span data-stu-id="589ab-107">Bind to the [**IADs**](/windows/desktop/api/iads/nn-iads-iads) interface of the object to move.</span></span>
2.  <span data-ttu-id="589ab-108">Ottenere il ADsPath dell'oggetto da spostare dalla proprietà [**IADs. ADsPath**](/windows/desktop/ADSI/iads-property-methods) .</span><span class="sxs-lookup"><span data-stu-id="589ab-108">Get the ADsPath of the object to move from the [**IADs.ADsPath**](/windows/desktop/ADSI/iads-property-methods) property.</span></span>
3.  <span data-ttu-id="589ab-109">Eseguire l'associazione all'interfaccia [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) del contenitore in cui verrà spostato l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="589ab-109">Bind to the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface of the container where the object will be moved to.</span></span>
4.  <span data-ttu-id="589ab-110">Spostare l'oggetto con il metodo [**IADsContainer. MoveHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere) .</span><span class="sxs-lookup"><span data-stu-id="589ab-110">Move the object with the [**IADsContainer.MoveHere**](/windows/desktop/api/iads/nf-iads-iadscontainer-movehere) method.</span></span>

<span data-ttu-id="589ab-111">Se è presente un'interfaccia per l'oggetto spostato, l'interfaccia non è valida dopo lo spostamento dell'oggetto perché l'oggetto directory rappresentato dall'interfaccia non esiste più.</span><span class="sxs-lookup"><span data-stu-id="589ab-111">If an interface exists to the object that was moved, the interface is not valid after the object is moved because the directory object the interface represents no longer exists.</span></span>

<span data-ttu-id="589ab-112">Per ulteriori informazioni e un esempio di codice in cui viene illustrato come spostare un oggetto, vedere il [codice di esempio per lo spostamento di un oggetto](example-code-for-moving-an-object.md).</span><span class="sxs-lookup"><span data-stu-id="589ab-112">For more information and a code example that shows how to move an object, see [Example Code for Moving an Object](example-code-for-moving-an-object.md).</span></span>

 

 