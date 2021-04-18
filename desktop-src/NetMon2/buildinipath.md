---
description: La funzione BuildINIPath restituisce il percorso completo di un file INI che corrisponde alle informazioni immesse.
ms.assetid: 214ce89c-8bb2-4e1a-872a-026743a3e3a6
title: Funzione BuildINIPath (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BuildINIPath
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 3f715e740319515fe4772d1a9905a2f9b563f3cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314186"
---
# <a name="buildinipath-function"></a><span data-ttu-id="03c83-103">BuildINIPath (funzione)</span><span class="sxs-lookup"><span data-stu-id="03c83-103">BuildINIPath function</span></span>

<span data-ttu-id="03c83-104">La funzione **BuildINIPath** restituisce il percorso completo di un file ini che corrisponde alle informazioni immesse.</span><span class="sxs-lookup"><span data-stu-id="03c83-104">The **BuildINIPath** function returns a fully qualified path to an INI file that corresponds to information you enter.</span></span>

## <a name="syntax"></a><span data-ttu-id="03c83-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="03c83-105">Syntax</span></span>


```C++
LPSTR BuildINIPath(
   char *FullPath,
   char *IniFileName
);
```



## <a name="parameters"></a><span data-ttu-id="03c83-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="03c83-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03c83-107">*FullPath*</span><span class="sxs-lookup"><span data-stu-id="03c83-107">*FullPath*</span></span> 
</dt> <dd>

<span data-ttu-id="03c83-108">Buffer che riceve il nome completo del file INI.</span><span class="sxs-lookup"><span data-stu-id="03c83-108">Buffer that receives the fully qualified INI file name.</span></span>

</dd> <dt>

<span data-ttu-id="03c83-109">*IniFileName*</span><span class="sxs-lookup"><span data-stu-id="03c83-109">*IniFileName*</span></span> 
</dt> <dd>

<span data-ttu-id="03c83-110">Nome del file INI (il nome file completo meno l'estensione filename).</span><span class="sxs-lookup"><span data-stu-id="03c83-110">Name of the INI file (the full file name minus the filename extension).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03c83-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="03c83-111">Return value</span></span>

<span data-ttu-id="03c83-112">Se la funzione ha esito positivo, il valore restituito è un puntatore al nome completo del file INI.</span><span class="sxs-lookup"><span data-stu-id="03c83-112">If the function is successful, the return value is a pointer to the fully qualified INI file name.</span></span>

<span data-ttu-id="03c83-113">Se la funzione ha esito negativo, il valore restituito è **null**.</span><span class="sxs-lookup"><span data-stu-id="03c83-113">If the function is unsuccessful, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="03c83-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="03c83-114">Remarks</span></span>

<span data-ttu-id="03c83-115">Il percorso restituito da questa funzione è il percorso completo di un file INI che corrisponde alle informazioni immesse.</span><span class="sxs-lookup"><span data-stu-id="03c83-115">The path that this function returns is a fully qualified path to an INI file that corresponds to information you enter.</span></span> <span data-ttu-id="03c83-116">Se ad esempio si immette XNS o TCP, la funzione genera un percorso rispettivamente per Xns.ini o Tcp.ini.</span><span class="sxs-lookup"><span data-stu-id="03c83-116">For example, if you enter XNS or TCP, the function generates a path to Xns.ini or Tcp.ini, respectively.</span></span>

## <a name="requirements"></a><span data-ttu-id="03c83-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="03c83-117">Requirements</span></span>



| <span data-ttu-id="03c83-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="03c83-118">Requirement</span></span> | <span data-ttu-id="03c83-119">Valore</span><span class="sxs-lookup"><span data-stu-id="03c83-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="03c83-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03c83-120">Minimum supported client</span></span><br/> | <span data-ttu-id="03c83-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="03c83-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="03c83-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03c83-122">Minimum supported server</span></span><br/> | <span data-ttu-id="03c83-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="03c83-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="03c83-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="03c83-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="03c83-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="03c83-125"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="03c83-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="03c83-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="03c83-127"><dt>Parser. lib</dt></span><span class="sxs-lookup"><span data-stu-id="03c83-127"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="03c83-128">DLL</span><span class="sxs-lookup"><span data-stu-id="03c83-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03c83-129"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03c83-129"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




