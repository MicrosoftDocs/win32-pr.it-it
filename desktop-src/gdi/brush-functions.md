---
description: Le funzioni seguenti vengono utilizzate con i pennelli.
ms.assetid: 617eb778-876c-4bbb-90da-c5f13359becb
title: Funzioni pennello (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2170ff5c4b743e19da669bd76b340ca95ac2ef9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528393"
---
# <a name="brush-functions-windows-gdi"></a>Funzioni pennello (Windows GDI)

Le funzioni seguenti vengono utilizzate con i pennelli.



| Funzione                                                   | Descrizione                                                |
|------------------------------------------------------------|------------------------------------------------------------|
| [**CreateBrushIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbrushindirect)         | Crea un pennello con lo stile, il colore e il modello specificati. |
| [**CreateDIBPatternBrushPt**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrushpt) | Crea un pennello con il modello da una DIB                |
| [**CreateHatchBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createhatchbrush)               | Crea un pennello con un motivo di tratteggio e un colore             |
| [**CreatePatternBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createpatternbrush)           | Crea un pennello con un modello bitmap                      |
| [**CreateSolidBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createsolidbrush)               | Crea un pennello con un colore a tinta unita                         |
| [**GetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-getbrushorgex)                     | Ottiene l'origine del pennello per un contesto di dispositivo                 |
| [**GetSysColorBrush**](/windows/desktop/api/Winuser/nf-winuser-getsyscolorbrush)               | Ottiene un handle per un pennello che corrisponde a un indice colori |
| [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt)                                   | Disegna un rettangolo                                         |
| [**SetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setbrushorgex)                     | Imposta l'origine del pennello per un contesto di dispositivo                 |
| [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)                 | Imposta il colore corrente del pennello del contesto di dispositivo.               |



 

## <a name="obsolete-functions"></a>Funzioni obsolete

Le funzioni seguenti vengono fornite solo per la compatibilità con le versioni di Windows a 16 bit.

[**CreateDIBPatternBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrush)

 

 



