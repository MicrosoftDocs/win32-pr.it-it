---
description: Recupera un identificatore del codice di errore (IDA) e una stringa di messaggio non formattato quando viene fornito un errore Jet.
ms.assetid: f90b6986-a8d5-430e-94b3-176012c7e282
title: JetErrRawMessage (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JetErrRawMessage
api_type:
- DllExport
api_location:
- Msjter40.dll
ms.openlocfilehash: 1b52fa519bee3abacd0cd9bd7e8eaaa0676d007c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324797"
---
# <a name="jeterrrawmessage-function"></a><span data-ttu-id="58921-103">JetErrRawMessage (funzione)</span><span class="sxs-lookup"><span data-stu-id="58921-103">JetErrRawMessage function</span></span>

<span data-ttu-id="58921-104">Recupera un identificatore del codice di errore (IDA) e una stringa di messaggio non formattato quando viene fornito un errore Jet.</span><span class="sxs-lookup"><span data-stu-id="58921-104">Retrieves an error code identifier (IDA) and an unformatted message string when a Jet error is provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="58921-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="58921-105">Syntax</span></span>


```C++
JET_ERR JetErrRawMessage(
   JET_ERR              err,
   JETERR_IDA           *pIda,
   WCHAR                *pMessage,
   unsigned long        cbMessage,
   unsigned long        *pcbActual,
   JETERR_HELPCONTEXTID *pContextId,
   WCHAR                **pwszHelp/file
);
```



## <a name="parameters"></a><span data-ttu-id="58921-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="58921-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58921-107">*Err*</span><span class="sxs-lookup"><span data-stu-id="58921-107">*err*</span></span> 
</dt> <dd>

<span data-ttu-id="58921-108">Errore Jet che corrisponde alle informazioni ottenute.</span><span class="sxs-lookup"><span data-stu-id="58921-108">The Jet error that corresponds to the information being obtained.</span></span>

</dd> <dt>

<span data-ttu-id="58921-109">*pIda*</span><span class="sxs-lookup"><span data-stu-id="58921-109">*pIda*</span></span> 
</dt> <dd>

<span data-ttu-id="58921-110">Puntatore a IDA.</span><span class="sxs-lookup"><span data-stu-id="58921-110">A pointer to the IDA.</span></span>

</dd> <dt>

<span data-ttu-id="58921-111">*pMessage*</span><span class="sxs-lookup"><span data-stu-id="58921-111">*pMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="58921-112">Puntatore al messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="58921-112">A pointer to the error message.</span></span>

</dd> <dt>

<span data-ttu-id="58921-113">*cbMessage*</span><span class="sxs-lookup"><span data-stu-id="58921-113">*cbMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="58921-114">Conteggio del numero di byte nel messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="58921-114">A count of the number of bytes in the error message.</span></span>

</dd> <dt>

<span data-ttu-id="58921-115">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="58921-115">*pcbActual*</span></span> 
</dt> <dd>

<span data-ttu-id="58921-116">Puntatore al numero effettivo di byte letti.</span><span class="sxs-lookup"><span data-stu-id="58921-116">A pointer to the actual number of bytes read.</span></span>

</dd> <dt>

<span data-ttu-id="58921-117">*pContextId*</span><span class="sxs-lookup"><span data-stu-id="58921-117">*pContextId*</span></span> 
</dt> <dd>

<span data-ttu-id="58921-118">Puntatore all'identificatore di contesto associato al file della guida.</span><span class="sxs-lookup"><span data-stu-id="58921-118">A pointer to the context identifier that is associated with the help file.</span></span>

</dd> <dt>

<span data-ttu-id="58921-119">*pwszHelp/file*</span><span class="sxs-lookup"><span data-stu-id="58921-119">*pwszHelp/file*</span></span> 
</dt> <dd>

<span data-ttu-id="58921-120">Punta a un puntatore al file che spiega l'errore.</span><span class="sxs-lookup"><span data-stu-id="58921-120">Points to a pointer to the file that explains the error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58921-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="58921-121">Return value</span></span>

<span data-ttu-id="58921-122">Se la funzione ha esito positivo, restituisce **Jet \_ errSuccess**. in caso contrario, restituisce un messaggio di errore non formattato che indica il motivo specifico dell'errore.</span><span class="sxs-lookup"><span data-stu-id="58921-122">If the function succeeds, it returns **JET\_errSuccess**; otherwise, it returns an unformatted error message that indicates the specific reason for failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="58921-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="58921-123">Remarks</span></span>

<span data-ttu-id="58921-124">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="58921-124">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="58921-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="58921-125">Requirements</span></span>



| <span data-ttu-id="58921-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="58921-126">Requirement</span></span> | <span data-ttu-id="58921-127">Valore</span><span class="sxs-lookup"><span data-stu-id="58921-127">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="58921-128">DLL</span><span class="sxs-lookup"><span data-stu-id="58921-128">DLL</span></span><br/> | <dl> <span data-ttu-id="58921-129"><dt>Msjter40.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58921-129"><dt>Msjter40.dll</dt></span></span> </dl> |



 

 
