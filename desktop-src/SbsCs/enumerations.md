---
description: Informazioni sulle enumerazioni usate nell'API assembly side-by-side, ad esempio ASM_CMP_FLAGS e CREATE_ASM_NAME_OBJ_FLAGS.
ms.assetid: e73c37e3-7879-4754-b39c-91be64fc8d73
title: Enumerazioni di assembly side-by-side
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52f393ab9d8657ecaa52cad555dad5a831699687
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404744"
---
# <a name="side-by-side-assembly-enumerations"></a><span data-ttu-id="9df5f-103">Enumerazioni di assembly side-by-side</span><span class="sxs-lookup"><span data-stu-id="9df5f-103">Side-by-Side Assembly Enumerations</span></span>

<span data-ttu-id="9df5f-104">L'API dell'assembly side-by-side usa le enumerazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="9df5f-104">The side-by-side assembly API uses the following enumerations.</span></span>



| <span data-ttu-id="9df5f-105">Enumerazione</span><span class="sxs-lookup"><span data-stu-id="9df5f-105">Enumeration</span></span>                                                         | <span data-ttu-id="9df5f-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9df5f-106">Description</span></span>                                                                                                                                                                                |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9df5f-107">**FLAG \_ CMP ASM \_**</span><span class="sxs-lookup"><span data-stu-id="9df5f-107">**ASM\_CMP\_FLAGS**</span></span>](/windows/win32/api/winsxs/ne-winsxs-asm_cmp_flags)                           | <span data-ttu-id="9df5f-108">Utilizzato dal metodo [**IsEqual**](/windows/desktop/api/winsxs/nf-winsxs-iassemblyname-isequal) per specificare le parti di due nomi di assembly da confrontare.</span><span class="sxs-lookup"><span data-stu-id="9df5f-108">Used by the [**IsEqual**](/windows/desktop/api/winsxs/nf-winsxs-iassemblyname-isequal) method to specify which parts of two assembly names to compare.</span></span>                                                                       |
| [<span data-ttu-id="9df5f-109">**FLAG DI VISUALIZZAZIONE ASM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9df5f-109">**ASM\_DISPLAY\_FLAGS**</span></span>](/windows/win32/api/winsxs/ne-winsxs-asm_display_flags)                   | <span data-ttu-id="9df5f-110">Usato dal [**metodo GetDisplayName**](/windows/desktop/api/winsxs/nf-winsxs-iassemblyname-getdisplayname) per specificare le parti del nome dell'assembly side-by-side da includere nella rappresentazione di stringa del nome.</span><span class="sxs-lookup"><span data-stu-id="9df5f-110">Used by the [**GetDisplayName**](/windows/desktop/api/winsxs/nf-winsxs-iassemblyname-getdisplayname) method to specify which portions of the side-by-side assembly name to include in the string representation of the name.</span></span> |
| [<span data-ttu-id="9df5f-111">**NOME \_ ASM**</span><span class="sxs-lookup"><span data-stu-id="9df5f-111">**ASM\_NAME**</span></span>](/windows/win32/api/winsxs/ne-winsxs-asm_name)                                      | <span data-ttu-id="9df5f-112">ID di proprietà per le coppie nome-valore in un nome di assembly side-by-side.</span><span class="sxs-lookup"><span data-stu-id="9df5f-112">Property IDs for the name-value pairs in an side-by-side assembly name.</span></span>                                                                                                                    |
| [<span data-ttu-id="9df5f-113">**CREATE \_ ASM \_ NAME \_ OBJ \_ FLAGS**</span><span class="sxs-lookup"><span data-stu-id="9df5f-113">**CREATE\_ASM\_NAME\_OBJ\_FLAGS**</span></span>](/windows/win32/api/winsxs/ne-winsxs-create_asm_name_obj_flags) | <span data-ttu-id="9df5f-114">Usato dalla [**funzione CreateAssemblyNameObject**](/windows/desktop/api/Winsxs/nf-winsxs-createassemblynameobject) per specificare il nome dell'assembly side-by-side.</span><span class="sxs-lookup"><span data-stu-id="9df5f-114">Used by the [**CreateAssemblyNameObject**](/windows/desktop/api/Winsxs/nf-winsxs-createassemblynameobject) function to specify the side-by-side assembly name.</span></span>                                                               |



 

 

 



