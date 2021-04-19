---
description: Recupera gli attributi di base per l'oggetto file specificato.
ms.assetid: 19f9a2ac-4db6-4c67-9f85-c107063e11b8
title: NtQueryAttributesFile (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQueryAttributesFile
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: a1d6d2ff20539f5ef65c0886ba51a0dbabafb44d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326093"
---
# <a name="ntqueryattributesfile-function"></a><span data-ttu-id="ed2a5-103">NtQueryAttributesFile (funzione)</span><span class="sxs-lookup"><span data-stu-id="ed2a5-103">NtQueryAttributesFile function</span></span>

<span data-ttu-id="ed2a5-104">\[Questa funzione può essere modificata o rimossa da Windows senza ulteriore preavviso.\]</span><span class="sxs-lookup"><span data-stu-id="ed2a5-104">\[This function may be changed or removed from Windows without further notice.\]</span></span>

<span data-ttu-id="ed2a5-105">Recupera gli attributi di base per l'oggetto file specificato.</span><span class="sxs-lookup"><span data-stu-id="ed2a5-105">Retrieves basic attributes for the specified file object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed2a5-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ed2a5-106">Syntax</span></span>


```C++
NTSTATUS NtQueryAttributesFile(
  _In_  POBJECT_ATTRIBUTES      ObjectAttributes,
  _Out_ PFILE_BASIC_INFORMATION FileInformation
);
```



## <a name="parameters"></a><span data-ttu-id="ed2a5-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="ed2a5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed2a5-108">*ObjectAttributes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ed2a5-108">*ObjectAttributes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed2a5-109">Puntatore a una struttura [degli \_ attributi dell'oggetto](https://msdn.microsoft.com/library/aa491657.aspx) che fornisce gli attributi da utilizzare per l'oggetto file.</span><span class="sxs-lookup"><span data-stu-id="ed2a5-109">A pointer to an [OBJECT\_ATTRIBUTES](https://msdn.microsoft.com/library/aa491657.aspx) structure that supplies the attributes to be used for the file object.</span></span>

</dd> <dt>

<span data-ttu-id="ed2a5-110">*Informazioni FileInformation* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ed2a5-110">*FileInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed2a5-111">Puntatore a una struttura [di \_ \_ informazioni di base del file](https://msdn.microsoft.com/library/aa491634.aspx) per ricevere le informazioni sugli attributi del file restituito.</span><span class="sxs-lookup"><span data-stu-id="ed2a5-111">A pointer to a [FILE\_BASIC\_INFORMATION](https://msdn.microsoft.com/library/aa491634.aspx) structure to receive the returned file attribute information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed2a5-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ed2a5-112">Return value</span></span>

<span data-ttu-id="ed2a5-113">Restituisce un codice NTSTATUS o Error.</span><span class="sxs-lookup"><span data-stu-id="ed2a5-113">Returns an NTSTATUS or error code.</span></span>

<span data-ttu-id="ed2a5-114">I moduli e il significato dei codici di errore NTSTATUS sono elencati nel file di intestazione Ntstatus. h disponibile in WDK e sono descritti nella documentazione di WDK.</span><span class="sxs-lookup"><span data-stu-id="ed2a5-114">The forms and significance of NTSTATUS error codes are listed in the Ntstatus.h header file available in the WDK, and are described in the WDK documentation.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed2a5-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="ed2a5-115">Remarks</span></span>

<span data-ttu-id="ed2a5-116">A questa funzione non è associato alcun file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="ed2a5-116">This function has no associated header file.</span></span> <span data-ttu-id="ed2a5-117">La libreria di importazione associata, Ntdll. lib, è disponibile in WDK.</span><span class="sxs-lookup"><span data-stu-id="ed2a5-117">The associated import library, Ntdll.lib, is available in the WDK.</span></span> <span data-ttu-id="ed2a5-118">È anche possibile usare le funzioni [**LoadLibrary**](-loadlibrary.md) e [**GetProcAddress**](-getprocaddress-.md) per eseguire un collegamento dinamico a Ntdll.dll.</span><span class="sxs-lookup"><span data-stu-id="ed2a5-118">You can also use the [**LoadLibrary**](-loadlibrary.md) and [**GetProcAddress**](-getprocaddress-.md) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed2a5-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ed2a5-119">Requirements</span></span>



| <span data-ttu-id="ed2a5-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed2a5-120">Requirement</span></span> | <span data-ttu-id="ed2a5-121">Valore</span><span class="sxs-lookup"><span data-stu-id="ed2a5-121">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ed2a5-122">DLL</span><span class="sxs-lookup"><span data-stu-id="ed2a5-122">DLL</span></span><br/> | <dl> <span data-ttu-id="ed2a5-123"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed2a5-123"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 




