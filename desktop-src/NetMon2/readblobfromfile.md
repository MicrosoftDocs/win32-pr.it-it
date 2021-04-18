---
description: La funzione ReadBlobFromFile legge un BLOB in un file.
ms.assetid: c3d4a892-160b-48e9-8881-0ada3ebd49b0
title: Funzione ReadBlobFromFile (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReadBlobFromFile
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 66d1f28bd43747adaaecf7fad156d80095a71b5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319407"
---
# <a name="readblobfromfile-function"></a><span data-ttu-id="2b021-103">ReadBlobFromFile (funzione)</span><span class="sxs-lookup"><span data-stu-id="2b021-103">ReadBlobFromFile function</span></span>

<span data-ttu-id="2b021-104">La funzione **ReadBlobFromFile** legge un BLOB in un file.</span><span class="sxs-lookup"><span data-stu-id="2b021-104">The **ReadBlobFromFile** function reads a BLOB in a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b021-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2b021-105">Syntax</span></span>


```C++
DWORD ReadBlobFromFile(
  _In_       HBLOB hBlob,
  _In_ const char  *pFileName
);
```



## <a name="parameters"></a><span data-ttu-id="2b021-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2b021-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b021-107">*hBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2b021-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b021-108">Handle per il BLOB.</span><span class="sxs-lookup"><span data-stu-id="2b021-108">Handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="2b021-109">*pFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2b021-109">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2b021-110">Puntatore al nome del file che contiene il BLOB.</span><span class="sxs-lookup"><span data-stu-id="2b021-110">Pointer to the name of the file that contains the BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b021-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2b021-111">Return value</span></span>

<span data-ttu-id="2b021-112">Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="2b021-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="2b021-113">Se la funzione ha esito negativo, il valore restituito è un valore NMERR che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="2b021-113">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b021-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2b021-114">Requirements</span></span>



| <span data-ttu-id="2b021-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b021-115">Requirement</span></span> | <span data-ttu-id="2b021-116">Valore</span><span class="sxs-lookup"><span data-stu-id="2b021-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2b021-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2b021-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2b021-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2b021-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2b021-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2b021-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2b021-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2b021-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2b021-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2b021-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b021-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="2b021-122"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="2b021-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="2b021-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="2b021-124"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2b021-124"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="2b021-125">DLL</span><span class="sxs-lookup"><span data-stu-id="2b021-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2b021-126"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2b021-126"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




