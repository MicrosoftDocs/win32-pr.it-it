---
title: CENUMNS. CPP
description: Nel componente provider di esempio, l'enumerazione di un oggetto spazio dei nomi utilizza i metodi, da cenumns. cpp, elencati nella tabella seguente.
ms.assetid: 52e23977-8df6-44a4-9a5e-a7896471c17e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0a8bc745535014a346e8042c577d14222302679
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300418"
---
# <a name="cenumnscpp"></a><span data-ttu-id="7dfd7-103">CENUMNS. CPP</span><span class="sxs-lookup"><span data-stu-id="7dfd7-103">CENUMNS.CPP</span></span>

<span data-ttu-id="7dfd7-104">Nel componente provider di esempio, l'enumerazione di un oggetto spazio dei nomi utilizza i metodi, da cenumns. cpp, elencati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-104">In the example provider component, the enumeration of a namespace object uses the methods, from cenumns.cpp, listed in the following table.</span></span>



| <span data-ttu-id="7dfd7-105">Metodo</span><span class="sxs-lookup"><span data-stu-id="7dfd7-105">Method</span></span>                                              | <span data-ttu-id="7dfd7-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7dfd7-106">Description</span></span>                                                                                                                                               |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7dfd7-107">**CSampleDSNamespaceEnum:: create**</span><span class="sxs-lookup"><span data-stu-id="7dfd7-107">**CSampleDSNamespaceEnum::Create**</span></span>                  | <span data-ttu-id="7dfd7-108">Creare un oggetto per consentire l'enumerazione di un oggetto spazio dei nomi ADS.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-108">Create an object to allow enumeration of an ADS namespace object.</span></span>                                                                                         |
| <span data-ttu-id="7dfd7-109">**CSampleDSNamespaceEnum::CSampleDSNamespaceEnum**</span><span class="sxs-lookup"><span data-stu-id="7dfd7-109">**CSampleDSNamespaceEnum::CSampleDSNamespaceEnum**</span></span>  | <span data-ttu-id="7dfd7-110">Costruttore standard.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-110">Standard constructor.</span></span>                                                                                                                                     |
| <span data-ttu-id="7dfd7-111">**CSampleDSNamespaceEnum:: ~ CSampleDSNamespaceEnum**</span><span class="sxs-lookup"><span data-stu-id="7dfd7-111">**CSampleDSNamespaceEnum::~CSampleDSNamespaceEnum**</span></span> | <span data-ttu-id="7dfd7-112">Distruttore standard.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-112">Standard destructor.</span></span>                                                                                                                                      |
| <span data-ttu-id="7dfd7-113">**CSampleDSNamespaceEnum:: Next**</span><span class="sxs-lookup"><span data-stu-id="7dfd7-113">**CSampleDSNamespaceEnum::Next**</span></span>                    | <span data-ttu-id="7dfd7-114">Recupera il numero specificato di elementi dall'oggetto spazio dei nomi indicato.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-114">Retrieve the specified number of elements from the namespace object indicated.</span></span>                                                                            |
| <span data-ttu-id="7dfd7-115">**CSampleDSNamespaceEnum:: EnumObjects**</span><span class="sxs-lookup"><span data-stu-id="7dfd7-115">**CSampleDSNamespaceEnum::EnumObjects**</span></span>             | <span data-ttu-id="7dfd7-116">Gestire il recupero dei puntatori di interfaccia agli oggetti.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-116">Manage retrieving the interface pointers to the objects.</span></span>                                                                                                  |
| <span data-ttu-id="7dfd7-117">**CSampleDSNamespaceEnum::FetchObjects**</span><span class="sxs-lookup"><span data-stu-id="7dfd7-117">**CSampleDSNamespaceEnum::FetchObjects**</span></span>            | <span data-ttu-id="7dfd7-118">Recupera il set di puntatori [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="7dfd7-118">Fetch the set of [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) pointers.</span></span>                                                                          |
| <span data-ttu-id="7dfd7-119">**CSampleDSNamespaceEnum::FetchNextObject**</span><span class="sxs-lookup"><span data-stu-id="7dfd7-119">**CSampleDSNamespaceEnum::FetchNextObject**</span></span>         | <span data-ttu-id="7dfd7-120">Recuperare l'oggetto successivo.</span><span class="sxs-lookup"><span data-stu-id="7dfd7-120">Fetch the next object.</span></span> <span data-ttu-id="7dfd7-121">Se trovato, creare un oggetto Active Directory generico e recuperare il puntatore [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="7dfd7-121">If found, create a generic Active Directory object and retrieve its [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) pointer.</span></span> |



 

 

 