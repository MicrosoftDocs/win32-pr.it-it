---
description: L'attributo color specifica il colore della penna.
ms.assetid: ce775359-65fc-40d0-8725-b392cc0464a6
title: Colore della penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92d831994ac444207832574dc104a9d5c2582db8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528302"
---
# <a name="pen-color"></a>Colore della penna

L'attributo color specifica il colore della penna. Un'applicazione può creare una penna cosmetica con un colore univoco usando la macro [**RGB**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) per archiviare la tripletta rossa, verde, blu che specifica il colore desiderato in una struttura [COLORREF](colorref.md) e passando l'indirizzo della struttura alla funzione [**CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)o [**ExtCreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) . Le penne azionarie sono limitate a nero, bianco e invisibile. Per ulteriori informazioni sui triple e sui colori RGB, vedere [colori](colors.md).

 

 



