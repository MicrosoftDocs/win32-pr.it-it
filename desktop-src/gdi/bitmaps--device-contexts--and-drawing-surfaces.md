---
description: Un contesto di dispositivo è una struttura di dati che definisce gli oggetti grafici, i relativi attributi associati e le modalità grafiche che influiscono sull'output in un dispositivo. Per creare un controller di dominio, chiamare la funzione CreateDC. per recuperare un controller di dominio, chiamare la funzione GetDC.
ms.assetid: 4feafb23-bf5a-493a-9d1d-96170711b907
title: Bitmap, contesti di dispositivo e superfici di disegno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed42215dc98ce179f9d36ddc0a24244c018c4177287d1fdfff974a2814e14d64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966391"
---
# <a name="bitmaps-device-contexts-and-drawing-surfaces"></a>Bitmap, contesti di dispositivo e superfici di disegno

Un *contesto di* dispositivo è una struttura di dati che definisce gli oggetti grafici, i relativi attributi associati e le modalità grafiche che influiscono sull'output in un dispositivo. Per creare un controller di dominio, chiamare [**la funzione CreateDC.**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) per recuperare un controller di dominio, chiamare la [**funzione GetDC.**](/windows/desktop/api/Winuser/nf-winuser-getdc)

Prima di restituire un handle che identifica tale controller di dominio, il sistema seleziona una superficie di disegno nel controller di dominio. Se l'applicazione ha chiamato la funzione [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) per creare un contesto di dispositivo per una visualizzazione VGA, le dimensioni di questa superficie di disegno sono di 640 per 480 pixel. Se l'applicazione ha chiamato [**la funzione GetDC,**](/windows/desktop/api/Winuser/nf-winuser-getdc) le dimensioni riflettono le dimensioni dell'area client.

Prima di iniziare a disegnare, un'applicazione deve selezionare una bitmap con la larghezza e l'altezza appropriate nel controller di dominio chiamando la [**funzione SelectObject.**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) Quando un'applicazione passa l'handle al controller di dominio a una delle funzioni di disegno GDI (Graphics Device Interface), l'output richiesto viene visualizzato sull'area di disegno selezionata nel controller di dominio.

Per altre informazioni, vedere [Contesti di dispositivo di memoria](memory-device-contexts.md).

 

 



