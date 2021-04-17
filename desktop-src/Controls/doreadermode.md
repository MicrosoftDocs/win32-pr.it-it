---
title: DoReaderMode (funzione)
description: Abilita la modalità lettore in una finestra.
ms.assetid: 8f898cdd-c907-430a-8287-15d88390c756
keywords:
- Controlli Windows per la funzione DoReaderMode
topic_type:
- apiref
api_name:
- DoReaderMode
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5f5c5863e804cd4bbaab651447e4c6f22dc24a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479472"
---
# <a name="doreadermode-function"></a><span data-ttu-id="39353-104">DoReaderMode (funzione)</span><span class="sxs-lookup"><span data-stu-id="39353-104">DoReaderMode function</span></span>

<span data-ttu-id="39353-105">\[**DoReaderMode** è disponibile tramite Windows XP con Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="39353-105">\[**DoReaderMode** is available through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="39353-106">Potrebbe non essere disponibile nelle versioni successive.\]</span><span class="sxs-lookup"><span data-stu-id="39353-106">It may be unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="39353-107">Abilita la modalità lettore in una finestra.</span><span class="sxs-lookup"><span data-stu-id="39353-107">Enables reader mode in a window.</span></span>

## <a name="syntax"></a><span data-ttu-id="39353-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="39353-108">Syntax</span></span>


```C++
void WINAPI DoReaderMode(
  _In_ PREADERMODEINFO prmi
);
```



## <a name="parameters"></a><span data-ttu-id="39353-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="39353-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39353-110">*prmi* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="39353-110">*prmi* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39353-111">Tipo: **PREADERMODEINFO**</span><span class="sxs-lookup"><span data-stu-id="39353-111">Type: **PREADERMODEINFO**</span></span>

<span data-ttu-id="39353-112">Puntatore a una struttura [**READERMODEINFO**](readermodeinfo.md) contenente informazioni di inizializzazione per la modalità Reader.</span><span class="sxs-lookup"><span data-stu-id="39353-112">A pointer to a [**READERMODEINFO**](readermodeinfo.md) structure that contains initialization information for the reader mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39353-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="39353-113">Return value</span></span>

<span data-ttu-id="39353-114">Questa funzione non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="39353-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="39353-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="39353-115">Remarks</span></span>

<span data-ttu-id="39353-116">La modalità lettore viene attivata tramite i dispositivi supportati con un clic del mouse, in genere utilizzando un terzo pulsante del mouse o una rotellina di scorrimento.</span><span class="sxs-lookup"><span data-stu-id="39353-116">Reader mode is activated through supported devices by a mouse click, typically using a third mouse button or scroll wheel.</span></span> <span data-ttu-id="39353-117">Il successivo movimento del mouse in un'area specificata scorre il contenuto dell'area anziché spostare un puntatore.</span><span class="sxs-lookup"><span data-stu-id="39353-117">Subsequent mouse movement in a specified area scrolls that area's contents rather than moving a pointer.</span></span> <span data-ttu-id="39353-118">Al di fuori di tale area, il puntatore del mouse viene visualizzato e funziona normalmente.</span><span class="sxs-lookup"><span data-stu-id="39353-118">Outside of that area, the mouse pointer is displayed and operates normally.</span></span> <span data-ttu-id="39353-119">Un secondo clic del pulsante o della rotellina di scorrimento rilascia il dispositivo dalla modalità lettore.</span><span class="sxs-lookup"><span data-stu-id="39353-119">A second click of the button or scroll wheel releases the device from reader mode.</span></span>

> [!Note]  
> <span data-ttu-id="39353-120">Questa funzione non è dichiarata in alcuna intestazione pubblica.</span><span class="sxs-lookup"><span data-stu-id="39353-120">This function is not declared in any public header.</span></span> <span data-ttu-id="39353-121">Per usarlo, è necessario accedervi come ordinale 383 da Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="39353-121">To use it, you must access it as ordinal 383 from Comctl32.dll.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="39353-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="39353-122">Requirements</span></span>



| <span data-ttu-id="39353-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="39353-123">Requirement</span></span> | <span data-ttu-id="39353-124">Valore</span><span class="sxs-lookup"><span data-stu-id="39353-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39353-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="39353-125">Minimum supported client</span></span><br/> | <span data-ttu-id="39353-126">Windows Vista, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="39353-126">Windows Vista, Windows Vista \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="39353-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="39353-127">Minimum supported server</span></span><br/> | <span data-ttu-id="39353-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="39353-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="39353-129">DLL</span><span class="sxs-lookup"><span data-stu-id="39353-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39353-130"><dt>Comctl32.dll (versione 4,72 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="39353-130"><dt>Comctl32.dll (version 4.72 or later)</dt></span></span> </dl> |



 

 





