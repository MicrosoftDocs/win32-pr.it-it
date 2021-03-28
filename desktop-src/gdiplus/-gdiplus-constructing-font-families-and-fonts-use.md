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
# <a name="constructing-font-families-and-fonts"></a><span data-ttu-id="538a4-103">Creazione di gruppi di caratteri e tipi di carattere</span><span class="sxs-lookup"><span data-stu-id="538a4-103">Constructing Font Families and Fonts</span></span>

<span data-ttu-id="538a4-104">Windows GDI+ raggruppa i tipi di carattere con lo stesso carattere tipografico ma con stili diversi nelle famiglie di caratteri.</span><span class="sxs-lookup"><span data-stu-id="538a4-104">Windows GDI+ groups fonts with the same typeface but different styles into font families.</span></span> <span data-ttu-id="538a4-105">Ad esempio, la famiglia di caratteri Arial contiene i tipi di carattere seguenti:</span><span class="sxs-lookup"><span data-stu-id="538a4-105">For example, the Arial font family contains the following fonts:</span></span>

-   <span data-ttu-id="538a4-106">Arial Regular</span><span class="sxs-lookup"><span data-stu-id="538a4-106">Arial Regular</span></span>
-   <span data-ttu-id="538a4-107">Arial grassetto</span><span class="sxs-lookup"><span data-stu-id="538a4-107">Arial Bold</span></span>
-   <span data-ttu-id="538a4-108">Arial corsivo</span><span class="sxs-lookup"><span data-stu-id="538a4-108">Arial Italic</span></span>
-   <span data-ttu-id="538a4-109">Arial grassetto corsivo</span><span class="sxs-lookup"><span data-stu-id="538a4-109">Arial Bold Italic</span></span>

<span data-ttu-id="538a4-110">GDI+ utilizza quattro stili per formare famiglie: normale, grassetto, corsivo e grassetto corsivo.</span><span class="sxs-lookup"><span data-stu-id="538a4-110">GDI+ uses four styles to form families: regular, bold, italic, and bold italic.</span></span> <span data-ttu-id="538a4-111">Gli aggettivi come *Narrow* e *arrotondati* non sono considerati stili; ma fanno parte del nome della famiglia.</span><span class="sxs-lookup"><span data-stu-id="538a4-111">Adjectives such as *narrow* and *rounded* are not considered styles; rather they are part of the family name.</span></span> <span data-ttu-id="538a4-112">Ad esempio, Arial Narrow è una famiglia di caratteri i cui membri sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="538a4-112">For example, Arial Narrow is a font family whose members are the following:</span></span>

-   <span data-ttu-id="538a4-113">Arial Narrow Regular</span><span class="sxs-lookup"><span data-stu-id="538a4-113">Arial Narrow Regular</span></span>
-   <span data-ttu-id="538a4-114">Arial Narrow Bold</span><span class="sxs-lookup"><span data-stu-id="538a4-114">Arial Narrow Bold</span></span>
-   <span data-ttu-id="538a4-115">Arial Narrow corsivo</span><span class="sxs-lookup"><span data-stu-id="538a4-115">Arial Narrow Italic</span></span>
-   <span data-ttu-id="538a4-116">Arial Narrow Bold corsivo</span><span class="sxs-lookup"><span data-stu-id="538a4-116">Arial Narrow Bold Italic</span></span>

<span data-ttu-id="538a4-117">Prima di poter creare un testo con GDI+, è necessario creare un oggetto [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) e un oggetto [**font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) .</span><span class="sxs-lookup"><span data-stu-id="538a4-117">Before you can draw text with GDI+, you need to construct a [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) object and a [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) object.</span></span> <span data-ttu-id="538a4-118">Gli oggetti **FontFamily** specificano il carattere tipografico (ad esempio, Arial) e l'oggetto **font** specifica le dimensioni, lo stile e le unità.</span><span class="sxs-lookup"><span data-stu-id="538a4-118">The **FontFamily** objects specifies the typeface (for example, Arial), and the **Font** object specifies the size, style, and units.</span></span>

<span data-ttu-id="538a4-119">Nell'esempio seguente viene costruito un tipo di carattere Arial di stile normale con una dimensione di 16 pixel:</span><span class="sxs-lookup"><span data-stu-id="538a4-119">The following example constructs a regular style Arial font with a size of 16 pixels:</span></span>


```
FontFamily fontFamily(L"Arial");
Font font(&fontFamily, 16, FontStyleRegular, UnitPixel);
            
```



<span data-ttu-id="538a4-120">Nel codice precedente, il primo argomento passato al costruttore del [**tipo di carattere**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) è l'indirizzo dell'oggetto [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) .</span><span class="sxs-lookup"><span data-stu-id="538a4-120">In the preceding code, the first argument passed to the [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) constructor is the address of the [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) object.</span></span> <span data-ttu-id="538a4-121">Il secondo argomento specifica la dimensione del tipo di carattere misurato in unità identificate dal quarto argomento.</span><span class="sxs-lookup"><span data-stu-id="538a4-121">The second argument specifies the size of the font measured in units identified by the fourth argument.</span></span> <span data-ttu-id="538a4-122">Il terzo argomento identifica lo stile.</span><span class="sxs-lookup"><span data-stu-id="538a4-122">The third argument identifies the style.</span></span>

<span data-ttu-id="538a4-123">[\* \* \* \* UnitPixel \* \*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-unit) \* \* è un membro dell'enumerazione di **unità** e [\* \* \* \* FontStyleRegular \* \*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-fontstyle) \* \* è un membro dell'enumerazione **FontStyle** .</span><span class="sxs-lookup"><span data-stu-id="538a4-123">[\*\*\*\*UnitPixel\*\*\*\*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-unit) is a member of the **Unit** enumeration, and [\*\*\*\*FontStyleRegular\*\*\*\*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-fontstyle) is a member of the **FontStyle** enumeration.</span></span> <span data-ttu-id="538a4-124">Entrambe le enumerazioni sono dichiarate in Gdiplusenums. h.</span><span class="sxs-lookup"><span data-stu-id="538a4-124">Both enumerations are declared in Gdiplusenums.h.</span></span>

 

 



