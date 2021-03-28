---
description: La classe InstalledFontCollection eredita dalla classe base astratta FontCollection.
ms.assetid: 59598f66-4241-4766-a2f0-5de736de959e
title: Enumerazione dei tipi di carattere installati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f41242522c2575ffb08e53f7100380ac9a849d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227080"
---
# <a name="enumerating-installed-fonts"></a>Enumerazione dei tipi di carattere installati

La classe [**InstalledFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-installedfontcollection) eredita dalla classe base astratta [**FontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection) . È possibile utilizzare un oggetto **InstalledFontCollection** per enumerare i tipi di carattere installati nel computer. Il metodo [**FontCollection:: GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) di un oggetto **InstalledFontCollection** restituisce una matrice di oggetti [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) . Prima di chiamare **FontCollection:: GetFamilies**, è necessario allocare un buffer sufficientemente grande da mantenere tale matrice. Per determinare le dimensioni del buffer richiesto, chiamare il metodo [**FontCollection:: GetFamilyCount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) e moltiplicare il valore restituito da **sizeof**(**FontFamily**).

Nell'esempio seguente vengono elencati i nomi di tutte le famiglie di caratteri installate nel computer. Il codice recupera i nomi delle famiglie di caratteri chiamando il metodo [**FontFamily:: Getfamilianame**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-getfamilyname) di ogni oggetto [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) nella matrice restituita da [**FontCollection:: GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies). Man mano che vengono recuperati, i nomi delle famiglie vengono concatenati per formare un elenco delimitato da virgole. Il metodo [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) della classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) disegna quindi l'elenco delimitato da virgole in un rettangolo.


```
FontFamily   fontFamily(L"Arial");
Font         font(&fontFamily, 8, FontStyleRegular, UnitPoint);
RectF        rectF(10.0f, 10.0f, 500.0f, 500.0f);
SolidBrush   solidBrush(Color(255, 0, 0, 0));

INT          count = 0;
INT          found = 0;
WCHAR        familyName[LF_FACESIZE];  // enough space for one family name
WCHAR*       familyList = NULL;
FontFamily*  pFontFamily = NULL;

InstalledFontCollection installedFontCollection;

// How many font families are installed?
count = installedFontCollection.GetFamilyCount();

// Allocate a buffer to hold the array of FontFamily
// objects returned by GetFamilies.
pFontFamily = new FontFamily[count];

// Get the array of FontFamily objects.
installedFontCollection.GetFamilies(count, pFontFamily, &found);

// The loop below creates a large string that is a comma-separated
// list of all font family names.
// Allocate a buffer large enough to hold that string.
familyList = new WCHAR[count*(sizeof(familyName)+ 3)];
StringCchCopy(familyList, 1, L"");

for(INT j = 0; j < count; ++j)
{
   pFontFamily[j].GetFamilyName(familyName);  
   StringCchCatW(familyList, count*(sizeof(familyName)+ 3), familyName);
   StringCchCatW(familyList, count*(sizeof(familyName)+ 3), L",  ");
}

// Draw the large string (list of all families) in a rectangle.
graphics.DrawString(
   familyList, -1, &font, rectF, NULL, &solidBrush);

delete [] pFontFamily;
delete [] familyList;
            
```



Nella figura seguente viene illustrato un possibile output del codice precedente. Se si esegue il codice, l'output potrebbe essere diverso, a seconda dei tipi di carattere installati nel computer.

![Screenshot di una finestra contenente un elenco delimitato da virgole di famiglie di caratteri installate](images/fontstext6.png)

 

 



