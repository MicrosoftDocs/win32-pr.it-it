---
title: Istruzione FONT
description: Definisce il tipo di carattere con cui il sistema trarrà il testo nella finestra di dialogo. Il tipo di carattere deve essere stato caricato in precedenza; ad esempio, chiamando la funzione LoadResource.
ms.assetid: d7b0f382-bc45-4405-a30e-0b571fdfd1db
keywords:
- Menu di istruzioni dei tipi di carattere e altre risorse
topic_type:
- apiref
api_name:
- FONT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4b31b280a5a973301e8410f1f74340138af07ba
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104473051"
---
# <a name="font-statement"></a><span data-ttu-id="9fd02-105">Istruzione FONT</span><span class="sxs-lookup"><span data-stu-id="9fd02-105">FONT statement</span></span>

<span data-ttu-id="9fd02-106">Definisce il tipo di carattere con cui il sistema trarrà il testo nella finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="9fd02-106">Defines the font with which the system will draw text in the dialog box.</span></span> <span data-ttu-id="9fd02-107">Il tipo di carattere deve essere stato caricato in precedenza; ad esempio, chiamando la funzione [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) .</span><span class="sxs-lookup"><span data-stu-id="9fd02-107">The font must have been previously loaded; for example, by calling the [**LoadResource**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource) function.</span></span>

``` syntax
FONT pointsize, "typeface", weight, italic, charset
```

<dl> <dt>

<span data-ttu-id="9fd02-108"><span id="pointsize"></span><span id="POINTSIZE"></span>*pointsize*</span><span class="sxs-lookup"><span data-stu-id="9fd02-108"><span id="pointsize"></span><span id="POINTSIZE"></span>*pointsize*</span></span>
</dt> <dd>

<span data-ttu-id="9fd02-109">Dimensioni in punti del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="9fd02-109">The size of the font, in points.</span></span>

</dd> <dt>

<span data-ttu-id="9fd02-110"><span id="typeface"></span><span id="TYPEFACE"></span>*carattere tipografico*</span><span class="sxs-lookup"><span data-stu-id="9fd02-110"><span id="typeface"></span><span id="TYPEFACE"></span>*typeface*</span></span>
</dt> <dd>

<span data-ttu-id="9fd02-111">Nome del carattere tipografico.</span><span class="sxs-lookup"><span data-stu-id="9fd02-111">The name of the typeface.</span></span> <span data-ttu-id="9fd02-112">Questo parametro deve essere racchiuso tra virgolette (").</span><span class="sxs-lookup"><span data-stu-id="9fd02-112">This parameter must be enclosed in quotes (").</span></span>

</dd> <dt>

<span data-ttu-id="9fd02-113"><span id="weight"></span><span id="WEIGHT"></span>*peso*</span><span class="sxs-lookup"><span data-stu-id="9fd02-113"><span id="weight"></span><span id="WEIGHT"></span>*weight*</span></span>
</dt> <dd>

<span data-ttu-id="9fd02-114">Spessore del tipo di carattere nell'intervallo compreso tra 0 e 1000.</span><span class="sxs-lookup"><span data-stu-id="9fd02-114">The weight of the font in the range 0 through 1000.</span></span> <span data-ttu-id="9fd02-115">400, ad esempio, è normale e 700 è in grassetto.</span><span class="sxs-lookup"><span data-stu-id="9fd02-115">For example, 400 is normal and 700 is bold.</span></span> <span data-ttu-id="9fd02-116">Se questo valore è 0, viene utilizzato il peso predefinito.</span><span class="sxs-lookup"><span data-stu-id="9fd02-116">If this value is 0, the default weight is used.</span></span> <span data-ttu-id="9fd02-117">Per un elenco di valori predefiniti, vedere i valori **FW \_ \*** definiti in wingdi. h.</span><span class="sxs-lookup"><span data-stu-id="9fd02-117">For a list of predefined values, see the **FW\_\*** values defined in WinGDI.h.</span></span>

</dd> <dt>

<span data-ttu-id="9fd02-118"><span id="italic"></span><span id="ITALIC"></span>*corsivo*</span><span class="sxs-lookup"><span data-stu-id="9fd02-118"><span id="italic"></span><span id="ITALIC"></span>*italic*</span></span>
</dt> <dd>

<span data-ttu-id="9fd02-119">Indica un tipo di carattere corsivo se impostato su TRUE.</span><span class="sxs-lookup"><span data-stu-id="9fd02-119">Indicates an italic font if set to TRUE.</span></span>

</dd> <dt>

<span data-ttu-id="9fd02-120"><span id="charset"></span><span id="CHARSET"></span>*charset*</span><span class="sxs-lookup"><span data-stu-id="9fd02-120"><span id="charset"></span><span id="CHARSET"></span>*charset*</span></span>
</dt> <dd>

<span data-ttu-id="9fd02-121">Set di caratteri.</span><span class="sxs-lookup"><span data-stu-id="9fd02-121">The character set.</span></span> <span data-ttu-id="9fd02-122">Per un elenco di valori, vedere il membro **lfCharSet** della struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .</span><span class="sxs-lookup"><span data-stu-id="9fd02-122">For a list of values, see the **lfCharSet** member of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="9fd02-123">Esempio</span><span class="sxs-lookup"><span data-stu-id="9fd02-123">Examples</span></span>

<span data-ttu-id="9fd02-124">Nell'esempio seguente viene illustrato l'utilizzo dell'istruzione **font** :</span><span class="sxs-lookup"><span data-stu-id="9fd02-124">The following example demonstrates the use of the **FONT** statement:</span></span>

``` syntax
FONT 12, "MS Shell Dlg"
```

## <a name="see-also"></a><span data-ttu-id="9fd02-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9fd02-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fd02-126">**LoadResource**</span><span class="sxs-lookup"><span data-stu-id="9fd02-126">**LoadResource**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-loadresource)
</dt> </dl>

 

 