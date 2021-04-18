---
title: Esposizione di Owner-Drawn voci di menu
description: Esposizione di Owner-Drawn voci di menu
ms.assetid: 93b51cbb-b7b4-4a38-ba69-d6345a269944
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e79668115cedd5fb6b8c20b0d4df361d6d1d800
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515919"
---
# <a name="exposing-owner-drawn-menu-items"></a><span data-ttu-id="40a24-103">Esposizione di Owner-Drawn voci di menu</span><span class="sxs-lookup"><span data-stu-id="40a24-103">Exposing Owner-Drawn Menu Items</span></span>

<span data-ttu-id="40a24-104">Gli sviluppatori di applicazioni possono utilizzare la struttura [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) per esporre i nomi delle voci di menu create dal proprietario.</span><span class="sxs-lookup"><span data-stu-id="40a24-104">Application developers can use the [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) structure to expose the names of owner-drawn menu items.</span></span> <span data-ttu-id="40a24-105">Associando questa struttura ai dati della voce di menu disegnata dal proprietario, non è necessario esporre le voci di menu con [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span><span class="sxs-lookup"><span data-stu-id="40a24-105">By associating this structure with the owner-drawn menu item data, you do not need to expose the menu items with [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span>

<span data-ttu-id="40a24-106">Quando si crea un menu creato dal proprietario, definire una classe o una struttura per i dati della voce di menu disegnata dal proprietario e creare istanze di questa classe per ogni voce di menu.</span><span class="sxs-lookup"><span data-stu-id="40a24-106">When creating an owner-drawn menu, define a class or structure for the owner-drawn menu item data and create instances of this class for each menu item.</span></span> <span data-ttu-id="40a24-107">Passare un puntatore ai dati dell'elemento quando si aggiungono elementi al menu.</span><span class="sxs-lookup"><span data-stu-id="40a24-107">Pass in a pointer to the item data when adding items to the menu.</span></span>

<span data-ttu-id="40a24-108">Per esporre i nomi delle voci di menu, è necessario che la struttura [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) sia il primo membro della struttura che definisce i dati dell'elemento specifici dell'applicazione, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="40a24-108">To expose the names of the menu items, the [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) structure must be the first member of the structure that defines the application-specific item data, as shown in the following example:</span></span>


```C++
// Application-specific owner-drawn menu info struct. Owner-drawn data 
// is a pointer to one of these.
struct MenuEntry
{
    MSAAMENUINFO m_MSAA;       // MSAA info - must be first member
    LPTSTR       m_pName;      // Displayed menu text or NULL for 
                               //   separator item 
    int          m_CmdID;      // Menu command ID 
    int          m_IconIndex;  // Index of icon in bitmap or -1 for
                               //   for separator 
};
```



<span data-ttu-id="40a24-109">La struttura [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) non può essere un membro di una classe che contiene funzioni virtuali.</span><span class="sxs-lookup"><span data-stu-id="40a24-109">The [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) structure cannot be a member in a class that contains virtual functions.</span></span> <span data-ttu-id="40a24-110">Quando il codice viene compilato, il primo membro della classe è sempre un puntatore generato dal compilatore a una tabella delle funzioni virtuali.</span><span class="sxs-lookup"><span data-stu-id="40a24-110">When the code is compiled, the first member of the class is always a compiler-generated pointer to a table of the virtual functions.</span></span> <span data-ttu-id="40a24-111">Per risolvere questo problema, creare una struttura di dati degli elementi che contenga **MSAAMENUINFO** come primo membro.</span><span class="sxs-lookup"><span data-stu-id="40a24-111">To work around this problem, create an item data structure that contains **MSAAMENUINFO** as the first member.</span></span> <span data-ttu-id="40a24-112">Il secondo membro è un puntatore a un'istanza della classe che definisce i dati creati dal proprietario.</span><span class="sxs-lookup"><span data-stu-id="40a24-112">The second member is a pointer to an instance of the class that defines the owner-drawn data.</span></span> <span data-ttu-id="40a24-113">Nell'esempio seguente viene illustrata questa tecnica.</span><span class="sxs-lookup"><span data-stu-id="40a24-113">The following example demonstrates this technique.</span></span>


```C++
// Application-defined class that contains the owner-drawn data and 
//  virtual functions that operate on that data.  
class MenuEntry
{
    LPTSTR       m_pName;      // Displayed menu text or NULL for 
                               //  separator item. 
    int          m_CmdID;      // Menu command ID 
    int          m_IconIndex;  // Index of icon in bitmap or -1 for
                               //  separator item 
    virtual void m_AnimateIcon();  
    virtual void m_ChangeIconColor();
}

// Application-defined struct that contains MSAAMENUINFO as first 
//  member. Second member points to owner-drawn data. 
struct MenuInfo
{
    MSAAMENUINFO m_MSAA;       // MSAA info - must be first member
    MenuEntry *pMenuData;      // Points to the owner-drawn data 
}
```



<span data-ttu-id="40a24-114">Quando si aggiungono elementi al menu, passare un puntatore a un'istanza della struttura che contiene [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) per esporre i nomi delle voci di menu.</span><span class="sxs-lookup"><span data-stu-id="40a24-114">When adding items to the menu, pass a pointer to an instance of the structure that contains [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) to expose the names of the menu items.</span></span>

 

 




