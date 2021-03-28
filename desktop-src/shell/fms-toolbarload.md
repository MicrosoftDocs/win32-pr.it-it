---
description: Contiene informazioni sui pulsanti personalizzati da aggiungere alla barra degli strumenti di gestione file. I pulsanti sono forniti da una DLL di estensione di file Manager.
title: Struttura FMS_TOOLBARLOAD (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMS_TOOLBARLOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 7185f9e5-10c6-43cc-b85b-cd077378338f
ms.openlocfilehash: 8e123c759a827adddf5fd00eaf33193ebca0dbf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979695"
---
# <a name="fms_toolbarload-structure"></a><span data-ttu-id="bb5db-104">\_Struttura TOOLBARLOAD FMS</span><span class="sxs-lookup"><span data-stu-id="bb5db-104">FMS\_TOOLBARLOAD structure</span></span>

<span data-ttu-id="bb5db-105">Contiene informazioni sui pulsanti personalizzati da aggiungere alla barra degli strumenti di gestione file.</span><span class="sxs-lookup"><span data-stu-id="bb5db-105">Contains information about custom buttons to be added to the File Manager toolbar.</span></span> <span data-ttu-id="bb5db-106">I pulsanti sono forniti da una DLL di estensione di file Manager.</span><span class="sxs-lookup"><span data-stu-id="bb5db-106">The buttons are provided by a File Manager extension DLL.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb5db-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bb5db-107">Syntax</span></span>


```C++
typedef struct _FMS_TOOLBARLOAD {
  DWORD        dwSize;
  LPEXT_BUTTON lpButtons;
  WORD         cButtons;
  WORD         cBitmaps;
  WORD         idBitmap;
  HBITMAP      hBitmap;
} FMS_TOOLBARLOAD;
```



## <a name="members"></a><span data-ttu-id="bb5db-108">Members</span><span class="sxs-lookup"><span data-stu-id="bb5db-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="bb5db-109">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="bb5db-109">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="bb5db-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="bb5db-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="bb5db-111">Dimensione, in byte, della struttura.</span><span class="sxs-lookup"><span data-stu-id="bb5db-111">The size, in bytes, of the structure.</span></span> <span data-ttu-id="bb5db-112">Gestione file imposta le dimensioni prima di chiamare l'estensione e controlla le dimensioni dopo la restituzione della procedura di estensione.</span><span class="sxs-lookup"><span data-stu-id="bb5db-112">File Manager sets the size before calling the extension and checks the size after the extension procedure returns.</span></span>

</dd> <dt>

<span data-ttu-id="bb5db-113">**lpButtons**</span><span class="sxs-lookup"><span data-stu-id="bb5db-113">**lpButtons**</span></span>
</dt> <dd>

<span data-ttu-id="bb5db-114">Tipo: **LPEXT \_ Button**</span><span class="sxs-lookup"><span data-stu-id="bb5db-114">Type: **LPEXT\_BUTTON**</span></span>

</dd> <dd>

<span data-ttu-id="bb5db-115">Indirizzo di una matrice di strutture [**di \_ pulsanti EXT**](ext-button.md) .</span><span class="sxs-lookup"><span data-stu-id="bb5db-115">The address of an array of [**EXT\_BUTTON**](ext-button.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="bb5db-116">**cButtons**</span><span class="sxs-lookup"><span data-stu-id="bb5db-116">**cButtons**</span></span>
</dt> <dd>

<span data-ttu-id="bb5db-117">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="bb5db-117">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="bb5db-118">Numero di strutture [**di \_ pulsanti EXT**](ext-button.md) nella matrice a cui punta il membro **lpButtons** .</span><span class="sxs-lookup"><span data-stu-id="bb5db-118">The number of [**EXT\_BUTTON**](ext-button.md) structures in the array pointed to by the **lpButtons** member.</span></span> <span data-ttu-id="bb5db-119">Questo numero è uguale al numero di pulsanti e separatori da aggiungere alla barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="bb5db-119">This number equals the number of buttons and separators to add to the toolbar.</span></span>

</dd> <dt>

<span data-ttu-id="bb5db-120">**cBitmaps**</span><span class="sxs-lookup"><span data-stu-id="bb5db-120">**cBitmaps**</span></span>
</dt> <dd>

<span data-ttu-id="bb5db-121">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="bb5db-121">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="bb5db-122">Numero di pulsanti rappresentati dalla bitmap specificata.</span><span class="sxs-lookup"><span data-stu-id="bb5db-122">The number of buttons represented by the given bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="bb5db-123">**idBitmap**</span><span class="sxs-lookup"><span data-stu-id="bb5db-123">**idBitmap**</span></span>
</dt> <dd>

<span data-ttu-id="bb5db-124">Tipo: **Word**</span><span class="sxs-lookup"><span data-stu-id="bb5db-124">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="bb5db-125">Identificatore di una risorsa bitmap nel file eseguibile per la DLL di estensione.</span><span class="sxs-lookup"><span data-stu-id="bb5db-125">The identifier of a bitmap resource in the executable file for the extension DLL.</span></span> <span data-ttu-id="bb5db-126">La risorsa bitmap contiene immagini per il numero di pulsanti specificato da **cBitmaps**.</span><span class="sxs-lookup"><span data-stu-id="bb5db-126">The bitmap resource contains images for the number of buttons specified by **cBitmaps**.</span></span> <span data-ttu-id="bb5db-127">Gestione file carica la risorsa bitmap e la usa per visualizzare i pulsanti.</span><span class="sxs-lookup"><span data-stu-id="bb5db-127">File Manager loads the bitmap resource and then uses it to display the buttons.</span></span>

</dd> <dt>

<span data-ttu-id="bb5db-128">**hBitmap**</span><span class="sxs-lookup"><span data-stu-id="bb5db-128">**hBitmap**</span></span>
</dt> <dd>

<span data-ttu-id="bb5db-129">Tipo: **HBITMAP**</span><span class="sxs-lookup"><span data-stu-id="bb5db-129">Type: **HBITMAP**</span></span>

</dd> <dd>

<span data-ttu-id="bb5db-130">Handle per una bitmap che verrà utilizzata da Gestione file per ottenere e visualizzare le immagini del pulsante se **idBitmap** è 0.</span><span class="sxs-lookup"><span data-stu-id="bb5db-130">A handle to a bitmap that File Manager will use to obtain and display button images if **idBitmap** is 0.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bb5db-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb5db-131">Requirements</span></span>



| <span data-ttu-id="bb5db-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb5db-132">Requirement</span></span> | <span data-ttu-id="bb5db-133">Valore</span><span class="sxs-lookup"><span data-stu-id="bb5db-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bb5db-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb5db-134">Minimum supported client</span></span><br/> | <span data-ttu-id="bb5db-135">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bb5db-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="bb5db-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb5db-136">Minimum supported server</span></span><br/> | <span data-ttu-id="bb5db-137">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bb5db-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bb5db-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bb5db-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb5db-139"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb5db-139"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb5db-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bb5db-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb5db-141">**\_TOOLBARLOAD FMEVENT**</span><span class="sxs-lookup"><span data-stu-id="bb5db-141">**FMEVENT\_TOOLBARLOAD**</span></span>](fmevent-toolbarload.md)
</dt> </dl>

 

 




