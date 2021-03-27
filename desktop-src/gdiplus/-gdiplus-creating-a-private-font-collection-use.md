---
description: La classe PrivateFontCollection eredita dalla classe base astratta FontCollection. È possibile usare un oggetto PrivateFontCollection per mantenere un set di tipi di carattere specifici per l'applicazione.
ms.assetid: ae12afcf-12cc-4c84-9aba-de56fc39437b
title: Creazione di raccolte private di tipi di carattere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 084e8a2d6f79f60e0719f04fbabb778b9483bd80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227085"
---
# <a name="creating-a-private-font-collection"></a><span data-ttu-id="e9245-104">Creazione di raccolte private di tipi di carattere</span><span class="sxs-lookup"><span data-stu-id="e9245-104">Creating a Private Font Collection</span></span>

<span data-ttu-id="e9245-105">La classe [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) eredita dalla classe base astratta [**FontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection) .</span><span class="sxs-lookup"><span data-stu-id="e9245-105">The [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) class inherits from the [**FontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection) abstract base class.</span></span> <span data-ttu-id="e9245-106">È possibile usare un oggetto **PrivateFontCollection** per mantenere un set di tipi di carattere specifici per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e9245-106">You can use a **PrivateFontCollection** object to maintain a set of fonts specifically for your application.</span></span>

<span data-ttu-id="e9245-107">Una raccolta di tipi di carattere privata può includere i tipi di carattere del sistema installato e i tipi di carattere che non sono stati installati nel computer.</span><span class="sxs-lookup"><span data-stu-id="e9245-107">A private font collection can include installed system fonts as well as fonts that have not been installed on the computer.</span></span> <span data-ttu-id="e9245-108">Per aggiungere un file del tipo di carattere a una raccolta di tipi di carattere privata, chiamare il metodo [**PrivateFontCollection:: AddFontFile**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-privatefontcollection-addfontfile) di un oggetto [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) .</span><span class="sxs-lookup"><span data-stu-id="e9245-108">To add a font file to a private font collection, call the [**PrivateFontCollection::AddFontFile**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-privatefontcollection-addfontfile) method of a [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) object.</span></span>

> [!Note]  
> <span data-ttu-id="e9245-109">Quando si usa l'API GDI+, non è mai necessario consentire all'applicazione di scaricare tipi di carattere arbitrari da origini non attendibili.</span><span class="sxs-lookup"><span data-stu-id="e9245-109">When you use the GDI+ API, you must never allow your application to download arbitrary fonts from untrusted sources.</span></span> <span data-ttu-id="e9245-110">Il sistema operativo richiede privilegi elevati per assicurarsi che tutti i tipi di carattere installati siano attendibili.</span><span class="sxs-lookup"><span data-stu-id="e9245-110">The operating system requires elevated privileges to assure that all installed fonts are trusted.</span></span>

 

<span data-ttu-id="e9245-111">Il metodo [**FontCollection:: GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) di un oggetto [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) restituisce una matrice di oggetti [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) .</span><span class="sxs-lookup"><span data-stu-id="e9245-111">The [**FontCollection::GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) method of a [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) object returns an array of [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) objects.</span></span> <span data-ttu-id="e9245-112">Prima di chiamare **FontCollection:: GetFamilies**, è necessario allocare un buffer sufficientemente grande da mantenere tale matrice.</span><span class="sxs-lookup"><span data-stu-id="e9245-112">Before you call **FontCollection::GetFamilies**, you must allocate a buffer large enough to hold that array.</span></span> <span data-ttu-id="e9245-113">Per determinare le dimensioni del buffer richiesto, chiamare il metodo [**FontCollection:: GetFamilyCount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) e moltiplicare il valore restituito da **sizeof**(**FontFamily**).</span><span class="sxs-lookup"><span data-stu-id="e9245-113">To determine the size of the required buffer, call the [**FontCollection::GetFamilyCount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) method and multiply the return value by **sizeof**(**FontFamily**).</span></span>

<span data-ttu-id="e9245-114">Il numero di famiglie di caratteri in una raccolta di tipi di carattere privata non è necessariamente uguale al numero di file del tipo di carattere aggiunti alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="e9245-114">The number of font families in a private font collection is not necessarily the same as the number of font files that have been added to the collection.</span></span> <span data-ttu-id="e9245-115">Si supponga, ad esempio, di aggiungere i file ArialBd. TFF, Times. tff e TimesBd. TFF a una raccolta.</span><span class="sxs-lookup"><span data-stu-id="e9245-115">For example, suppose you add the files ArialBd.tff, Times.tff, and TimesBd.tff to a collection.</span></span> <span data-ttu-id="e9245-116">Saranno presenti tre file, ma solo due famiglie della raccolta, poiché Times. tff e TimesBd. tff appartengono alla stessa famiglia.</span><span class="sxs-lookup"><span data-stu-id="e9245-116">There will be three files but only two families in the collection because Times.tff and TimesBd.tff belong to the same family.</span></span>

