---
description: Questo argomento elenca i metodi DrawString della classe Graphics. Per un elenco completo dei metodi per la classe graphics, vedere Graphics.
ms.assetid: b3568ed9-e359-4916-a83d-7553c021d197
title: Metodi Graphics. DrawString (Gdiplusgraphics. h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 275c256ec2c7284401d37794bccf368538cbdd80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "104982995"
---
# <a name="graphicsdrawstring-methods"></a><span data-ttu-id="33c93-104">Metodi Graphics. DrawString</span><span class="sxs-lookup"><span data-stu-id="33c93-104">Graphics.DrawString methods</span></span>

<span data-ttu-id="33c93-105">Questo argomento elenca i metodi DrawString della classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="33c93-105">This topic lists the DrawString methods of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="33c93-106">Per un elenco completo dei metodi per la classe **Graphics** , vedere [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics).</span><span class="sxs-lookup"><span data-stu-id="33c93-106">For a complete list of methods for the **Graphics** class, see [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics).</span></span>

### <a name="overload-list"></a><span data-ttu-id="33c93-107">Elenco di overload</span><span class="sxs-lookup"><span data-stu-id="33c93-107">Overload list</span></span>



| <span data-ttu-id="33c93-108">Metodo</span><span class="sxs-lookup"><span data-stu-id="33c93-108">Method</span></span>                                                                                                                                                       | <span data-ttu-id="33c93-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="33c93-109">Description</span></span>                                                                                                                                                                                                   |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33c93-110">[**DrawString (WCHAR \* , int, Font \* , PointF&, Brush \* )**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush))</span><span class="sxs-lookup"><span data-stu-id="33c93-110">[**DrawString(WCHAR\*,INT,Font\*,PointF&,Brush\*)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush))</span></span>                                | <span data-ttu-id="33c93-111">Il metodo [**Graphics::D RawString**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) disegna una stringa basata su un tipo di carattere e un'origine per la stringa.</span><span class="sxs-lookup"><span data-stu-id="33c93-111">The [**Graphics::DrawString**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)) method draws a string based on a font and an origin for the string.</span></span><br/>                        |
| <span data-ttu-id="33c93-112">[**DrawString (WCHAR \* , int, Font \* , RectF&, StringFormat \* , Brush \* )**](/previous-versions//ms535991(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="33c93-112">[**DrawString(WCHAR\*,INT,Font\*,RectF&,StringFormat\*,Brush\*)**](/previous-versions//ms535991(v=vs.85))</span></span> | <span data-ttu-id="33c93-113">Il metodo [**Graphics::D RawString**](/previous-versions//ms535991(v=vs.85)) disegna una stringa basata su un tipo di carattere, un rettangolo di layout e un formato.</span><span class="sxs-lookup"><span data-stu-id="33c93-113">The [**Graphics::DrawString**](/previous-versions//ms535991(v=vs.85)) method draws a string based on a font, a layout rectangle, and a format.</span></span> <br/> |
| <span data-ttu-id="33c93-114">[**DrawString (WCHAR \* , int, Font \* , PointF&, StringFormat \* , Brush \* )**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush))</span><span class="sxs-lookup"><span data-stu-id="33c93-114">[**DrawString(WCHAR\*,INT,Font\*,PointF&,StringFormat\*,Brush\*)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush))</span></span>    | <span data-ttu-id="33c93-115">Il metodo [**Graphics::D RawString**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) disegna una stringa basata su un tipo di carattere, un'origine di stringa e un formato.</span><span class="sxs-lookup"><span data-stu-id="33c93-115">The [**Graphics::DrawString**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__conststringformat_constbrush)) method draws a string based on a font, a string origin, and a format.</span></span><br/>         |



## <a name="requirements"></a><span data-ttu-id="33c93-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="33c93-116">Requirements</span></span>



| <span data-ttu-id="33c93-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="33c93-117">Requirement</span></span> | <span data-ttu-id="33c93-118">Valore</span><span class="sxs-lookup"><span data-stu-id="33c93-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="33c93-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="33c93-119">Header</span></span><br/> | <dl> <span data-ttu-id="33c93-120"><dt>Gdiplusgraphics. h</dt></span><span class="sxs-lookup"><span data-stu-id="33c93-120"><dt>Gdiplusgraphics.h</dt></span></span> </dl> |



 

 
