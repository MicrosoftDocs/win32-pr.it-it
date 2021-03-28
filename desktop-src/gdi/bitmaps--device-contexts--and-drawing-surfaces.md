---
description: Un contesto di dispositivo (DC) è una struttura di dati che definisce gli oggetti grafici, gli attributi associati e le modalità grafiche che interessano l'output in un dispositivo. Per creare un controller di dominio, chiamare la funzione CreateDC. per recuperare un controller di dominio, chiamare la funzione GetDC.
ms.assetid: 4feafb23-bf5a-493a-9d1d-96170711b907
title: Bitmap, contesti di dispositivo e superfici di disegno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6297eb3446d05d0fa21ac23c9de9f3416a300746
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226710"
---
# <a name="bitmaps-device-contexts-and-drawing-surfaces"></a>Bitmap, contesti di dispositivo e superfici di disegno

Un *contesto di dispositivo* (DC) è una struttura di dati che definisce gli oggetti grafici, gli attributi associati e le modalità grafiche che interessano l'output in un dispositivo. Per creare un controller di dominio, chiamare la funzione [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) . per recuperare un controller di dominio, chiamare la funzione [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) .

Prima di restituire un handle che identifichi il controller di dominio, il sistema seleziona una superficie di disegno nel controller di dominio. Se l'applicazione ha chiamato la funzione [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) per creare un contesto di dispositivo per una visualizzazione VGA, le dimensioni della superficie di disegno sono 640 per 480 pixel. Se l'applicazione ha chiamato la funzione [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) , le dimensioni riflettono le dimensioni dell'area client.

Prima che un'applicazione possa iniziare a disegnare, deve selezionare una bitmap con la larghezza e l'altezza appropriate per il controller di dominio chiamando la funzione [**SelezionaOggetto**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) . Quando un'applicazione passa l'handle al controller di dominio a una delle funzioni di disegno GDI (Graphics Device Interface), l'output richiesto viene visualizzato nella superficie di disegno selezionata nel controller di dominio.

Per altre informazioni, vedere [contesti di dispositivo di memoria](memory-device-contexts.md).

 

 



