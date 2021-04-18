---
description: L'interfaccia IUpdateCollection definisce le proprietà seguenti.
ms.assetid: 38420d5e-4d36-4ed7-be06-e1df903929a7
title: Proprietà di IUpdateCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8aae347885deccb52ac44513bd1138aa18995c41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307629"
---
# <a name="iupdatecollection-properties"></a><span data-ttu-id="fe97f-103">Proprietà di IUpdateCollection</span><span class="sxs-lookup"><span data-stu-id="fe97f-103">IUpdateCollection Properties</span></span>

<span data-ttu-id="fe97f-104">L'interfaccia [**IUpdateCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatecollection) definisce le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="fe97f-104">The [**IUpdateCollection**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatecollection) interface defines the following properties.</span></span>



| <span data-ttu-id="fe97f-105">Proprietà</span><span class="sxs-lookup"><span data-stu-id="fe97f-105">Property</span></span>                                        | <span data-ttu-id="fe97f-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fe97f-106">Description</span></span>                                                                                                              |
|-------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fe97f-107">**\_NewEnum**</span><span class="sxs-lookup"><span data-stu-id="fe97f-107">**\_NewEnum**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get__newenum) | <span data-ttu-id="fe97f-108">Ottiene un'interfaccia [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) che può essere utilizzata per enumerare la raccolta.</span><span class="sxs-lookup"><span data-stu-id="fe97f-108">Gets an [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface that can be used to enumerate the collection.</span></span> |
| [<span data-ttu-id="fe97f-109">**Conteggio**</span><span class="sxs-lookup"><span data-stu-id="fe97f-109">**Count**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get_count)        | <span data-ttu-id="fe97f-110">Ottiene il numero di elementi nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="fe97f-110">Gets the number of elements in the collection.</span></span>                                                                           |
| [<span data-ttu-id="fe97f-111">**Elemento**</span><span class="sxs-lookup"><span data-stu-id="fe97f-111">**Item**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get_item)          | <span data-ttu-id="fe97f-112">Ottiene o imposta un'interfaccia [**IUpdate**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate) in una raccolta.</span><span class="sxs-lookup"><span data-stu-id="fe97f-112">Gets or sets an [**IUpdate**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate) interface in a collection.</span></span>                                                    |
| [<span data-ttu-id="fe97f-113">**ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="fe97f-113">**ReadOnly**</span></span>](/windows/desktop/api/Wuapi/nf-wuapi-iupdatecollection-get_readonly)  | <span data-ttu-id="fe97f-114">Ottiene un valore booleano che indica se la raccolta di aggiornamenti è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="fe97f-114">Gets a Boolean value that indicates whether the update collection is read-only.</span></span>                                          |



 

 

 
