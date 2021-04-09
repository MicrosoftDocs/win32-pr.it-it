---
description: La funzione CreateNPPInterface usa il BLOB restituito dal Finder per creare un oggetto NPP che può essere usato dall'applicazione.
ms.assetid: 41f48c72-3284-4ebc-baff-63553c8971e6
title: Funzione CreateNPPInterface (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateNPPInterface
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: d0efa1c33dd5e0778f13ddd59290de324c92e813
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967779"
---
# <a name="createnppinterface-function"></a><span data-ttu-id="6ad57-103">CreateNPPInterface (funzione)</span><span class="sxs-lookup"><span data-stu-id="6ad57-103">CreateNPPInterface function</span></span>

<span data-ttu-id="6ad57-104">La funzione **CreateNPPInterface** usa il BLOB restituito dal Finder per creare un oggetto NPP che può essere usato dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="6ad57-104">The **CreateNPPInterface** function uses the BLOB returned from the finder to create an NPP that the application can use.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ad57-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6ad57-105">Syntax</span></span>


```C++
DWORD CreateNPPInterface(
  _In_  HBLOB  hBlob,
  _In_  REFIID iid,
  _Out_ void   **ppvObject
);
```



## <a name="parameters"></a><span data-ttu-id="6ad57-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6ad57-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ad57-107">*hBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6ad57-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ad57-108">Handle per il BLOB restituito dal Finder.</span><span class="sxs-lookup"><span data-stu-id="6ad57-108">Handle to the BLOB returned from the finder.</span></span>

</dd> <dt>

<span data-ttu-id="6ad57-109">*IID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6ad57-109">*iid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ad57-110">Identificatore dell'interfaccia chiamata dall'oggetto NPP (ad esempio,**IRTC** o **IDelaydC**).</span><span class="sxs-lookup"><span data-stu-id="6ad57-110">Identifier of the interface that you call from the NPP (**IRTC** or **IDelaydC**, for example).</span></span>

</dd> <dt>

<span data-ttu-id="6ad57-111">*ppvObject* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6ad57-111">*ppvObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ad57-112">Puntatore al puntatore restituito all'interfaccia richiesta.</span><span class="sxs-lookup"><span data-stu-id="6ad57-112">Pointer to the returned pointer to the requested interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ad57-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6ad57-113">Return value</span></span>

<span data-ttu-id="6ad57-114">Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="6ad57-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="6ad57-115">Se la funzione ha esito negativo, il valore restituito è un valore NMERR che descrive l'errore.</span><span class="sxs-lookup"><span data-stu-id="6ad57-115">If the function is unsuccessful, the return value is a NMERR value that describes the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ad57-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6ad57-116">Requirements</span></span>



| <span data-ttu-id="6ad57-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ad57-117">Requirement</span></span> | <span data-ttu-id="6ad57-118">Valore</span><span class="sxs-lookup"><span data-stu-id="6ad57-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ad57-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6ad57-119">Minimum supported client</span></span><br/> | <span data-ttu-id="6ad57-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6ad57-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6ad57-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6ad57-121">Minimum supported server</span></span><br/> | <span data-ttu-id="6ad57-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6ad57-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6ad57-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6ad57-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ad57-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ad57-124"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="6ad57-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="6ad57-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="6ad57-126"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6ad57-126"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="6ad57-127">DLL</span><span class="sxs-lookup"><span data-stu-id="6ad57-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ad57-128"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ad57-128"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




