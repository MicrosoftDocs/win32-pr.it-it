---
description: L'attributo color specifica il colore della penna.
ms.assetid: ce775359-65fc-40d0-8725-b392cc0464a6
title: Colore penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e88d73fc80f6fe02a6d9e1de1d33568c94e05768f113c8bee0754c5d8afb418
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117886206"
---
# <a name="pen-color"></a>Colore penna

L'attributo color specifica il colore della penna. Un'applicazione può creare una penna cosmesi con un colore univoco usando la macro [**RGB**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) per archiviare la tripletta rossa, verde e blu che specifica il colore desiderato in una struttura [COLORREF](colorref.md) e passando l'indirizzo di questa struttura alla [**funzione CreatePen**](/windows/desktop/api/Wingdi/nf-wingdi-createpen), [**CreatePenIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createpenindirect)o [**ExtCreatePen.**](/windows/desktop/api/Wingdi/nf-wingdi-extcreatepen) Le penne predefinite sono limitate a nero, bianco e invisibile. Per altre informazioni sulle triplette RGB e sul colore, vedere [Colori](colors.md).

 

 



