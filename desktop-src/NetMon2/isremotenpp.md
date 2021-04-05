---
description: La funzione IsRemoteNPP indica se il BLOB specificato specifica un oggetto NPP remoto.
ms.assetid: 66ee0a9a-3199-479f-baec-da6ae6b46c65
title: Funzione IsRemoteNPP (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsRemoteNPP
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: c52346f368c0720601423f258e4dc73c27296311
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755391"
---
# <a name="isremotenpp-function"></a><span data-ttu-id="d08f5-103">IsRemoteNPP (funzione)</span><span class="sxs-lookup"><span data-stu-id="d08f5-103">IsRemoteNPP function</span></span>

<span data-ttu-id="d08f5-104">La funzione **IsRemoteNPP** indica se il blob specificato specifica un oggetto NPP remoto.</span><span class="sxs-lookup"><span data-stu-id="d08f5-104">The **IsRemoteNPP** function indicates whether the given BLOB specifies a remote NPP.</span></span>

## <a name="syntax"></a><span data-ttu-id="d08f5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d08f5-105">Syntax</span></span>


```C++
BOOL IsRemoteNPP(
  _In_ HBLOB hBlob
);
```



## <a name="parameters"></a><span data-ttu-id="d08f5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d08f5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d08f5-107">*hBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d08f5-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d08f5-108">Handle per un BLOB.</span><span class="sxs-lookup"><span data-stu-id="d08f5-108">Handle to a BLOB.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d08f5-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d08f5-109">Return value</span></span>

<span data-ttu-id="d08f5-110">Se la funzione ha esito positivo, il valore restituito è **true**.</span><span class="sxs-lookup"><span data-stu-id="d08f5-110">If the function is successful, the return value is **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d08f5-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="d08f5-111">Remarks</span></span>

<span data-ttu-id="d08f5-112">Utilizzare questa funzione per verificare se esiste una categoria remota.</span><span class="sxs-lookup"><span data-stu-id="d08f5-112">Use this function to test whether a remote category exists.</span></span>

<span data-ttu-id="d08f5-113">Verificare che i nomi dei computer locali e remoti siano diversi.</span><span class="sxs-lookup"><span data-stu-id="d08f5-113">Make certain that the remote and local computer names are different.</span></span>

## <a name="requirements"></a><span data-ttu-id="d08f5-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d08f5-114">Requirements</span></span>



| <span data-ttu-id="d08f5-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d08f5-115">Requirement</span></span> | <span data-ttu-id="d08f5-116">Valore</span><span class="sxs-lookup"><span data-stu-id="d08f5-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d08f5-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d08f5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d08f5-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d08f5-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d08f5-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d08f5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d08f5-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d08f5-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d08f5-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d08f5-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d08f5-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d08f5-122"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="d08f5-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="d08f5-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="d08f5-124"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d08f5-124"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="d08f5-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d08f5-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d08f5-126"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d08f5-126"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




