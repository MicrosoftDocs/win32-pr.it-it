---
description: Si verifica quando i dati sono disponibili dalla risposta.
ms.assetid: 62d02e3b-466a-4d3d-994b-0a1ae12049e1
title: 'Evento IWinHttpRequestEvents:: OnResponseDataAvailable'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41cb2fbc680b1f6739a66bb68565188c8a5d78b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314110"
---
# <a name="iwinhttprequesteventsonresponsedataavailable-event"></a><span data-ttu-id="8d3c5-103">Evento IWinHttpRequestEvents:: OnResponseDataAvailable</span><span class="sxs-lookup"><span data-stu-id="8d3c5-103">IWinHttpRequestEvents::OnResponseDataAvailable event</span></span>

<span data-ttu-id="8d3c5-104">L'evento **OnResponseDataAvailable** si verifica quando i dati sono disponibili dalla risposta.</span><span class="sxs-lookup"><span data-stu-id="8d3c5-104">The **OnResponseDataAvailable** event occurs when data is available from the response.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d3c5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8d3c5-105">Syntax</span></span>


```C++
void OnResponseDataAvailable(
  [in] SAFEARRAY(unsigned char) *Data
);
```



## <a name="parameters"></a><span data-ttu-id="8d3c5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8d3c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d3c5-107">*Dati* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="8d3c5-107">*Data* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d3c5-108">Matrice di byte in base zero che riceve i dati di risposta ricevuti dai servizi HTTP di Microsoft Windows (WinHTTP) fino al momento in cui si verifica questo evento.</span><span class="sxs-lookup"><span data-stu-id="8d3c5-108">A zero-based array of bytes that receives the response data received by Microsoft Windows HTTP Services (WinHTTP) up to the point that this event occurs.</span></span> <span data-ttu-id="8d3c5-109">Si tratta di una **variante** di tipo VT \_ array \| VT \_ Ui1.</span><span class="sxs-lookup"><span data-stu-id="8d3c5-109">This is a **VARIANT** of type VT\_ARRAY \| VT\_UI1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d3c5-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8d3c5-110">Return value</span></span>

<span data-ttu-id="8d3c5-111">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="8d3c5-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d3c5-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="8d3c5-112">Remarks</span></span>

<span data-ttu-id="8d3c5-113">Poiché i dati sono in byte, devono essere convertiti in caratteri wide se inseriti in una stringa di caratteri wide (Unicode).</span><span class="sxs-lookup"><span data-stu-id="8d3c5-113">Because data is in bytes, it must be converted to wide characters when placed in a wide character (Unicode) string.</span></span>

> [!Note]  
> <span data-ttu-id="8d3c5-114">Per Windows XP e Windows 2000, vedere la sezione [requisiti di run-time](winhttp-start-page.md) della pagina iniziale di WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="8d3c5-114">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP Start Page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8d3c5-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8d3c5-115">Requirements</span></span>



| <span data-ttu-id="8d3c5-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8d3c5-116">Requirement</span></span> | <span data-ttu-id="8d3c5-117">Valore</span><span class="sxs-lookup"><span data-stu-id="8d3c5-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d3c5-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8d3c5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="8d3c5-119">Windows XP, Windows 2000 Professional con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="8d3c5-119">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="8d3c5-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8d3c5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="8d3c5-121">Windows Server 2003, Windows 2000 Server con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="8d3c5-121">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="8d3c5-122">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="8d3c5-122">Redistributable</span></span><br/>          | <span data-ttu-id="8d3c5-123">WinHTTP 5,0 e Internet Explorer 5,01 o versioni successive in Windows XP e Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="8d3c5-123">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="8d3c5-124">IDL</span><span class="sxs-lookup"><span data-stu-id="8d3c5-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8d3c5-125"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8d3c5-125"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8d3c5-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8d3c5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d3c5-127">**IWinHttpRequestEvents**</span><span class="sxs-lookup"><span data-stu-id="8d3c5-127">**IWinHttpRequestEvents**</span></span>](iwinhttprequestevents-interface.md)
</dt> <dt>

[<span data-ttu-id="8d3c5-128">**WinHttpRequest**</span><span class="sxs-lookup"><span data-stu-id="8d3c5-128">**WinHttpRequest**</span></span>](winhttprequest.md)
</dt> <dt>

[<span data-ttu-id="8d3c5-129">Versioni WinHTTP</span><span class="sxs-lookup"><span data-stu-id="8d3c5-129">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




