---
title: requestedit (attributo)
description: L'attributo \ requestedit \ indica che la proprietà supporta la notifica OnRequestEdit.
ms.assetid: 63f38d83-596b-4031-bb6a-972374cd0c60
keywords:
- attributo MIDL di requestedit
topic_type:
- apiref
api_name:
- requestedit
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18d83beea34f008e6e96fcd493d8410d7d2c5b88
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299632"
---
# <a name="requestedit-attribute"></a><span data-ttu-id="efb4c-104">requestedit (attributo)</span><span class="sxs-lookup"><span data-stu-id="efb4c-104">requestedit attribute</span></span>

<span data-ttu-id="efb4c-105">L'attributo **\[ \] requestedit** indica che la proprietà supporta la notifica **OnRequestEdit** .</span><span class="sxs-lookup"><span data-stu-id="efb4c-105">The **\[requestedit\]** attribute indicates that the property supports the **OnRequestEdit** notification.</span></span>

``` syntax
[requestedit [,optional-attributes]] return-type function-name(params)
```

## <a name="parameters"></a><span data-ttu-id="efb4c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="efb4c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efb4c-107">*facoltativo-attributi*</span><span class="sxs-lookup"><span data-stu-id="efb4c-107">*optional-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="efb4c-108">Zero o più attributi MIDL.</span><span class="sxs-lookup"><span data-stu-id="efb4c-108">Zero or more MIDL attributes.</span></span>

</dd> <dt>

<span data-ttu-id="efb4c-109">*tipo restituito*</span><span class="sxs-lookup"><span data-stu-id="efb4c-109">*return-type*</span></span> 
</dt> <dd>

<span data-ttu-id="efb4c-110">Specifica il tipo restituito della funzione.</span><span class="sxs-lookup"><span data-stu-id="efb4c-110">Specifies the return type of the function.</span></span>

</dd> <dt>

<span data-ttu-id="efb4c-111">*Nome funzione*</span><span class="sxs-lookup"><span data-stu-id="efb4c-111">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="efb4c-112">Specifica il nome della funzione nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="efb4c-112">Specifies the name of the function in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="efb4c-113">*params*</span><span class="sxs-lookup"><span data-stu-id="efb4c-113">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="efb4c-114">Zero o più parametri di funzione.</span><span class="sxs-lookup"><span data-stu-id="efb4c-114">Zero or more function parameters.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="efb4c-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="efb4c-115">Remarks</span></span>

<span data-ttu-id="efb4c-116">Il supporto della notifica **OnRequestEdit** significa che, prima che venga apportata una modifica, l'oggetto invierà al client una richiesta di autorizzazione per la modifica di una proprietà.</span><span class="sxs-lookup"><span data-stu-id="efb4c-116">Supporting **OnRequestEdit** notification means that, before a change is made, the object will send the client a request for permission to change a property.</span></span> <span data-ttu-id="efb4c-117">Un oggetto può supportare data binding ma non avere questo attributo.</span><span class="sxs-lookup"><span data-stu-id="efb4c-117">An object can support data binding but not have this attribute.</span></span>

### <a name="flags"></a><span data-ttu-id="efb4c-118">Flags</span><span class="sxs-lookup"><span data-stu-id="efb4c-118">Flags</span></span>

<span data-ttu-id="efb4c-119">FUNCFLAG \_ FREQUESTEDIT, VARFLAG \_ FREQUESTEDIT</span><span class="sxs-lookup"><span data-stu-id="efb4c-119">FUNCFLAG\_FREQUESTEDIT, VARFLAG\_FREQUESTEDIT</span></span>

## <a name="examples"></a><span data-ttu-id="efb4c-120">Esempi</span><span class="sxs-lookup"><span data-stu-id="efb4c-120">Examples</span></span>

``` syntax
properties:
    [propget, helpstring("A useful comment"), bindable, defaultbind,
     displaybind, requestedit] long Func1(void);
```

## <a name="see-also"></a><span data-ttu-id="efb4c-121">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="efb4c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efb4c-122">TYPEFLAGS</span><span class="sxs-lookup"><span data-stu-id="efb4c-122">TYPEFLAGS</span></span>](/windows/win32/api/oaidl/ne-oaidl-typeflags)
</dt> <dt>

[<span data-ttu-id="efb4c-123">Sintassi del file di FAD</span><span class="sxs-lookup"><span data-stu-id="efb4c-123">ODL File Syntax</span></span>](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[<span data-ttu-id="efb4c-124">Esempio di file di FAD</span><span class="sxs-lookup"><span data-stu-id="efb4c-124">ODL File Example</span></span>](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[<span data-ttu-id="efb4c-125">Generazione di una libreria dei tipi con MIDL</span><span class="sxs-lookup"><span data-stu-id="efb4c-125">Generating a Type Library With MIDL</span></span>](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 