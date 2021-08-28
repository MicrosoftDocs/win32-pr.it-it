---
title: Appendice D Notes for Visual Basic Developers
description: In questa sezione vengono fornite informazioni sui Microsoft Active Accessibility per gli sviluppatori Visual Basic Microsoft.
ms.assetid: 82a016a2-872d-4ba6-ac93-78b59f7ec639
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a857aeb8e04a0648d991e26913f9a9cf5c35328c62ed3f1ac3903a267e5a4e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122421"
---
# <a name="appendix-d-notes-for-visual-basic-developers"></a>Appendice D: Note per Visual Basic sviluppatori

In questa sezione vengono fornite informazioni sui Microsoft Active Accessibility per gli sviluppatori Visual Basic Microsoft.

Le applicazioni scritte in Visual Basic sono Microsoft Active Accessibility client. Non forniscono informazioni sugli elementi dell'interfaccia utente personalizzata perché non implementano [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) o qualsiasi altra interfaccia Component Object Model (COM).

Questa documentazione usa i nomi C/C++ per le [**proprietà IAccessible.**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) Tuttavia, i Visual Basic sono simili. Ad esempio, la [**proprietà IAccessible::get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) viene chiamata **accName** in un'Visual Basic applicazione.

## <a name="in-this-section"></a>Contenuto della sezione

-   [Visual Basic Note sul metodo: accName](visual-basic-method-notes--accname.md)
-   [Visual Basic Note sul metodo: accValue](visual-basic-method-notes--accvalue.md)
-   [Visual Basic Programmi di esempio](visual-basic-sample-programs.md)

 

 




