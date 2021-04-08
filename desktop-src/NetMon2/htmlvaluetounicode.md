---
description: La funzione HTMLValueToUnicode converte una stringa in formato Unicode del CP HTML \_ in una stringa Unicode.
ms.assetid: d175476e-9c84-48b8-9c89-00255b7cb638
title: Funzione HTMLValueToUnicode (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HTMLValueToUnicode
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 8ef5f4a2b49139ce1ab5366dac3f6c141425653e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750066"
---
# <a name="htmlvaluetounicode-function"></a><span data-ttu-id="5fd05-103">HTMLValueToUnicode (funzione)</span><span class="sxs-lookup"><span data-stu-id="5fd05-103">HTMLValueToUnicode function</span></span>

<span data-ttu-id="5fd05-104">La funzione **HTMLValueToUnicode** converte una stringa in formato Unicode del CP HTML \_ in una stringa Unicode.</span><span class="sxs-lookup"><span data-stu-id="5fd05-104">The **HTMLValueToUnicode** function converts an HTML CP\_UTF8 string to a Unicode string.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fd05-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5fd05-105">Syntax</span></span>


```C++
WCHAR* HTMLValueToUnicode(
  _Inout_ const char *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="5fd05-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5fd05-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fd05-107">*pValue* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="5fd05-107">*pValue* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5fd05-108">In input, puntatore alla stringa HTML fornita da MCSVC.</span><span class="sxs-lookup"><span data-stu-id="5fd05-108">On input, pointer to the HTML string supplied by the MCSVC.</span></span>

<span data-ttu-id="5fd05-109">Nell'output, puntatore alla stringa Unicode convertita.</span><span class="sxs-lookup"><span data-stu-id="5fd05-109">On output, pointer to the converted Unicode string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fd05-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5fd05-110">Return value</span></span>

<span data-ttu-id="5fd05-111">La funzione restituisce l'equivalente Unicode della stringa.</span><span class="sxs-lookup"><span data-stu-id="5fd05-111">The function returns the Unicode equivalent of the string.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fd05-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5fd05-112">Requirements</span></span>



| <span data-ttu-id="5fd05-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fd05-113">Requirement</span></span> | <span data-ttu-id="5fd05-114">Valore</span><span class="sxs-lookup"><span data-stu-id="5fd05-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5fd05-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5fd05-115">Minimum supported client</span></span><br/> | <span data-ttu-id="5fd05-116">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5fd05-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="5fd05-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5fd05-117">Minimum supported server</span></span><br/> | <span data-ttu-id="5fd05-118">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5fd05-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5fd05-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5fd05-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="5fd05-120"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5fd05-120"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="5fd05-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="5fd05-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="5fd05-122"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5fd05-122"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="5fd05-123">DLL</span><span class="sxs-lookup"><span data-stu-id="5fd05-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5fd05-124"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5fd05-124"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




