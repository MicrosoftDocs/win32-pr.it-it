---
title: Classe Matrix4x3F ( \_ Helper D2d1. h)
description: La classe Matrix4x3F rappresenta una matrice 4 per 3 e fornisce metodi pratici per la creazione di matrici.
ms.assetid: 633B1828-0CB5-4CD3-9826-C65083C6C0A9
keywords:
- Classe Matrix4x3F Direct2D
- Classe Matrix4x3F Direct2D, descritta
topic_type:
- apiref
api_name:
- Matrix4x3F
api_location:
- D2d1.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81467b51eb22586d537c7ea8032e13a30da19c55
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874642"
---
# <a name="matrix4x3f-class"></a><span data-ttu-id="c7c65-105">Classe Matrix4x3F</span><span class="sxs-lookup"><span data-stu-id="c7c65-105">Matrix4x3F class</span></span>

<span data-ttu-id="c7c65-106">La classe **Matrix4x3F** rappresenta una matrice 4 per 3 e fornisce metodi pratici per la creazione di matrici.</span><span class="sxs-lookup"><span data-stu-id="c7c65-106">The **Matrix4x3F** class represents a 4-by-3 matrix and provides convenience methods for creating matrices.</span></span>

## <a name="members"></a><span data-ttu-id="c7c65-107">Membri</span><span class="sxs-lookup"><span data-stu-id="c7c65-107">Members</span></span>

<span data-ttu-id="c7c65-108">La classe **Matrix4x3F** eredita da [**d2d1 \_ Matrix \_ 4x3 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x3_f).</span><span class="sxs-lookup"><span data-stu-id="c7c65-108">The **Matrix4x3F** class inherits from [**D2D1\_MATRIX\_4X3\_F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x3_f).</span></span> <span data-ttu-id="c7c65-109">**Matrix4x3F** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c7c65-109">**Matrix4x3F** also has these types of members:</span></span>

-   [<span data-ttu-id="c7c65-110">Costruttori</span><span class="sxs-lookup"><span data-stu-id="c7c65-110">Constructors</span></span>](#constructors)

### <a name="constructors"></a><span data-ttu-id="c7c65-111">Costruttori</span><span class="sxs-lookup"><span data-stu-id="c7c65-111">Constructors</span></span>

<span data-ttu-id="c7c65-112">La classe **Matrix4x3F** dispone di questi costruttori.</span><span class="sxs-lookup"><span data-stu-id="c7c65-112">The **Matrix4x3F** class has these constructors.</span></span>



| <span data-ttu-id="c7c65-113">Costruttore</span><span class="sxs-lookup"><span data-stu-id="c7c65-113">Constructor</span></span>                                                                                                                                                                                           | <span data-ttu-id="c7c65-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c7c65-114">Description</span></span>                                                                                                                        |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c7c65-115">**Matrix4x3F()**</span><span class="sxs-lookup"><span data-stu-id="c7c65-115">**Matrix4x3F()**</span></span>](matrix4x3f-matrix4x3f--.md)                                                                                                                                                       | <span data-ttu-id="c7c65-116">Crea una nuova istanza di una classe **Matrix4x3F** non inizializzata.</span><span class="sxs-lookup"><span data-stu-id="c7c65-116">Instantiates a new instance of an uninitialized **Matrix4x3F** class.</span></span><br/>                                                   |
| [<span data-ttu-id="c7c65-117">**Matrix4x3F (FLOAT, FLOAT, float, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, float, float) (FLOAT, FLOAT, float, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, FLOAT, float, float, float)**</span><span class="sxs-lookup"><span data-stu-id="c7c65-117">**Matrix4x3F(FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT)(FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT,FLOAT)**</span></span>](matrix4x3f-matrix4x3f-floats-.md) | <span data-ttu-id="c7c65-118">Crea un'istanza di una nuova istanza di una classe **Matrix4x3F** inizializzata con tutti i valori della matrice a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="c7c65-118">Instantiates a new instance of a **Matrix4x3F** class that is initialized with all of the floating point matrix values.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c7c65-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c7c65-119">Requirements</span></span>



| <span data-ttu-id="c7c65-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7c65-120">Requirement</span></span> | <span data-ttu-id="c7c65-121">Valore</span><span class="sxs-lookup"><span data-stu-id="c7c65-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7c65-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c7c65-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c7c65-123">Windows 7, Windows Vista con SP2 e aggiornamento della piattaforma per app desktop di Windows Vista \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c7c65-123">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="c7c65-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c7c65-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c7c65-125">Windows Server 2008 R2, Windows Server 2008 con SP2 e aggiornamento della piattaforma per app desktop di Windows Server 2008 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c7c65-125">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="c7c65-126">Telefono minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c7c65-126">Minimum supported phone</span></span><br/>  | <span data-ttu-id="c7c65-127">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e app per Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="c7c65-127">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="c7c65-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="c7c65-128">Namespace</span></span><br/>                | <span data-ttu-id="c7c65-129">D2D1</span><span class="sxs-lookup"><span data-stu-id="c7c65-129">D2D1</span></span><br/>                                                                                                                          |
| <span data-ttu-id="c7c65-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c7c65-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7c65-131"><dt>\_Helper D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7c65-131"><dt>D2d1\_helper.h</dt></span></span> </dl>                                                |
| <span data-ttu-id="c7c65-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="c7c65-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="c7c65-133"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c7c65-133"><dt>D2d1.lib</dt></span></span> </dl>                                                      |
| <span data-ttu-id="c7c65-134">DLL</span><span class="sxs-lookup"><span data-stu-id="c7c65-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7c65-135"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7c65-135"><dt>D2d1.dll</dt></span></span> </dl>                                                      |



## <a name="see-also"></a><span data-ttu-id="c7c65-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c7c65-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7c65-137">**\_Matrice d2d1 \_ 4x3 \_ F**</span><span class="sxs-lookup"><span data-stu-id="c7c65-137">**D2D1\_MATRIX\_4X3\_F**</span></span>](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_4x3_f)
</dt> </dl>

 

 





