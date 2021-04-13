---
title: funzione gluGetString (Glu. h)
description: La funzione gluGetString ottiene una stringa che descrive il numero di versione di GLU o le chiamate all'estensione GLU supportate.
ms.assetid: e6d9ce03-3218-4145-8bb5-3989afe62436
keywords:
- funzione gluGetString OpenGL
topic_type:
- apiref
api_name:
- gluGetString
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 574ed93c9c6f8d1f964e38ee14541d57bd5c34da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400525"
---
# <a name="glugetstring-function"></a><span data-ttu-id="9ddfb-104">gluGetString (funzione)</span><span class="sxs-lookup"><span data-stu-id="9ddfb-104">gluGetString function</span></span>

<span data-ttu-id="9ddfb-105">La funzione **GluGetString** ottiene una stringa che descrive il numero di versione di Glu o le chiamate all'estensione Glu supportate.</span><span class="sxs-lookup"><span data-stu-id="9ddfb-105">The **gluGetString** function gets a string that describes the GLU version number or supported GLU extension calls.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ddfb-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9ddfb-106">Syntax</span></span>


```C++
const GLubyte* WINAPI gluGetString(
   GLenum name
);
```



## <a name="parameters"></a><span data-ttu-id="9ddfb-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="9ddfb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ddfb-108">*nome*</span><span class="sxs-lookup"><span data-stu-id="9ddfb-108">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="9ddfb-109">Il numero di versione di GLU (GLU \_ Version) o delle chiamate di estensione specifiche del fornitore disponibili (Glu \_ Extensions).</span><span class="sxs-lookup"><span data-stu-id="9ddfb-109">Either the version number of GLU (GLU\_VERSION) or available vendor-specific extension calls (GLU\_EXTENSIONS).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9ddfb-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="9ddfb-110">Remarks</span></span>

<span data-ttu-id="9ddfb-111">La funzione **GluGetString** restituisce un puntatore a una stringa statica con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="9ddfb-111">The **gluGetString** function returns a pointer to a static, null-terminated string.</span></span> <span data-ttu-id="9ddfb-112">Quando *Name* è la \_ versione Glu, la stringa restituita è un valore che rappresenta il numero di versione di Glu.</span><span class="sxs-lookup"><span data-stu-id="9ddfb-112">When *name* is GLU\_VERSION, the returned string is a value that represents the version number of GLU.</span></span> <span data-ttu-id="9ddfb-113">Il formato del numero di versione è il seguente:</span><span class="sxs-lookup"><span data-stu-id="9ddfb-113">The format of the version number is as follows:</span></span>

``` syntax
<version number><space><vendor-specific information> 
(for example, "1.2.11 Microsoft Windows")
```

<span data-ttu-id="9ddfb-114">Il numero di versione ha il formato "numero principale \_ . \_ numero secondario" o "numero principale. numero \_ secondario \_ . \_ numero versione".</span><span class="sxs-lookup"><span data-stu-id="9ddfb-114">The version number has the form "major\_number.minor\_number" or "major\_number.minor\_number.release\_number".</span></span> <span data-ttu-id="9ddfb-115">Le informazioni specifiche del fornitore sono facoltative e il formato e il contenuto dipendono dall'implementazione di.</span><span class="sxs-lookup"><span data-stu-id="9ddfb-115">The vendor-specific information is optional, and the format and contents depend on the implementation.</span></span>

<span data-ttu-id="9ddfb-116">Quando *Name* è \_ il nome dell'estensione Glu, la stringa restituita contiene un elenco di nomi di estensioni Glu supportate separate da spazi.</span><span class="sxs-lookup"><span data-stu-id="9ddfb-116">When *name* is GLU\_EXTENSIONS, the returned string contains a list of names of supported GLU extensions that are separated by spaces.</span></span> <span data-ttu-id="9ddfb-117">Il formato dell'elenco di nomi restituito è il seguente:</span><span class="sxs-lookup"><span data-stu-id="9ddfb-117">The format of the returned list of names is as follows:</span></span>

``` syntax
<extension_name><space><extension_name><space> . . .
(for example, "GLU_NURBS GL_TESSELATION")
```

<span data-ttu-id="9ddfb-118">I nomi di estensione non possono contenere spazi.</span><span class="sxs-lookup"><span data-stu-id="9ddfb-118">The extension names cannot contain any spaces.</span></span>

<span data-ttu-id="9ddfb-119">La funzione **GluGetString** è valida per GLU versione 1,1 o successiva.</span><span class="sxs-lookup"><span data-stu-id="9ddfb-119">The **gluGetString** function is valid for GLU version 1.1 or later.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ddfb-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9ddfb-120">Requirements</span></span>



| <span data-ttu-id="9ddfb-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ddfb-121">Requirement</span></span> | <span data-ttu-id="9ddfb-122">Valore</span><span class="sxs-lookup"><span data-stu-id="9ddfb-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9ddfb-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ddfb-123">Minimum supported client</span></span><br/> | <span data-ttu-id="9ddfb-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9ddfb-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9ddfb-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9ddfb-125">Minimum supported server</span></span><br/> | <span data-ttu-id="9ddfb-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9ddfb-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9ddfb-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9ddfb-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="9ddfb-128"><dt>Glu. h</dt></span><span class="sxs-lookup"><span data-stu-id="9ddfb-128"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="9ddfb-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="9ddfb-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="9ddfb-130"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9ddfb-130"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9ddfb-131">DLL</span><span class="sxs-lookup"><span data-stu-id="9ddfb-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ddfb-132"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ddfb-132"><dt>Glu32.dll</dt></span></span> </dl> |



 

 





