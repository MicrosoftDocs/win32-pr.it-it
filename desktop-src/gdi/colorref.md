---
Description: Il valore COLORREF viene usato per specificare un colore RGB.
ms.assetid: b87d3de2-7a13-44ef-8253-c6851a75fa54
title: COLORREF (windef. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 6836cfcc1b18d0b20d5e347fb83206551b27de06
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "104996457"
---
# <a name="colorref"></a><span data-ttu-id="723b4-103">COLORREF</span><span class="sxs-lookup"><span data-stu-id="723b4-103">COLORREF</span></span>

<span data-ttu-id="723b4-104">Il valore COLORREF viene usato per specificare un colore [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) .</span><span class="sxs-lookup"><span data-stu-id="723b4-104">The COLORREF value is used to specify an [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) color.</span></span>


```C++
typedef DWORD COLORREF;
typedef DWORD* LPCOLORREF;
```



## <a name="remarks"></a><span data-ttu-id="723b4-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="723b4-105">Remarks</span></span>

<span data-ttu-id="723b4-106">Quando si specifica un colore [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) esplicito, il valore di **COLORREF** ha il seguente formato esadecimale:</span><span class="sxs-lookup"><span data-stu-id="723b4-106">When specifying an explicit [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) color, the **COLORREF** value has the following hexadecimal form:</span></span>

`0x00bbggrr`

<span data-ttu-id="723b4-107">Il byte di ordine inferiore contiene un valore per l'intensità relativa del rosso; il secondo byte contiene un valore per il verde; e il terzo byte contiene un valore per il blu.</span><span class="sxs-lookup"><span data-stu-id="723b4-107">The low-order byte contains a value for the relative intensity of red; the second byte contains a value for green; and the third byte contains a value for blue.</span></span> <span data-ttu-id="723b4-108">Il byte di ordine superiore deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="723b4-108">The high-order byte must be zero.</span></span> <span data-ttu-id="723b4-109">Il valore massimo per un singolo byte è 0xFF.</span><span class="sxs-lookup"><span data-stu-id="723b4-109">The maximum value for a single byte is 0xFF.</span></span>

<span data-ttu-id="723b4-110">Per creare un valore di colore **COLORREF** , usare la macro [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) .</span><span class="sxs-lookup"><span data-stu-id="723b4-110">To create a **COLORREF** color value, use the [RGB](/windows/desktop/api/Wingdi/nf-wingdi-rgb) macro.</span></span> <span data-ttu-id="723b4-111">Per estrarre i singoli valori per i componenti rosso, verde e blu di un valore di colore, utilizzare rispettivamente le macro [**GetRValue**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue), [GetGValue](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue)e [GetBValue](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue) .</span><span class="sxs-lookup"><span data-stu-id="723b4-111">To extract the individual values for the red, green, and blue components of a color value, use the [**GetRValue**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue), [GetGValue](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue), and [GetBValue](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue) macros, respectively.</span></span>

## <a name="example"></a><span data-ttu-id="723b4-112">Esempio</span><span class="sxs-lookup"><span data-stu-id="723b4-112">Example</span></span>

```cpp
// Color constants.
const COLORREF rgbRed   =  0x000000FF;
const COLORREF rgbGreen =  0x0000FF00;
const COLORREF rgbBlue  =  0x00FF0000;
const COLORREF rgbBlack =  0x00000000;
const COLORREF rgbWhite =  0x00FFFFFF;
```

<span data-ttu-id="723b4-113">Esempio di [esempi di Windows classico](https://github.com/microsoft/Windows-classic-samples) in GitHub.</span><span class="sxs-lookup"><span data-stu-id="723b4-113">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples) on GitHub.</span></span>

## <a name="requirements"></a><span data-ttu-id="723b4-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="723b4-114">Requirements</span></span>



| <span data-ttu-id="723b4-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="723b4-115">Requirement</span></span> | <span data-ttu-id="723b4-116">Valore</span><span class="sxs-lookup"><span data-stu-id="723b4-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="723b4-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="723b4-117">Minimum supported client</span></span><br/> | <span data-ttu-id="723b4-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="723b4-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="723b4-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="723b4-119">Minimum supported server</span></span><br/> | <span data-ttu-id="723b4-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="723b4-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="723b4-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="723b4-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="723b4-122"><dt>Windef. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="723b4-122"><dt>Windef.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="723b4-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="723b4-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="723b4-124">Panoramica sui colori</span><span class="sxs-lookup"><span data-stu-id="723b4-124">Colors Overview</span></span>](colors.md)
</dt> <dt>

[<span data-ttu-id="723b4-125">Strutture colore</span><span class="sxs-lookup"><span data-stu-id="723b4-125">Color Structures</span></span>](color-structures.md)
</dt> <dt>

[<span data-ttu-id="723b4-126">GetBValue</span><span class="sxs-lookup"><span data-stu-id="723b4-126">GetBValue</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue)
</dt> <dt>

[<span data-ttu-id="723b4-127">GetGValue</span><span class="sxs-lookup"><span data-stu-id="723b4-127">GetGValue</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue)
</dt> <dt>

[<span data-ttu-id="723b4-128">**GetRValue**</span><span class="sxs-lookup"><span data-stu-id="723b4-128">**GetRValue**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue)
</dt> <dt>

[<span data-ttu-id="723b4-129">RGB</span><span class="sxs-lookup"><span data-stu-id="723b4-129">RGB</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-rgb)
</dt> </dl>

 

 