<span data-ttu-id="e9245-117">Nell'esempio seguente vengono aggiunti i tre file del tipo di carattere seguenti a un oggetto [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) :</span><span class="sxs-lookup"><span data-stu-id="e9245-117">The following example adds the following three font files to a [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) object:</span></span>

-   <span data-ttu-id="e9245-118">C: \\ WinNT \\ fonts \\ Arial. tff (Arial, Regular)</span><span class="sxs-lookup"><span data-stu-id="e9245-118">C:\\WINNT\\Fonts\\Arial.tff (Arial, regular)</span></span>
-   <span data-ttu-id="e9245-119">C: \\ WinNT \\ fonts \\ Courbi. tff (Courier New, Bold Italic)</span><span class="sxs-lookup"><span data-stu-id="e9245-119">C:\\WINNT\\Fonts\\CourBI.tff (Courier New, bold italic)</span></span>
-   <span data-ttu-id="e9245-120">C: \\ WinNT \\ fonts \\ TimesBd. tff (Times New Roman, Bold)</span><span class="sxs-lookup"><span data-stu-id="e9245-120">C:\\WINNT\\Fonts\\TimesBd.tff (Times New Roman, bold)</span></span>

<span data-ttu-id="e9245-121">Il codice chiama il metodo [**FontCollection:: GetFamilyCount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) dell'oggetto [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) per determinare il numero di famiglie nella raccolta privata, quindi chiama [**FontCollection:: GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) per recuperare una matrice di oggetti [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) .</span><span class="sxs-lookup"><span data-stu-id="e9245-121">The code calls the [**FontCollection::GetFamilyCount**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilycount) method of the [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) object to determine the number of families in the private collection, and then calls [**FontCollection::GetFamilies**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontcollection-getfamilies) to retrieve an array of [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) objects.</span></span>

<span data-ttu-id="e9245-122">Per ogni oggetto [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) della raccolta, il codice chiama il metodo [**FontFamily:: IsStyleAvailable**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-isstyleavailable) per determinare se sono disponibili diversi stili (Regular, Bold, Italic, Bold Italic, Underline e Strike).</span><span class="sxs-lookup"><span data-stu-id="e9245-122">For each [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) object in the collection, the code calls the [**FontFamily::IsStyleAvailable**](/windows/win32/api/Gdiplusheaders/nf-gdiplusheaders-fontfamily-isstyleavailable) method to determine whether various styles (regular, bold, italic, bold italic, underline, and strikeout) are available.</span></span> <span data-ttu-id="e9245-123">Gli argomenti passati al metodo **FontFamily:: IsStyleAvailable** sono membri dell'enumerazione [**FontStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-fontstyle) , dichiarata in Gdiplusenums. h.</span><span class="sxs-lookup"><span data-stu-id="e9245-123">The arguments passed to the **FontFamily::IsStyleAvailable** method are members of the [**FontStyle**](/windows/win32/api/Gdiplusenums/ne-gdiplusenums-fontstyle) enumeration, which is declared in Gdiplusenums.h.</span></span>

