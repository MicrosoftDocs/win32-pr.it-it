---
description: Il rettangolo di delimitazione accumulato è il rettangolo più piccolo che racchiude la parte di una finestra o di un'area client interessata dalle operazioni di disegno recenti.
ms.assetid: 8ae13486-a9e2-4841-ada3-c70d30450ac8
title: Rettangolo di delimitazione accumulato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ae3237304af68a4b8ff447b7ea2d64d3f81053
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528399"
---
# <a name="accumulated-bounding-rectangle"></a>Rettangolo di delimitazione accumulato

Il *rettangolo di delimitazione accumulato* è il rettangolo più piccolo che racchiude la parte di una finestra o di un'area client interessata dalle operazioni di disegno recenti. Un'applicazione può utilizzare questo rettangolo per determinare agevolmente l'entità delle modifiche causate dalle operazioni di disegno. Viene talvolta utilizzata insieme a [**LockWindowUpdate**](/windows/desktop/api/Winuser/nf-winuser-lockwindowupdate) per determinare quale parte dell'area client deve essere ridisegnato dopo che il blocco di aggiornamento è stato cancellato.

Un'applicazione usa la funzione [**SetBoundsRect**](/windows/desktop/api/Wingdi/nf-wingdi-setboundsrect) (specificando DCB \_ Enable) per iniziare a accumulare il rettangolo di delimitazione. Il sistema accumula quindi punti per il rettangolo di delimitazione perché l'applicazione usa il contesto del dispositivo di visualizzazione specificato. L'applicazione può recuperare il rettangolo di delimitazione corrente in qualsiasi momento tramite la funzione [**GetBoundsRect**](/windows/desktop/api/Wingdi/nf-wingdi-getboundsrect) . L'applicazione interrompe l'accumulo chiamando di nuovo **SetBoundsRect** , specificando il \_ valore di disabilitazione di DCB.

 

 



