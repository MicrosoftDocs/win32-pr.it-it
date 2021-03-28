---
description: La funzione ExcludeUpdateRgn esclude l'area di aggiornamento dall'area di visualizzazione del contesto del dispositivo di visualizzazione.
ms.assetid: e652122b-a3b7-4d1b-8afd-9648d5ee3d42
title: Esclusione dell'area di aggiornamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7be39b948e61fc06c7f7005d15c1163cef0068f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049726"
---
# <a name="excluding-the-update-region"></a>Esclusione dell'area di aggiornamento

La funzione [**ExcludeUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-excludeupdatergn) esclude l'area di aggiornamento dall'area di visualizzazione del contesto del dispositivo di visualizzazione. Questa funzione è utile quando si disegna in una finestra diversa da quando viene elaborato un messaggio di disegno WM \_ . Impedisce il disegno nelle aree che verranno aggiornate durante il successivo messaggio di disegno WM \_ .

 

 



