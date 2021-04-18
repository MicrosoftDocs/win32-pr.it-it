---
title: Risorsa cursore
description: Definisce una bitmap che definisce la forma del cursore sulla schermata di visualizzazione o su un cursore animato.
ms.assetid: c087abca-5502-4625-8c9b-464e1718571f
keywords:
- Menu delle risorse del cursore e altre risorse
topic_type:
- apiref
api_name:
- CURSOR
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 594f406420b3b18f88b8890ca4248345ba77fa8e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299682"
---
# <a name="cursor-resource"></a><span data-ttu-id="f9395-104">Risorsa cursore</span><span class="sxs-lookup"><span data-stu-id="f9395-104">CURSOR resource</span></span>

<span data-ttu-id="f9395-105">Definisce una bitmap che definisce la forma del cursore sulla schermata di visualizzazione o su un cursore animato.</span><span class="sxs-lookup"><span data-stu-id="f9395-105">Defines a bitmap that defines the shape of the cursor on the display screen or an animated cursor.</span></span>

``` syntax
nameID CURSOR filename
```

## <a name="parameters"></a><span data-ttu-id="f9395-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f9395-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9395-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span><span class="sxs-lookup"><span data-stu-id="f9395-107"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="f9395-108">Nome univoco o Unsigned Integer a 16 bit che identifica la risorsa.</span><span class="sxs-lookup"><span data-stu-id="f9395-108">Unique name or a 16-bit unsigned integer identifying the resource.</span></span>

</dd> <dt>

<span data-ttu-id="f9395-109"><span id="filename"></span><span id="FILENAME"></span>*filename*</span><span class="sxs-lookup"><span data-stu-id="f9395-109"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="f9395-110">Nome del file che contiene la risorsa.</span><span class="sxs-lookup"><span data-stu-id="f9395-110">Name of the file that contains the resource.</span></span> <span data-ttu-id="f9395-111">Il nome deve essere un nome di file valido. deve essere un percorso completo se il file non si trova nella directory di lavoro corrente.</span><span class="sxs-lookup"><span data-stu-id="f9395-111">The name must be a valid file name; it must be a full path if the file is not in the current working directory.</span></span> <span data-ttu-id="f9395-112">Il percorso deve essere una stringa racchiusa tra virgolette.</span><span class="sxs-lookup"><span data-stu-id="f9395-112">The path should be a quoted string.</span></span>

</dd> </dl>

<span data-ttu-id="f9395-113">Alcuni attributi sono supportati anche per la compatibilità con le versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="f9395-113">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="f9395-114">Per altre informazioni, vedere [attributi di risorse comuni](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="f9395-114">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f9395-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="f9395-115">Remarks</span></span>

<span data-ttu-id="f9395-116">Le risorse icona e cursore possono contenere più di un'immagine.</span><span class="sxs-lookup"><span data-stu-id="f9395-116">Icon and cursor resources can contain more than one image.</span></span>

## <a name="examples"></a><span data-ttu-id="f9395-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="f9395-117">Examples</span></span>

<span data-ttu-id="f9395-118">Nell'esempio seguente vengono definite due risorse cursore. uno per nome (Cursor1) e l'altro per numero (2):</span><span class="sxs-lookup"><span data-stu-id="f9395-118">The following example defines two cursor resources; one by name (cursor1) and the other by number (2):</span></span>

``` syntax
cursor1 CURSOR "bullseye.cur"
2       CURSOR "d:\\cursor\\arrow.cur" 
```

## <a name="see-also"></a><span data-ttu-id="f9395-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f9395-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9395-120">Uso dei cursori</span><span class="sxs-lookup"><span data-stu-id="f9395-120">Using Cursors</span></span>](./using-cursors.md)
</dt> </dl>

 

 