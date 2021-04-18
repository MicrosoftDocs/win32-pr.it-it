---
description: Inizializza una tabella di stringhe.
ms.assetid: 184df85a-6d59-42c5-8ec1-f0c046091645
title: pSetupStringTableInitializeEx (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupStringTableInitializeEx
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: d40f221656da4cada610e7254b392bb2bd627a14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325201"
---
# <a name="psetupstringtableinitializeex-function"></a><span data-ttu-id="8c799-103">pSetupStringTableInitializeEx (funzione)</span><span class="sxs-lookup"><span data-stu-id="8c799-103">pSetupStringTableInitializeEx function</span></span>

<span data-ttu-id="8c799-104">\[Questa funzione non è disponibile in Windows Vista o Windows Server 2008.\]</span><span class="sxs-lookup"><span data-stu-id="8c799-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="8c799-105">Inizializza una tabella di stringhe.</span><span class="sxs-lookup"><span data-stu-id="8c799-105">Initializes a string table.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c799-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8c799-106">Syntax</span></span>


```C++
PVOID pSetupStringTableInitializeEx(
  _In_ UINT ExtraDataSize,
  _In_ UINT Reserved
);
```



## <a name="parameters"></a><span data-ttu-id="8c799-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="8c799-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c799-108">*ExtraDataSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8c799-108">*ExtraDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c799-109">Dimensioni dell'oggetto dati aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="8c799-109">Size of extra data object.</span></span>

</dd> <dt>

<span data-ttu-id="8c799-110">*Riservato* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8c799-110">*Reserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c799-111">Riservato.</span><span class="sxs-lookup"><span data-stu-id="8c799-111">Reserved.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8c799-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="8c799-112">Remarks</span></span>

<span data-ttu-id="8c799-113">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="8c799-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c799-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8c799-114">Requirements</span></span>



| <span data-ttu-id="8c799-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c799-115">Requirement</span></span> | <span data-ttu-id="8c799-116">Valore</span><span class="sxs-lookup"><span data-stu-id="8c799-116">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c799-117">DLL</span><span class="sxs-lookup"><span data-stu-id="8c799-117">DLL</span></span><br/> | <dl> <span data-ttu-id="8c799-118"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c799-118"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
