---
description: Contiene informazioni sui pulsanti personalizzati da aggiungere alla barra degli strumenti di File Manager. I pulsanti sono forniti da una DLL di estensione di File Manager.
title: FMS_TOOLBARLOAD (Wfext.h)
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
ms.openlocfilehash: 3a993312b9e365561018459c43dab87afbd3c2b2
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842162"
---
# <a name="fms_toolbarload-structure"></a><span data-ttu-id="0ebdc-104">Struttura TOOLBARLOAD DI FMS \_</span><span class="sxs-lookup"><span data-stu-id="0ebdc-104">FMS\_TOOLBARLOAD structure</span></span>

<span data-ttu-id="0ebdc-105">Contiene informazioni sui pulsanti personalizzati da aggiungere alla barra degli strumenti di File Manager.</span><span class="sxs-lookup"><span data-stu-id="0ebdc-105">Contains information about custom buttons to be added to the File Manager toolbar.</span></span> <span data-ttu-id="0ebdc-106">I pulsanti sono forniti da una DLL di estensione di File Manager.</span><span class="sxs-lookup"><span data-stu-id="0ebdc-106">The buttons are provided by a File Manager extension DLL.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ebdc-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0ebdc-107">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="0ebdc-108">Members</span><span class="sxs-lookup"><span data-stu-id="0ebdc-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="0ebdc-109">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="0ebdc-109">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="0ebdc-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="0ebdc-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="0ebdc-111">Dimensione, in byte, della struttura .</span><span class="sxs-lookup"><span data-stu-id="0ebdc-111">The size, in bytes, of the structure.</span></span> <span data-ttu-id="0ebdc-112">File Manager imposta le dimensioni prima di chiamare l'estensione e controlla le dimensioni al termine della procedura di estensione.</span><span class="sxs-lookup"><span data-stu-id="0ebdc-112">File Manager sets the size before calling the extension and checks the size after the extension procedure returns.</span></span>

</dd> <dt>

<span data-ttu-id="0ebdc-113">**lpButtons**</span><span class="sxs-lookup"><span data-stu-id="0ebdc-113">**lpButtons**</span></span>
</dt> <dd>

<span data-ttu-id="0ebdc-114">Tipo: **PULSANTE \_ LPEXT**</span><span class="sxs-lookup"><span data-stu-id="0ebdc-114">Type: **LPEXT\_BUTTON**</span></span>

</dd> <dd>

<span data-ttu-id="0ebdc-115">Indirizzo di una matrice di [**strutture BUTTON \_ EXT.**](ext-button.md)</span><span class="sxs-lookup"><span data-stu-id="0ebdc-115">The address of an array of [**EXT\_BUTTON**](ext-button.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="0ebdc-116">**cButtons**</span><span class="sxs-lookup"><span data-stu-id="0ebdc-116">**cButtons**</span></span>
</dt> <dd>

<span data-ttu-id="0ebdc-117">Tipo: **WORD**</span><span class="sxs-lookup"><span data-stu-id="0ebdc-117">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="0ebdc-118">Numero di [**strutture EXT \_ BUTTON**](ext-button.md) nella matrice a cui punta il **membro lpButtons.**</span><span class="sxs-lookup"><span data-stu-id="0ebdc-118">The number of [**EXT\_BUTTON**](ext-button.md) structures in the array pointed to by the **lpButtons** member.</span></span> <span data-ttu-id="0ebdc-119">Questo numero è uguale al numero di pulsanti e separatori da aggiungere alla barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="0ebdc-119">This number equals the number of buttons and separators to add to the toolbar.</span></span>

</dd> <dt>

<span data-ttu-id="0ebdc-120">**cBitmaps**</span><span class="sxs-lookup"><span data-stu-id="0ebdc-120">**cBitmaps**</span></span>
</dt> <dd>

<span data-ttu-id="0ebdc-121">Tipo: **WORD**</span><span class="sxs-lookup"><span data-stu-id="0ebdc-121">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="0ebdc-122">Numero di pulsanti rappresentati dalla bitmap specificata.</span><span class="sxs-lookup"><span data-stu-id="0ebdc-122">The number of buttons represented by the given bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="0ebdc-123">**idBitmap**</span><span class="sxs-lookup"><span data-stu-id="0ebdc-123">**idBitmap**</span></span>
</dt> <dd>

<span data-ttu-id="0ebdc-124">Tipo: **WORD**</span><span class="sxs-lookup"><span data-stu-id="0ebdc-124">Type: **WORD**</span></span>

</dd> <dd>

<span data-ttu-id="0ebdc-125">Identificatore di una risorsa bitmap nel file eseguibile per la DLL di estensione.</span><span class="sxs-lookup"><span data-stu-id="0ebdc-125">The identifier of a bitmap resource in the executable file for the extension DLL.</span></span> <span data-ttu-id="0ebdc-126">La risorsa bitmap contiene immagini per il numero di pulsanti specificato da **cBitmaps**.</span><span class="sxs-lookup"><span data-stu-id="0ebdc-126">The bitmap resource contains images for the number of buttons specified by **cBitmaps**.</span></span> <span data-ttu-id="0ebdc-127">File Manager carica la risorsa bitmap e la usa per visualizzare i pulsanti.</span><span class="sxs-lookup"><span data-stu-id="0ebdc-127">File Manager loads the bitmap resource and then uses it to display the buttons.</span></span>

</dd> <dt>

<span data-ttu-id="0ebdc-128">**Hbitmap**</span><span class="sxs-lookup"><span data-stu-id="0ebdc-128">**hBitmap**</span></span>
</dt> <dd>

<span data-ttu-id="0ebdc-129">Tipo: **HBITMAP**</span><span class="sxs-lookup"><span data-stu-id="0ebdc-129">Type: **HBITMAP**</span></span>

</dd> <dd>

<span data-ttu-id="0ebdc-130">Handle di una bitmap che File Manager userà per ottenere e visualizzare le immagini dei pulsanti se **idBitmap** è 0.</span><span class="sxs-lookup"><span data-stu-id="0ebdc-130">A handle to a bitmap that File Manager will use to obtain and display button images if **idBitmap** is 0.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0ebdc-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0ebdc-131">Requirements</span></span>



| <span data-ttu-id="0ebdc-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ebdc-132">Requirement</span></span> | <span data-ttu-id="0ebdc-133">Valore</span><span class="sxs-lookup"><span data-stu-id="0ebdc-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0ebdc-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ebdc-134">Minimum supported client</span></span><br/> | <span data-ttu-id="0ebdc-135">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0ebdc-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="0ebdc-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0ebdc-136">Minimum supported server</span></span><br/> | <span data-ttu-id="0ebdc-137">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0ebdc-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0ebdc-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0ebdc-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="0ebdc-139"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="0ebdc-139"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ebdc-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0ebdc-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ebdc-141">**BARRA DEGLI STRUMENTI \_ FMEVENTLOAD**</span><span class="sxs-lookup"><span data-stu-id="0ebdc-141">**FMEVENT\_TOOLBARLOAD**</span></span>](fmevent-toolbarload.md)
</dt> </dl>

 

 




