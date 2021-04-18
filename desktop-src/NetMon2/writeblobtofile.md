---
description: La funzione WriteBlobToFile scrive un BLOB in un file.
ms.assetid: 0793dced-82c2-4553-90b2-acf594c6749e
title: Funzione WriteBlobToFile (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WriteBlobToFile
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 5fbf17b76631da6dbff9ef2077776106505a37b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315445"
---
# <a name="writeblobtofile-function"></a><span data-ttu-id="930f6-103">WriteBlobToFile (funzione)</span><span class="sxs-lookup"><span data-stu-id="930f6-103">WriteBlobToFile function</span></span>

<span data-ttu-id="930f6-104">La funzione **WriteBlobToFile** scrive un BLOB in un file.</span><span class="sxs-lookup"><span data-stu-id="930f6-104">The **WriteBlobToFile** function writes a BLOB to a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="930f6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="930f6-105">Syntax</span></span>


```C++
DWORD WriteBlobToFile(
  _In_       HBLOB hBlob,
  _In_ const char  *pFileName
);
```



## <a name="parameters"></a><span data-ttu-id="930f6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="930f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="930f6-107">*hBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="930f6-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="930f6-108">Handle per il BLOB.</span><span class="sxs-lookup"><span data-stu-id="930f6-108">Handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="930f6-109">*pFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="930f6-109">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="930f6-110">Puntatore al nome del file in cui il BLOB viene salvato.</span><span class="sxs-lookup"><span data-stu-id="930f6-110">Pointer to the name of the file, in which the BLOB is saved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="930f6-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="930f6-111">Return value</span></span>

<span data-ttu-id="930f6-112">Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="930f6-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="930f6-113">Se la funzione ha esito negativo, il valore restituito è un valore NMERR che indica l'errore.</span><span class="sxs-lookup"><span data-stu-id="930f6-113">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="930f6-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="930f6-114">Requirements</span></span>



| <span data-ttu-id="930f6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="930f6-115">Requirement</span></span> | <span data-ttu-id="930f6-116">Valore</span><span class="sxs-lookup"><span data-stu-id="930f6-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="930f6-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="930f6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="930f6-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="930f6-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="930f6-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="930f6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="930f6-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="930f6-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="930f6-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="930f6-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="930f6-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="930f6-122"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="930f6-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="930f6-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="930f6-124"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="930f6-124"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="930f6-125">DLL</span><span class="sxs-lookup"><span data-stu-id="930f6-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="930f6-126"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="930f6-126"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




