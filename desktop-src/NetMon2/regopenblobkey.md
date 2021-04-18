---
description: La funzione RegOpenBlobKey recupera un BLOB archiviato nella chiave del registro di sistema specificata.
ms.assetid: f6b16c07-c705-47f1-a21c-6155368551c7
title: Funzione RegOpenBlobKey (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RegOpenBlobKey
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 24d788c8c4b69525d6c0be374845b44f804982bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319404"
---
# <a name="regopenblobkey-function"></a><span data-ttu-id="202ed-103">RegOpenBlobKey (funzione)</span><span class="sxs-lookup"><span data-stu-id="202ed-103">RegOpenBlobKey function</span></span>

<span data-ttu-id="202ed-104">La funzione **RegOpenBlobKey** recupera un BLOB archiviato nella chiave del registro di sistema specificata.</span><span class="sxs-lookup"><span data-stu-id="202ed-104">The **RegOpenBlobKey** function retrieves a BLOB stored at the given registry key.</span></span>

## <a name="syntax"></a><span data-ttu-id="202ed-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="202ed-105">Syntax</span></span>


```C++
DWORD RegOpenBlobKey(
  _In_        HKEY  hkey,
  _In_  const char  *szBlobName,
  _Out_       HBLOB *phBlob
);
```



## <a name="parameters"></a><span data-ttu-id="202ed-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="202ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="202ed-107">*HKEY* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="202ed-107">*hkey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="202ed-108">Handle per la chiave del registro di sistema che contiene il BLOB.</span><span class="sxs-lookup"><span data-stu-id="202ed-108">Handle to the registry key that contains the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="202ed-109">*szBlobName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="202ed-109">*szBlobName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="202ed-110">Nome che identifica il BLOB specificato nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="202ed-110">Name that identifies the given BLOB in the registry.</span></span>

</dd> <dt>

<span data-ttu-id="202ed-111">*phBlob* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="202ed-111">*phBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="202ed-112">Puntatore al BLOB recuperato.</span><span class="sxs-lookup"><span data-stu-id="202ed-112">Pointer to the BLOB that is retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="202ed-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="202ed-113">Return value</span></span>

<span data-ttu-id="202ed-114">Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="202ed-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="202ed-115">Se la funzione ha esito negativo, il valore restituito è un valore NMERR che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="202ed-115">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="202ed-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="202ed-116">Requirements</span></span>



| <span data-ttu-id="202ed-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="202ed-117">Requirement</span></span> | <span data-ttu-id="202ed-118">Valore</span><span class="sxs-lookup"><span data-stu-id="202ed-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="202ed-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="202ed-119">Minimum supported client</span></span><br/> | <span data-ttu-id="202ed-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="202ed-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="202ed-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="202ed-121">Minimum supported server</span></span><br/> | <span data-ttu-id="202ed-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="202ed-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="202ed-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="202ed-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="202ed-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="202ed-124"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="202ed-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="202ed-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="202ed-126"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="202ed-126"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="202ed-127">DLL</span><span class="sxs-lookup"><span data-stu-id="202ed-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="202ed-128"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="202ed-128"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="202ed-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="202ed-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="202ed-130">RegCreateBlobKey</span><span class="sxs-lookup"><span data-stu-id="202ed-130">RegCreateBlobKey</span></span>](regcreateblobkey.md)
</dt> </dl>

 

 




