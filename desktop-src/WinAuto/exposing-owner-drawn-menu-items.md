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
# <a name="exposing-owner-drawn-menu-items"></a>Esposizione di Owner-Drawn voci di menu

Gli sviluppatori di applicazioni possono utilizzare la struttura [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) per esporre i nomi delle voci di menu create dal proprietario. Associando questa struttura ai dati della voce di menu disegnata dal proprietario, non è necessario esporre le voci di menu con [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).

Quando si crea un menu creato dal proprietario, definire una classe o una struttura per i dati della voce di menu disegnata dal proprietario e creare istanze di questa classe per ogni voce di menu. Passare un puntatore ai dati dell'elemento quando si aggiungono elementi al menu.

Per esporre i nomi delle voci di menu, è necessario che la struttura [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) sia il primo membro della struttura che definisce i dati dell'elemento specifici dell'applicazione, come illustrato nell'esempio seguente:


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



La struttura [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) non può essere un membro di una classe che contiene funzioni virtuali. Quando il codice viene compilato, il primo membro della classe è sempre un puntatore generato dal compilatore a una tabella delle funzioni virtuali. Per risolvere questo problema, creare una struttura di dati degli elementi che contenga **MSAAMENUINFO** come primo membro. Il secondo membro è un puntatore a un'istanza della classe che definisce i dati creati dal proprietario. Nell'esempio seguente viene illustrata questa tecnica.


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



Quando si aggiungono elementi al menu, passare un puntatore a un'istanza della struttura che contiene [**MSAAMENUINFO**](/windows/win32/api/oleacc/ns-oleacc-msaamenuinfo) per esporre i nomi delle voci di menu.

 

 




