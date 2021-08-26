---
description: Windows GDI+ i tipi di carattere con lo stesso carattere tipografico ma stili diversi in famiglie di caratteri.
ms.assetid: 57428fae-6af4-47a5-a499-717dc378767a
title: Costruzione di famiglie di caratteri e tipi di carattere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cc405883eadd85b5b8018f75da270085197aed4792bf1c6848628cce02f457d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015193"
---
# <a name="constructing-font-families-and-fonts"></a>Costruzione di famiglie di caratteri e tipi di carattere

Windows GDI+ i tipi di carattere con lo stesso carattere tipografico ma stili diversi in famiglie di caratteri. Ad esempio, la famiglia di caratteri Arial contiene i tipi di carattere seguenti:

-   Arial Regular
-   Arial Bold
-   Corsivo Arial
-   Corsivo grassetto Arial

GDI+ usa quattro stili per formare le famiglie: normale, grassetto, corsivo e corsivo grassetto. Gli aggettivi, ad *esempio narrow* e *rounded,* non sono considerati stili. piuttosto che fanno parte del nome della famiglia. Ad esempio, Arial Narrow è una famiglia di caratteri i cui membri sono i seguenti:

-   Arial Narrow Regular
-   Arial Narrow Bold
-   Arial Narrow Italic
-   Arial Narrow Bold Italic

Prima di poter disegnare testo con GDI+, è necessario costruire un [**oggetto FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) e un [**oggetto Font.**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) Gli **oggetti FontFamily** specificano il carattere tipografico (ad esempio, Arial) e l'oggetto **Font** specifica le dimensioni, lo stile e le unità.

L'esempio seguente costruisce un tipo di carattere Arial di stile normale con dimensioni di 16 pixel:


```
FontFamily fontFamily(L"Arial");
Font font(&fontFamily, 16, FontStyleRegular, UnitPixel);
            
```



Nel codice precedente il primo argomento passato al costruttore [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) è l'indirizzo dell'oggetto [**FontFamily.**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) Il secondo argomento specifica la dimensione del tipo di carattere misurata in unità identificate dal quarto argomento. Il terzo argomento identifica lo stile.

[***UnitPixel****](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-unit) è un membro dell'enumerazione **Unit** e [****FontStyleRegular****](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-fontstyle) è un membro dell'enumerazione **FontStyle.** Entrambe le enumerazioni sono dichiarate in Gdiplusenums.h.

 

 



