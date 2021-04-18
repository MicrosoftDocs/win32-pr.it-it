---
description: La funzione RegCreateBlobKey archivia un BLOB nella chiave del registro di sistema specificata.
ms.assetid: 14f3763e-aa04-4d51-b388-81ebf0d3952c
title: Funzione RegCreateBlobKey (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RegCreateBlobKey
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: fc46b38919b37dc004c1065b0cc8d5f80e65984c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319405"
---
# <a name="regcreateblobkey-function"></a><span data-ttu-id="ca10e-103">RegCreateBlobKey (funzione)</span><span class="sxs-lookup"><span data-stu-id="ca10e-103">RegCreateBlobKey function</span></span>

<span data-ttu-id="ca10e-104">La funzione **RegCreateBlobKey** archivia un BLOB nella chiave del registro di sistema specificata.</span><span class="sxs-lookup"><span data-stu-id="ca10e-104">The **RegCreateBlobKey** function stores a BLOB at the given registry key.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca10e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ca10e-105">Syntax</span></span>


```C++
DWORD RegCreateBlobKey(
  _Out_       HKEY  hkey,
  _In_  const char  *szBlobName,
  _In_        HBLOB hBlob
);
```



## <a name="parameters"></a><span data-ttu-id="ca10e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ca10e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca10e-107">*HKEY* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ca10e-107">*hkey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ca10e-108">Handle per la chiave del registro di sistema in cui verrà archiviato il BLOB.</span><span class="sxs-lookup"><span data-stu-id="ca10e-108">Handle to the registry key where the BLOB will be stored.</span></span>

</dd> <dt>

<span data-ttu-id="ca10e-109">*szBlobName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ca10e-109">*szBlobName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca10e-110">Nome (applicazione definita) che rappresenta il BLOB nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="ca10e-110">Name (application defined) that represents the BLOB in the registry.</span></span>

</dd> <dt>

<span data-ttu-id="ca10e-111">*hBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ca10e-111">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca10e-112">Handle per il BLOB salvato.</span><span class="sxs-lookup"><span data-stu-id="ca10e-112">Handle to the BLOB that is saved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca10e-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ca10e-113">Return value</span></span>

<span data-ttu-id="ca10e-114">Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="ca10e-114">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="ca10e-115">Se la funzione ha esito negativo, il valore restituito è un valore NMERR che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="ca10e-115">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca10e-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ca10e-116">Requirements</span></span>



| <span data-ttu-id="ca10e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca10e-117">Requirement</span></span> | <span data-ttu-id="ca10e-118">Valore</span><span class="sxs-lookup"><span data-stu-id="ca10e-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca10e-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca10e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ca10e-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ca10e-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ca10e-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ca10e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ca10e-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="ca10e-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ca10e-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ca10e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca10e-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ca10e-124"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="ca10e-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="ca10e-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="ca10e-126"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ca10e-126"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="ca10e-127">DLL</span><span class="sxs-lookup"><span data-stu-id="ca10e-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca10e-128"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca10e-128"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca10e-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ca10e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca10e-130">RegOpenBlobKey</span><span class="sxs-lookup"><span data-stu-id="ca10e-130">RegOpenBlobKey</span></span>](regopenblobkey.md)
</dt> </dl>

 

 




