---
title: Appendice D Note per gli sviluppatori di Visual Basic
description: In questa sezione vengono fornite informazioni su Microsoft Active Accessibility per sviluppatori Microsoft Visual Basic.
ms.assetid: 82a016a2-872d-4ba6-ac93-78b59f7ec639
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc09c23a81b2f987a6f651a923dd10b0d16a2a27
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955414"
---
# <a name="appendix-d-notes-for-visual-basic-developers"></a>Appendice D: Note per gli sviluppatori di Visual Basic

In questa sezione vengono fornite informazioni su Microsoft Active Accessibility per sviluppatori Microsoft Visual Basic.

Le applicazioni scritte in Visual Basic sono client Microsoft Active Accessibility. Non forniscono informazioni sugli elementi dell'interfaccia utente personalizzati perché non implementano [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) o qualsiasi altra interfaccia Component Object Model (com).

In questa documentazione vengono utilizzati i nomi C/C++ per le proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . Tuttavia, i nomi di Visual Basic sono simili. Ad esempio, la proprietà [**IAccessible:: Get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) viene chiamata **accName** in un'applicazione Visual Basic.

## <a name="in-this-section"></a>Contenuto della sezione

-   [Note sul metodo Visual Basic: accName](visual-basic-method-notes--accname.md)
-   [Note sul metodo Visual Basic: accValue](visual-basic-method-notes--accvalue.md)
-   [Visual Basic programmi di esempio](visual-basic-sample-programs.md)

 

 




