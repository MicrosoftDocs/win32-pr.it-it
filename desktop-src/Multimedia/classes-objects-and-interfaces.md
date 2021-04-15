---
title: Classi, oggetti e interfacce
description: Classi, oggetti e interfacce
ms.assetid: 52e48402-32d5-46b0-8eb9-46432e59e36a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d4892a805c87122ff7fb6db80feb52a7dcd7625
ms.sourcegitcommit: 52d79b29f3b9933c8bef43207ff80c668a81cb73
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "104474615"
---
# <a name="classes-objects-and-interfaces"></a><span data-ttu-id="fcf68-103">Classi, oggetti e interfacce</span><span class="sxs-lookup"><span data-stu-id="fcf68-103">Classes, Objects, and Interfaces</span></span>

<span data-ttu-id="fcf68-104">Nel linguaggio di programmazione C++, una *classe* è costituita da *Proprietà* (o dati membro) e *Metodi* (o funzioni membro).</span><span class="sxs-lookup"><span data-stu-id="fcf68-104">In the C++ programming language, a *class* consists of *properties* (or member data) and *methods* (or member functions).</span></span> <span data-ttu-id="fcf68-105">Le proprietà sono elementi dati, ad esempio quelli contenuti in una struttura.</span><span class="sxs-lookup"><span data-stu-id="fcf68-105">The properties are data elements, such as those contained in a structure.</span></span> <span data-ttu-id="fcf68-106">I metodi vengono utilizzati per diversi scopi, ad esempio l'inizializzazione, l'assegnazione, le operazioni e l'accesso ai dati.</span><span class="sxs-lookup"><span data-stu-id="fcf68-106">The methods are used for a variety of purposes, such as initialization, assignment, operations, and data access.</span></span> <span data-ttu-id="fcf68-107">Usare una dichiarazione di classe nello stesso modo in cui si usa una dichiarazione della struttura.</span><span class="sxs-lookup"><span data-stu-id="fcf68-107">You use a class declaration in the same way that you use a structure declaration.</span></span> <span data-ttu-id="fcf68-108">La memoria viene allocata per una classe quando si definisce un *oggetto* classe.</span><span class="sxs-lookup"><span data-stu-id="fcf68-108">Memory is allocated for a class when you define a class *object*.</span></span> <span data-ttu-id="fcf68-109">Ogni oggetto classe dispone di un'area dati per le relative proprietà e una tabella di puntatori ai metodi supportati.</span><span class="sxs-lookup"><span data-stu-id="fcf68-109">Each class object has a data area for its properties and a table of pointers to the methods it supports.</span></span>

<span data-ttu-id="fcf68-110">In OLE un oggetto è costituito da dati e metodi, come avviene in C++.</span><span class="sxs-lookup"><span data-stu-id="fcf68-110">In OLE, an object consists of data and methods, as it does in C++.</span></span> <span data-ttu-id="fcf68-111">Tuttavia, un oggetto OLE rispetta regole più restrittive.</span><span class="sxs-lookup"><span data-stu-id="fcf68-111">However, an OLE object adheres to stricter rules.</span></span> <span data-ttu-id="fcf68-112">I dati sono strettamente interni.</span><span class="sxs-lookup"><span data-stu-id="fcf68-112">The data is strictly internal.</span></span> <span data-ttu-id="fcf68-113">Un oggetto espone solo le interfacce.</span><span class="sxs-lookup"><span data-stu-id="fcf68-113">An object only exposes interfaces.</span></span> <span data-ttu-id="fcf68-114">Un' *interfaccia* è un set di metodi correlati per un oggetto.</span><span class="sxs-lookup"><span data-stu-id="fcf68-114">An *interface* is a set of related methods for an object.</span></span> <span data-ttu-id="fcf68-115">Ogni oggetto può supportare più interfacce.</span><span class="sxs-lookup"><span data-stu-id="fcf68-115">Each object can support multiple interfaces.</span></span> <span data-ttu-id="fcf68-116">Tutte le interfacce OLE supportano l'interfaccia [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="fcf68-116">All OLE interfaces support the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span>

 

 




