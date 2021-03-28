---
description: Windows GDI+ raggruppa i tipi di carattere con lo stesso carattere tipografico ma con stili diversi nelle famiglie di caratteri.
ms.assetid: 57428fae-6af4-47a5-a499-717dc378767a
title: Creazione di gruppi di caratteri e tipi di carattere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2761923847a15be6b1ad51eec0d683129b70b349
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994296"
---
# <a name="constructing-font-families-and-fonts"></a>Creazione di gruppi di caratteri e tipi di carattere

Windows GDI+ raggruppa i tipi di carattere con lo stesso carattere tipografico ma con stili diversi nelle famiglie di caratteri. Ad esempio, la famiglia di caratteri Arial contiene i tipi di carattere seguenti:

-   Arial Regular
-   Arial grassetto
-   Arial corsivo
-   Arial grassetto corsivo

GDI+ utilizza quattro stili per formare famiglie: normale, grassetto, corsivo e grassetto corsivo. Gli aggettivi come *Narrow* e *arrotondati* non sono considerati stili; ma fanno parte del nome della famiglia. Ad esempio, Arial Narrow è una famiglia di caratteri i cui membri sono i seguenti:

-   Arial Narrow Regular
-   Arial Narrow Bold
-   Arial Narrow corsivo
-   Arial Narrow Bold corsivo

Prima di poter creare un testo con GDI+, è necessario creare un oggetto [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) e un oggetto [**font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) . Gli oggetti **FontFamily** specificano il carattere tipografico (ad esempio, Arial) e l'oggetto **font** specifica le dimensioni, lo stile e le unità.

Nell'esempio seguente viene costruito un tipo di carattere Arial di stile normale con una dimensione di 16 pixel:


```
FontFamily fontFamily(L"Arial");
Font font(&fontFamily, 16, FontStyleRegular, UnitPixel);
            
```



Nel codice precedente, il primo argomento passato al costruttore del [**tipo di carattere**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) è l'indirizzo dell'oggetto [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) . Il secondo argomento specifica la dimensione del tipo di carattere misurato in unità identificate dal quarto argomento. Il terzo argomento identifica lo stile.

[* * * * UnitPixel * *](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-unit) * * è un membro dell'enumerazione di **unità** e [* * * * FontStyleRegular * *](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-fontstyle) * * è un membro dell'enumerazione **FontStyle** . Entrambe le enumerazioni sono dichiarate in Gdiplusenums. h.

 

 



