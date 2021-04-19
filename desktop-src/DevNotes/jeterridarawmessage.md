---
description: Recupera una stringa di messaggio non formattata quando viene fornito un identificatore del codice di errore (IDA).
ms.assetid: 3869e0c0-b3ec-4409-b071-04fd793ebf93
title: JetErrIDARawMessage (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JetErrIDARawMessage
api_type:
- DllExport
api_location:
- Msjter40.dll
ms.openlocfilehash: 8a904a99577a6fa0fd6955f4c78906b470ea96b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332277"
---
# <a name="jeterridarawmessage-function"></a><span data-ttu-id="9570d-103">JetErrIDARawMessage (funzione)</span><span class="sxs-lookup"><span data-stu-id="9570d-103">JetErrIDARawMessage function</span></span>

<span data-ttu-id="9570d-104">Recupera una stringa di messaggio non formattata quando viene fornito un identificatore del codice di errore (IDA).</span><span class="sxs-lookup"><span data-stu-id="9570d-104">Retrieves an unformatted message string when an error code identifier (IDA) is provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="9570d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9570d-105">Syntax</span></span>


```C++
JET_ERR JetErrIDARawMessage(
   JETERR_IDA           Ida,
   WCHAR                *pMessage,
   unsigned long        cbMessage,
   unsigned long        *pcbActual,
   JETERR_HELPCONTEXTID *pContextId,
   WCHAR                **pwszHelp/file
);
```



## <a name="parameters"></a><span data-ttu-id="9570d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9570d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9570d-107">*Ida*</span><span class="sxs-lookup"><span data-stu-id="9570d-107">*Ida*</span></span> 
</dt> <dd>

<span data-ttu-id="9570d-108">Numero che esegue il mapping a un codice di errore specifico e viene visualizzato all'utente.</span><span class="sxs-lookup"><span data-stu-id="9570d-108">A number that maps to a specific error code and is displayed to the user.</span></span>

</dd> <dt>

<span data-ttu-id="9570d-109">*pMessage*</span><span class="sxs-lookup"><span data-stu-id="9570d-109">*pMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="9570d-110">Puntatore al messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="9570d-110">A pointer to the error message.</span></span>

</dd> <dt>

<span data-ttu-id="9570d-111">*cbMessage*</span><span class="sxs-lookup"><span data-stu-id="9570d-111">*cbMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="9570d-112">Conteggio del numero di byte nel messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="9570d-112">A count of the number of bytes in the error message.</span></span>

</dd> <dt>

<span data-ttu-id="9570d-113">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="9570d-113">*pcbActual*</span></span> 
</dt> <dd>

<span data-ttu-id="9570d-114">Puntatore al numero effettivo di byte letti.</span><span class="sxs-lookup"><span data-stu-id="9570d-114">A pointer to the actual number of bytes read.</span></span>

</dd> <dt>

<span data-ttu-id="9570d-115">*pContextId*</span><span class="sxs-lookup"><span data-stu-id="9570d-115">*pContextId*</span></span> 
</dt> <dd>

<span data-ttu-id="9570d-116">Puntatore all'identificatore di contesto associato al file della guida.</span><span class="sxs-lookup"><span data-stu-id="9570d-116">A pointer to the context identifier that is associated with the help file.</span></span>

</dd> <dt>

<span data-ttu-id="9570d-117">*pwszHelp/file*</span><span class="sxs-lookup"><span data-stu-id="9570d-117">*pwszHelp/file*</span></span> 
</dt> <dd>

<span data-ttu-id="9570d-118">Puntatore a un puntatore al file che spiega l'errore.</span><span class="sxs-lookup"><span data-stu-id="9570d-118">A pointer to a pointer to the file that explains the error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9570d-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9570d-119">Return value</span></span>

<span data-ttu-id="9570d-120">Se la funzione ha esito positivo, restituisce **Jet \_ errSuccess**. in caso contrario, restituisce un messaggio non formattato che indica il motivo specifico dell'errore.</span><span class="sxs-lookup"><span data-stu-id="9570d-120">If the function succeeds, it returns **JET\_errSuccess**; otherwise, it returns an unformatted message that indicates the specific reason for failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="9570d-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="9570d-121">Remarks</span></span>

<span data-ttu-id="9570d-122">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="9570d-122">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="9570d-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9570d-123">Requirements</span></span>



| <span data-ttu-id="9570d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="9570d-124">Requirement</span></span> | <span data-ttu-id="9570d-125">Valore</span><span class="sxs-lookup"><span data-stu-id="9570d-125">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9570d-126">DLL</span><span class="sxs-lookup"><span data-stu-id="9570d-126">DLL</span></span><br/> | <dl> <span data-ttu-id="9570d-127"><dt>Msjter40.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9570d-127"><dt>Msjter40.dll</dt></span></span> </dl> |



 

 
