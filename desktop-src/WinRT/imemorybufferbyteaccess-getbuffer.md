---
description: Ottiene un IMemoryBuffer come matrice di byte.
ms.assetid: E9C2AF2D-ADBE-4D76-A549-2DBCB9818B09
title: 'Metodo IMemoryBufferByteAccess:: GetBuffer'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMemoryBufferByteAccess.GetBuffer
api_type:
- COM
api_location: ''
ms.openlocfilehash: f31d1506822f21977e2d60492248c2d70a51829c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307076"
---
# <a name="imemorybufferbyteaccessgetbuffer-method"></a><span data-ttu-id="7b823-103">Metodo IMemoryBufferByteAccess:: GetBuffer</span><span class="sxs-lookup"><span data-stu-id="7b823-103">IMemoryBufferByteAccess::GetBuffer method</span></span>

<span data-ttu-id="7b823-104">Ottiene un [**IMemoryBuffer**](/uwp/api/Windows.Foundation.IMemoryBuffer?view=winrt-19041) come matrice di byte.</span><span class="sxs-lookup"><span data-stu-id="7b823-104">Gets an [**IMemoryBuffer**](/uwp/api/Windows.Foundation.IMemoryBuffer?view=winrt-19041) as an array of bytes.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b823-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7b823-105">Syntax</span></span>


```C++
HRESULT GetBuffer(
  [out] BYTE   **value,
  [out] UINT32 *capacity
);
```



## <a name="parameters"></a><span data-ttu-id="7b823-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7b823-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b823-107">*valore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="7b823-107">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7b823-108">Puntatore a una matrice di byte contenente i dati del buffer.</span><span class="sxs-lookup"><span data-stu-id="7b823-108">A pointer to a byte array containing the buffer data.</span></span>

</dd> <dt>

<span data-ttu-id="7b823-109">*capacità* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="7b823-109">*capacity* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7b823-110">Numero di byte nella matrice restituita</span><span class="sxs-lookup"><span data-stu-id="7b823-110">The number of bytes in the returned array</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b823-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7b823-111">Return value</span></span>

<span data-ttu-id="7b823-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7b823-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7b823-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7b823-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b823-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="7b823-114">Remarks</span></span>

<span data-ttu-id="7b823-115">Quando viene chiamato [**MemoryBuffer:: Close**](/uwp/api/Windows.Foundation.MemoryBuffer?view=winrt-19041) , il codice che utilizza questo buffer deve impostare il puntatore del *valore* su null.</span><span class="sxs-lookup"><span data-stu-id="7b823-115">When [**MemoryBuffer::Close**](/uwp/api/Windows.Foundation.MemoryBuffer?view=winrt-19041) is called, the code using this buffer should set the *value* pointer to null.</span></span>

## <a name="see-also"></a><span data-ttu-id="7b823-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7b823-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="7b823-117">[**IMemoryBufferByteAccess**](/previous-versions//mt297505(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7b823-117">[**IMemoryBufferByteAccess**](/previous-versions//mt297505(v=vs.85))</span></span>
</dt> </dl>

 

 