<span data-ttu-id="e9245-124">Se è disponibile una particolare combinazione di famiglia/stile, viene creato un oggetto del [**tipo di carattere**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) usando tale famiglia e stile.</span><span class="sxs-lookup"><span data-stu-id="e9245-124">If a particular family/style combination is available, a [**Font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) object is constructed using that family and style.</span></span> <span data-ttu-id="e9245-125">Il primo argomento passato al costruttore del **tipo di carattere** è il nome della famiglia di caratteri (non un oggetto [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) come nel caso di altre varianti del costruttore del **tipo di carattere** ) e l'argomento finale è l'indirizzo dell'oggetto [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) .</span><span class="sxs-lookup"><span data-stu-id="e9245-125">The first argument passed to the **Font** constructor is the font family name (not a [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) object as is the case for other variations of the **Font** constructor), and the final argument is the address of the [**PrivateFontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-privatefontcollection) object.</span></span> <span data-ttu-id="e9245-126">Dopo la creazione dell'oggetto **font** , il relativo indirizzo viene passato al metodo [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) della classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) per visualizzare il nome della famiglia insieme al nome dello stile.</span><span class="sxs-lookup"><span data-stu-id="e9245-126">After the **Font** object is constructed, its address is passed to the [DrawString](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class to display the family name along with the name of the style.</span></span>


```
#define MAX_STYLE_SIZE 20
#define MAX_FACEANDSTYLE_SIZE (LF_FACESIZE + MAX_STYLE_SIZE + 2)

PointF      pointF(10.0f, 0.0f);
SolidBrush  solidBrush(Color(255, 0, 0, 0));
INT                   count = 0;
INT                   found = 0;
WCHAR                 familyName[LF_FACESIZE];
WCHAR                 familyNameAndStyle[MAX_FACEANDSTYLE_SIZE]; 
FontFamily*           pFontFamily;
PrivateFontCollection privateFontCollection;

// Add three font files to the private collection.
privateFontCollection.AddFontFile(L"c:\\Winnt\\Fonts\\Arial.ttf");
privateFontCollection.AddFontFile(L"c:\\Winnt\\Fonts\\CourBI.ttf");
privateFontCollection.AddFontFile(L"c:\\Winnt\\Fonts\\TimesBd.ttf");

// How many font families are in the private collection?
count = privateFontCollection.GetFamilyCount();

// Allocate a buffer to hold the array of FontFamily
// objects returned by GetFamilies.
pFontFamily = new FontFamily[count];

// Get the array of FontFamily objects.
privateFontCollection.GetFamilies(count, pFontFamily, &found);

// Display the name of each font family in the private collection
// along with the available styles for that font family.
for(INT j = 0; j < count; ++j)
{
   // Get the font family name.
   pFontFamily[j].GetFamilyName(familyName);
   
   // Is the regular style available?
   if(pFontFamily[j].IsStyleAvailable(FontStyleRegular))
   {
      StringCchCopyW(familyNameAndStyle, LF_FACESIZE, familyName);
      StringCchCatW(familyNameAndStyle, MAX_FACEANDSTYLE_SIZE, L" Regular");

      Font* pFont = new Font(
         familyName, 16, FontStyleRegular, UnitPixel, &privateFontCollection);

      graphics.DrawString(familyNameAndStyle, -1, pFont, pointF, &solidBrush);

      pointF.Y += pFont->GetHeight(0.0f);
      delete(pFont);      
   }

   // Is the bold style available?
   if(pFontFamily[j].IsStyleAvailable(FontStyleBold))
   {
      StringCchCopyW(familyNameAndStyle, LF_FACESIZE, familyName);
      StringCchCatW(familyNameAndStyle, MAX_FACEANDSTYLE_SIZE, L" Bold");

      Font* pFont = new Font(
         familyName, 16, FontStyleBold, UnitPixel, &privateFontCollection);

      graphics.DrawString(familyNameAndStyle, -1, pFont, pointF, &solidBrush);

      pointF.Y += pFont->GetHeight(0.0f);
      delete(pFont);
   }

   // Is the italic style available?
   if(pFontFamily[j].IsStyleAvailable(FontStyleItalic))
   {
      StringCchCopyW(familyNameAndStyle, LF_FACESIZE, familyName);
      StringCchCatW(familyNameAndStyle, MAX_FACEANDSTYLE_SIZE, L" Italic");

      Font* pFont = new Font(
         familyName, 16, FontStyleItalic, UnitPixel, &privateFontCollection);

      graphics.DrawString(familyNameAndStyle, -1, pFont, pointF, &solidBrush);

      pointF.Y += pFont->GetHeight(0.0f);
      delete(pFont);
   }

   // Is the bold italic style available?
   if(pFontFamily[j].IsStyleAvailable(FontStyleBoldItalic))
   {
      StringCchCopyW(familyNameAndStyle, LF_FACESIZE, familyName);
      StringCchCatW(familyNameAndStyle, MAX_FACEANDSTYLE_SIZE, L" BoldItalic");

      Font* pFont = new Font(familyName, 16, 
         FontStyleBoldItalic, UnitPixel, &privateFontCollection);

      graphics.DrawString(familyNameAndStyle, -1, pFont, pointF, &solidBrush);

      pointF.Y += pFont->GetHeight(0.0f);
      delete(pFont);
    }

   // Is the underline style available?
   if(pFontFamily[j].IsStyleAvailable(FontStyleUnderline))
   {
      StringCchCopyW(familyNameAndStyle, LF_FACESIZE, familyName);
      StringCchCatW(familyNameAndStyle, MAX_FACEANDSTYLE_SIZE, L" Underline");

      Font* pFont = new Font(familyName, 16, 
         FontStyleUnderline, UnitPixel, &privateFontCollection);

      graphics.DrawString(familyNameAndStyle, -1, pFont, pointF, &solidBrush);

      pointF.Y += pFont->GetHeight(0.0);
      delete(pFont);
   }
 
   // Is the strikeout style available?
   if(pFontFamily[j].IsStyleAvailable(FontStyleStrikeout))
   {
      StringCchCopyW(familyNameAndStyle, LF_FACESIZE, familyName);
      StringCchCatW(familyNameAndStyle, MAX_FACEANDSTYLE_SIZE, L" Strikeout");

      Font* pFont = new Font(familyName, 16, 
         FontStyleStrikeout, UnitPixel, &privateFontCollection);

      graphics.DrawString(familyNameAndStyle, -1, pFont, pointF, &solidBrush);

      pointF.Y += pFont->GetHeight(0.0f);
      delete(pFont);
   }

   // Separate the families with white space.
   pointF.Y += 10.0f;

} // for

delete pFontFamily;
            
```



<span data-ttu-id="e9245-127">Nella figura seguente viene illustrato l'output del codice precedente.</span><span class="sxs-lookup"><span data-stu-id="e9245-127">The following illustration shows the output of the preceding code.</span></span>

![Screenshot di una finestra in cui sono elencati nove nomi di caratteri, ognuno dei quali illustra il tipo di carattere denominato](images/fontstext7.png)

<span data-ttu-id="e9245-129">Arial. TFF, che è stato aggiunto alla raccolta di tipi di carattere privati nell'esempio di codice precedente, è il file del tipo di carattere per lo stile normale Arial.</span><span class="sxs-lookup"><span data-stu-id="e9245-129">Arial.tff (which was added to the private font collection in the preceding code example) is the font file for the Arial regular style.</span></span> <span data-ttu-id="e9245-130">Si noti, tuttavia, che l'output del programma mostra diversi stili disponibili diversi da Regular per la famiglia di caratteri Arial.</span><span class="sxs-lookup"><span data-stu-id="e9245-130">Note, however, that the program output shows several available styles other than regular for the Arial font family.</span></span> <span data-ttu-id="e9245-131">Ciò è dovuto al fatto che Windows GDI+ è in grado di simulare gli stili in grassetto, corsivo e corsivo in grassetto dallo stile normale.</span><span class="sxs-lookup"><span data-stu-id="e9245-131">That is because Windows GDI+ can simulate the bold, italic, and bold italic styles from the regular style.</span></span> <span data-ttu-id="e9245-132">GDI+ può inoltre produrre sottolineature e strikeouts dallo stile normale.</span><span class="sxs-lookup"><span data-stu-id="e9245-132">GDI+ can also produce underlines and strikeouts from the regular style.</span></span>

<span data-ttu-id="e9245-133">Analogamente, GDI+ è in grado di simulare lo stile corsivo grassetto dallo stile grassetto o corsivo.</span><span class="sxs-lookup"><span data-stu-id="e9245-133">Similarly, GDI+ can simulate the bold italic style from either the bold style or the italic style.</span></span> <span data-ttu-id="e9245-134">L'output del programma mostra che lo stile corsivo in grassetto è disponibile per la famiglia Times anche se TimesBd. tff (Times New Roman, Bold) è l'unico file di volte nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="e9245-134">The program output shows that the bold italic style is available for the Times family even though TimesBd.tff (Times New Roman, bold) is the only Times file in the collection.</span></span>

<span data-ttu-id="e9245-135">Questa tabella specifica i tipi di carattere non di sistema supportati da GDI+.</span><span class="sxs-lookup"><span data-stu-id="e9245-135">This table specifies the non-system fonts that GDI+ supports.</span></span>



|                     | <span data-ttu-id="e9245-136">GDI</span><span class="sxs-lookup"><span data-stu-id="e9245-136">GDI</span></span> | <span data-ttu-id="e9245-137">GDI+ in Windows 7</span><span class="sxs-lookup"><span data-stu-id="e9245-137">GDI+ on Windows 7</span></span> | <span data-ttu-id="e9245-138">GDI+ in Windows 8</span><span class="sxs-lookup"><span data-stu-id="e9245-138">GDI+ on Windows 8</span></span> | <span data-ttu-id="e9245-139">DirectWrite</span><span class="sxs-lookup"><span data-stu-id="e9245-139">DirectWrite</span></span> |
|---------------------|-----|-------------------|-------------------|-------------|
| <span data-ttu-id="e9245-140">. FON</span><span class="sxs-lookup"><span data-stu-id="e9245-140">.FON</span></span>                | <span data-ttu-id="e9245-141">sì</span><span class="sxs-lookup"><span data-stu-id="e9245-141">yes</span></span> | <span data-ttu-id="e9245-142">no</span><span class="sxs-lookup"><span data-stu-id="e9245-142">no</span></span>                | <span data-ttu-id="e9245-143">no</span><span class="sxs-lookup"><span data-stu-id="e9245-143">no</span></span>                | <span data-ttu-id="e9245-144">no</span><span class="sxs-lookup"><span data-stu-id="e9245-144">no</span></span>          |
| <span data-ttu-id="e9245-145">. FNT</span><span class="sxs-lookup"><span data-stu-id="e9245-145">.FNT</span></span>                | <span data-ttu-id="e9245-146">sì</span><span class="sxs-lookup"><span data-stu-id="e9245-146">yes</span></span> | <span data-ttu-id="e9245-147">no</span><span class="sxs-lookup"><span data-stu-id="e9245-147">no</span></span>                | <span data-ttu-id="e9245-148">no</span><span class="sxs-lookup"><span data-stu-id="e9245-148">no</span></span>                | <span data-ttu-id="e9245-149">no</span><span class="sxs-lookup"><span data-stu-id="e9245-149">no</span></span>          |
| <span data-ttu-id="e9245-150">. TTF</span><span class="sxs-lookup"><span data-stu-id="e9245-150">.TTF</span></span>                | <span data-ttu-id="e9245-151">sì</span><span class="sxs-lookup"><span data-stu-id="e9245-151">yes</span></span> | <span data-ttu-id="e9245-152">sì</span><span class="sxs-lookup"><span data-stu-id="e9245-152">yes</span></span>               | <span data-ttu-id="e9245-153">sì</span><span class="sxs-lookup"><span data-stu-id="e9245-153">yes</span></span>               | <span data-ttu-id="e9245-154">sì</span><span class="sxs-lookup"><span data-stu-id="e9245-154">yes</span></span>         |
| <span data-ttu-id="e9245-155">. OTF con TrueType</span><span class="sxs-lookup"><span data-stu-id="e9245-155">.OTF with TrueType</span></span>  | <span data-ttu-id="e9245-156">sì</span><span class="sxs-lookup"><span data-stu-id="e9245-156">yes</span></span> | <span data-ttu-id="e9245-157">sì</span><span class="sxs-lookup"><span data-stu-id="e9245-157">yes</span></span>               | <span data-ttu-id="e9245-158">sì</span><span class="sxs-lookup"><span data-stu-id="e9245-158">yes</span></span>               | <span data-ttu-id="e9245-159">sì</span><span class="sxs-lookup"><span data-stu-id="e9245-159">yes</span></span>         |
| <span data-ttu-id="e9245-160">. OTF con Adobe CFF</span><span class="sxs-lookup"><span data-stu-id="e9245-160">.OTF with Adobe CFF</span></span> | <span data-ttu-id="e9245-161">sì</span><span class="sxs-lookup"><span data-stu-id="e9245-161">yes</span></span> | <span data-ttu-id="e9245-162">no</span><span class="sxs-lookup"><span data-stu-id="e9245-162">no</span></span>                | <span data-ttu-id="e9245-163">sì</span><span class="sxs-lookup"><span data-stu-id="e9245-163">yes</span></span>               | <span data-ttu-id="e9245-164">sì</span><span class="sxs-lookup"><span data-stu-id="e9245-164">yes</span></span>         |
| <span data-ttu-id="e9245-165">Adobe Type 1</span><span class="sxs-lookup"><span data-stu-id="e9245-165">Adobe Type 1</span></span>        | <span data-ttu-id="e9245-166">sì</span><span class="sxs-lookup"><span data-stu-id="e9245-166">yes</span></span> | <span data-ttu-id="e9245-167">no</span><span class="sxs-lookup"><span data-stu-id="e9245-167">no</span></span>                | <span data-ttu-id="e9245-168">no</span><span class="sxs-lookup"><span data-stu-id="e9245-168">no</span></span>                | <span data-ttu-id="e9245-169">no</span><span class="sxs-lookup"><span data-stu-id="e9245-169">no</span></span>          |



 

 

 



