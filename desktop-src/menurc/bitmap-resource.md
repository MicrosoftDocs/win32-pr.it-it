---
title: Risorsa BITMAP
description: Definisce una bitmap utilizzata da un'applicazione nella visualizzazione dello schermo o come elemento in un menu o un controllo.
ms.assetid: 2db2f7f0-735f-4aac-9813-c04a2f7788b2
keywords:
- Menu delle risorse BITMAP e altre risorse
topic_type:
- apiref
api_name:
- BITMAP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e5bed33fb66d9deb85e1f25165f3f7a0f664961
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398919"
---
# <a name="bitmap-resource"></a><span data-ttu-id="d8d4f-104">Risorsa BITMAP</span><span class="sxs-lookup"><span data-stu-id="d8d4f-104">BITMAP resource</span></span>

<span data-ttu-id="d8d4f-105">Definisce una bitmap utilizzata da un'applicazione nella visualizzazione dello schermo o come elemento in un menu o un controllo.</span><span class="sxs-lookup"><span data-stu-id="d8d4f-105">Defines a bitmap that an application uses in its screen display or as an item in a menu or control.</span></span>

``` syntax
nameID BITMAP filename
```

## <a name="parameters"></a><span data-ttu-id="d8d4f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d8d4f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8d4f-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="d8d4f-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="d8d4f-108">Nome univoco o valore di Unsigned Integer a 16 bit che identifica la risorsa.</span><span class="sxs-lookup"><span data-stu-id="d8d4f-108">Unique name or a 16-bit unsigned integer value identifying the resource.</span></span>

</dd> <dt>

<span data-ttu-id="d8d4f-109"><span id="filename"></span><span id="FILENAME"></span>*filename*</span><span class="sxs-lookup"><span data-stu-id="d8d4f-109"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="d8d4f-110">Nome del file che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="d8d4f-110">Name of the file that contains the resource.</span></span> <span data-ttu-id="d8d4f-111">Il nome deve essere un nome di file valido. deve essere un percorso completo se il file non si trova nella directory di lavoro corrente.</span><span class="sxs-lookup"><span data-stu-id="d8d4f-111">The name must be a valid file name; it must be a full path if the file is not in the current working directory.</span></span> <span data-ttu-id="d8d4f-112">Il percorso deve essere una stringa racchiusa tra virgolette.</span><span class="sxs-lookup"><span data-stu-id="d8d4f-112">The path should be a quoted string.</span></span>

</dd> </dl>

<span data-ttu-id="d8d4f-113">Alcuni attributi sono supportati anche per la compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="d8d4f-113">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="d8d4f-114">Per altre informazioni, vedere [attributi di risorse comuni](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="d8d4f-114">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="examples"></a><span data-ttu-id="d8d4f-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="d8d4f-115">Examples</span></span>

<span data-ttu-id="d8d4f-116">Nell'esempio seguente vengono definite due risorse bitmap:</span><span class="sxs-lookup"><span data-stu-id="d8d4f-116">The following example defines two bitmap resources:</span></span>

``` syntax
disk1   BITMAP "disk.bmp"
12      BITMAP "diskette.bmp"
```

## <a name="see-also"></a><span data-ttu-id="d8d4f-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d8d4f-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8d4f-118">Uso di bitmap</span><span class="sxs-lookup"><span data-stu-id="d8d4f-118">Using Bitmaps</span></span>](/windows/desktop/gdi/using-bitmaps)
</dt> <dt>

[<span data-ttu-id="d8d4f-119">**LoadBitmap**</span><span class="sxs-lookup"><span data-stu-id="d8d4f-119">**LoadBitmap**</span></span>](/windows/desktop/api/winuser/nf-winuser-loadbitmapa)
</dt> <dt>

[<span data-ttu-id="d8d4f-120">**LoadImage**</span><span class="sxs-lookup"><span data-stu-id="d8d4f-120">**LoadImage**</span></span>](/windows/desktop/api/Winuser/nf-winuser-loadimagea)
</dt> </dl>

 

 