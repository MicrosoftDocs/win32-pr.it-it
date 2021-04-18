---
description: Recupera il tipo MAC dalla categoria NetworkInfo della sezione NPP del BLOB e converte i dati del tipo in un numero di tipo MAC.
ms.assetid: 53aa538c-69ee-4b34-93fb-9e61c6baadea
title: Funzione GetNPPMacTypeAsNumber (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPMacTypeAsNumber
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 9174b1deeb04d8d9665509daeff56d832d447892
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525134"
---
# <a name="getnppmactypeasnumber-function"></a><span data-ttu-id="3086a-103">GetNPPMacTypeAsNumber (funzione)</span><span class="sxs-lookup"><span data-stu-id="3086a-103">GetNPPMacTypeAsNumber function</span></span>

<span data-ttu-id="3086a-104">La funzione **GetNPPMacTypeAsNumber** Recupera il tipo Mac dalla categoria networkInfo della sezione NPP del BLOB e converte i dati del tipo in un numero di tipo Mac.</span><span class="sxs-lookup"><span data-stu-id="3086a-104">The **GetNPPMacTypeAsNumber** function retrieves the MAC type from the NetworkInfo category of the NPP section of the BLOB and converts the type data into a MAC type number.</span></span>

## <a name="syntax"></a><span data-ttu-id="3086a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3086a-105">Syntax</span></span>


```C++
DWORD GetNPPMacTypeAsNumber(
  _In_  HBLOB   hBlob,
  _Out_ LPDWORD lpMacType
);
```



## <a name="parameters"></a><span data-ttu-id="3086a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3086a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3086a-107">*hBlob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3086a-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3086a-108">Handle per il BLOB specificato.</span><span class="sxs-lookup"><span data-stu-id="3086a-108">A handle to the specified BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="3086a-109">*lpMacType* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3086a-109">*lpMacType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3086a-110">Puntatore al tipo MAC.</span><span class="sxs-lookup"><span data-stu-id="3086a-110">A pointer to the MAC type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3086a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3086a-111">Return value</span></span>

<span data-ttu-id="3086a-112">Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="3086a-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="3086a-113">Se il tag non è disponibile, il valore restituito è il \_ tipo Mac \_ Unknown.</span><span class="sxs-lookup"><span data-stu-id="3086a-113">If the tag is unavailable, the return value is MAC\_TYPE\_UNKNOWN.</span></span>

## <a name="remarks"></a><span data-ttu-id="3086a-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="3086a-114">Remarks</span></span>

<span data-ttu-id="3086a-115">Questa funzione esegue il mapping del tag, **NPP: networkInfo: MacType** al **\_ tipo \_ \* Mac** come definito nel file Npptypes. h.</span><span class="sxs-lookup"><span data-stu-id="3086a-115">This function maps the tag, **NPP:NetworkInfo:MacType** to the **MAC\_TYPE\_\*** as defined in the Npptypes.h file.</span></span>

## <a name="requirements"></a><span data-ttu-id="3086a-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3086a-116">Requirements</span></span>



| <span data-ttu-id="3086a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3086a-117">Requirement</span></span> | <span data-ttu-id="3086a-118">Valore</span><span class="sxs-lookup"><span data-stu-id="3086a-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3086a-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3086a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3086a-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3086a-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3086a-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3086a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3086a-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3086a-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3086a-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3086a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3086a-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="3086a-124"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="3086a-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="3086a-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="3086a-126"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3086a-126"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="3086a-127">DLL</span><span class="sxs-lookup"><span data-stu-id="3086a-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3086a-128"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3086a-128"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




