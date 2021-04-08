---
description: La funzione GetCaptureMacType restituisce il tipo MAC di una determinata acquisizione.
ms.assetid: de0dfb36-df3a-4f6e-b266-09c81dfdc88b
title: Funzione GetCaptureMacType (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureMacType
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 73569109db5b958e854135461a0e480178d0105a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750095"
---
# <a name="getcapturemactype-function"></a><span data-ttu-id="ea96c-103">GetCaptureMacType (funzione)</span><span class="sxs-lookup"><span data-stu-id="ea96c-103">GetCaptureMacType function</span></span>

<span data-ttu-id="ea96c-104">La funzione **GetCaptureMacType** restituisce il tipo Mac di una determinata acquisizione.</span><span class="sxs-lookup"><span data-stu-id="ea96c-104">The **GetCaptureMacType** function returns the MAC type of a given capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea96c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ea96c-105">Syntax</span></span>


```C++
DWORD WINAPI GetCaptureMacType(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a><span data-ttu-id="ea96c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ea96c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea96c-107">*hCapture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ea96c-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea96c-108">Handle per l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="ea96c-108">Handle to the capture.</span></span> <span data-ttu-id="ea96c-109">Per informazioni sull'acquisizione dell'handle di acquisizione, vedere la sezione Osservazioni in questo argomento **GetCaptureMacType** .</span><span class="sxs-lookup"><span data-stu-id="ea96c-109">For information about obtaining the capture handle, see the Remarks section in this **GetCaptureMacType** topic.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea96c-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ea96c-110">Return value</span></span>

<span data-ttu-id="ea96c-111">Se la funzione ha esito positivo, il valore restituito è uno dei tipi MAC seguenti.</span><span class="sxs-lookup"><span data-stu-id="ea96c-111">If the function is successful, the return value is one of the following MAC types.</span></span>

-   <span data-ttu-id="ea96c-112">\_tipo Mac \_ sconosciuto</span><span class="sxs-lookup"><span data-stu-id="ea96c-112">MAC\_TYPE\_UNKNOWN</span></span>
-   <span data-ttu-id="ea96c-113">\_Ethernet di tipo Mac \_</span><span class="sxs-lookup"><span data-stu-id="ea96c-113">MAC\_TYPE\_ETHERNET</span></span>
-   <span data-ttu-id="ea96c-114">\_Tokenring di tipo Mac \_</span><span class="sxs-lookup"><span data-stu-id="ea96c-114">MAC\_TYPE\_TOKENRING</span></span>
-   <span data-ttu-id="ea96c-115">\_FDDI di tipo Mac \_</span><span class="sxs-lookup"><span data-stu-id="ea96c-115">MAC\_TYPE\_FDDI</span></span>

<span data-ttu-id="ea96c-116">Se la funzione ha esito negativo, il valore restituito è un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="ea96c-116">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="ea96c-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ea96c-117">Return code</span></span>                                                                                              | <span data-ttu-id="ea96c-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ea96c-118">Description</span></span>                                                 |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="ea96c-119"><dt>**\_tipo Mac \_ NMERR \_ sconosciuto**</dt></span><span class="sxs-lookup"><span data-stu-id="ea96c-119"><dt>**NMERR\_MAC\_TYPE\_UNKNOWN**</dt></span></span> </dl> | <span data-ttu-id="ea96c-120">Network Monitor non è riuscito a trovare un tipo MAC noto.</span><span class="sxs-lookup"><span data-stu-id="ea96c-120">Network Monitor could not find a known MAC type.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ea96c-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="ea96c-121">Remarks</span></span>

<span data-ttu-id="ea96c-122">L'handle dell'acquisizione può essere ottenuto in diversi modi, a seconda dell'utente che effettua la chiamata.</span><span class="sxs-lookup"><span data-stu-id="ea96c-122">The handle of the capture can be obtained in several ways, depending on who makes the call.</span></span> <span data-ttu-id="ea96c-123">Per gli esperti, l'handle viene specificato nel membro **hCapture** della struttura [EXPERTSTARTUPINFO](expertstartupinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="ea96c-123">For experts, the handle is specified in the **hCapture** member of the [EXPERTSTARTUPINFO](expertstartupinfo.md) structure.</span></span> <span data-ttu-id="ea96c-124">Per i parser, è possibile ottenere l'handle di acquisizione chiamando la funzione [GetFrameCaptureHandle](getframecapturehandle.md) .</span><span class="sxs-lookup"><span data-stu-id="ea96c-124">For parsers, the capture handle can be obtained by calling the [GetFrameCaptureHandle](getframecapturehandle.md) function.</span></span>

<span data-ttu-id="ea96c-125">Gli [*esperti*](e.md) e i [*parser*](p.md) possono chiamare la funzione **GetCaptureMacType** .</span><span class="sxs-lookup"><span data-stu-id="ea96c-125">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetCaptureMacType** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea96c-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ea96c-126">Requirements</span></span>



| <span data-ttu-id="ea96c-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea96c-127">Requirement</span></span> | <span data-ttu-id="ea96c-128">Valore</span><span class="sxs-lookup"><span data-stu-id="ea96c-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ea96c-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ea96c-129">Minimum supported client</span></span><br/> | <span data-ttu-id="ea96c-130">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ea96c-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="ea96c-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ea96c-131">Minimum supported server</span></span><br/> | <span data-ttu-id="ea96c-132">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ea96c-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ea96c-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ea96c-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea96c-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea96c-134"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="ea96c-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="ea96c-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="ea96c-136"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea96c-136"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="ea96c-137">DLL</span><span class="sxs-lookup"><span data-stu-id="ea96c-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea96c-138"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea96c-138"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




