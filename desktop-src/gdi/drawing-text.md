---
description: Disegno di testo
ms.assetid: 8a06f659-4e08-4738-b7a9-956b599c1344
title: Disegno di testo (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7db44a756ff211bcae7605cb87bdac77005b34f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754423"
---
# <a name="drawing-text-windows-gdi"></a>Disegno di testo (Windows GDI)

Dopo che un'applicazione ha selezionato il tipo di carattere appropriato, imposta le opzioni di formattazione del testo necessarie e calcola i valori di larghezza e altezza dei caratteri necessari per una stringa di testo, può iniziare a disegnare caratteri e simboli chiamando una delle funzioni di output di testo:

-   [DrawText](/windows/desktop/api/Winuser/nf-winuser-drawtext)
-   [DrawTextEx](/windows/desktop/api/Winuser/nf-winuser-drawtextexa)
-   [ExtTextOut](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta)
-   [Sottotesto](/windows/desktop/api/Wingdi/nf-wingdi-polytextouta)
-   [TabbedTextOut](/windows/desktop/api/Winuser/nf-winuser-tabbedtextouta)
-   [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta)

Quando un'applicazione chiama una di queste funzioni, il sistema operativo passa la chiamata al motore di grafica, che a sua volta passa la chiamata al driver di dispositivo appropriato. A livello di driver di dispositivo, tutte queste chiamate sono supportate da una o più chiamate alla funzione [ExtTextOut](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta) o [Text](/windows/desktop/api/Wingdi/nf-wingdi-textouta) out del driver. Un'applicazione raggiungerà l'esecuzione più veloce chiamando [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta), che viene rapidamente convertito in una chiamata **ExtTextOut** per il dispositivo. Tuttavia, esistono istanze quando un'applicazione deve chiamare una delle altre tre funzioni; per creare, ad esempio, più righe di testo all'interno dei bordi di un'area rettangolare specificata, è più efficiente chiamare [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext). Per creare una tabella a più colonne con colonne giustificate di testo, è più efficiente chiamare [**TabbedTextOut**](/windows/win32/api/winuser/nf-winuser-tabbedtextouta).

 

 
