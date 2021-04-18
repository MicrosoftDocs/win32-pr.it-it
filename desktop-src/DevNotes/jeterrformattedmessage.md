---
description: Recupera un identificatore del codice di errore (IDA) e crea la stringa di visualizzazione finale quando vengono forniti un errore Jet e informazioni estese sull'errore.
ms.assetid: 961da4fb-cb70-4f3d-a4a4-1774be7a05f4
title: JetErrFormattedMessage (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JetErrFormattedMessage
api_type:
- DllExport
api_location:
- Msjter40.dll
ms.openlocfilehash: 75cdf93b4c35a8c7b3dd77fca42c205d898f6e97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324702"
---
# <a name="jeterrformattedmessage-function"></a><span data-ttu-id="2d695-103">JetErrFormattedMessage (funzione)</span><span class="sxs-lookup"><span data-stu-id="2d695-103">JetErrFormattedMessage function</span></span>

<span data-ttu-id="2d695-104">Recupera un identificatore del codice di errore (IDA) e crea la stringa di visualizzazione finale quando vengono forniti un errore Jet e informazioni estese sull'errore.</span><span class="sxs-lookup"><span data-stu-id="2d695-104">Retrieves an error code identifier (IDA) and creates the final display string when a Jet error and extended error information is provided.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d695-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2d695-105">Syntax</span></span>


```C++
JET_ERR JetErrFormattedMessage(
   JET_ERR              err,
   JETERR_EXTERR        *pExtendedErrorInfo,
   JETERR_IDA           *pIda,
   WCHAR                *pMessage,
   unsigned long        cbMessage,
   unsigned long        *pcbActual,
   JETERR_HELPCONTEXTID *pContextId,
   WCHAR                **pwszHelp/file
);
```



## <a name="parameters"></a><span data-ttu-id="2d695-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2d695-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d695-107">*Err*</span><span class="sxs-lookup"><span data-stu-id="2d695-107">*err*</span></span> 
</dt> <dd>

<span data-ttu-id="2d695-108">Numero di errore Jet utilizzato per cercare e formattare il messaggio di errore visualizzabile.</span><span class="sxs-lookup"><span data-stu-id="2d695-108">The Jet error number that is used to look up and format the displayable error message.</span></span>

</dd> <dt>

<span data-ttu-id="2d695-109">*pExtendedErrorInfo*</span><span class="sxs-lookup"><span data-stu-id="2d695-109">*pExtendedErrorInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="2d695-110">Tutte le informazioni sull'errore Jet, inclusi il nome del database, il nome della tabella e qualsiasi informazione secondaria sugli errori.</span><span class="sxs-lookup"><span data-stu-id="2d695-110">All Jet error information including the database name, the table name, and any minor error information.</span></span>

</dd> <dt>

<span data-ttu-id="2d695-111">*pIda*</span><span class="sxs-lookup"><span data-stu-id="2d695-111">*pIda*</span></span> 
</dt> <dd>

<span data-ttu-id="2d695-112">Puntatore a IDA associato al codice di errore specifico.</span><span class="sxs-lookup"><span data-stu-id="2d695-112">A pointer to the IDA that is associated with the specific error code.</span></span>

</dd> <dt>

<span data-ttu-id="2d695-113">*pMessage*</span><span class="sxs-lookup"><span data-stu-id="2d695-113">*pMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="2d695-114">Puntatore al messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="2d695-114">A pointer to the error message.</span></span>

</dd> <dt>

<span data-ttu-id="2d695-115">*cbMessage*</span><span class="sxs-lookup"><span data-stu-id="2d695-115">*cbMessage*</span></span> 
</dt> <dd>

<span data-ttu-id="2d695-116">Conteggio del numero di byte nel messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="2d695-116">A count of the number of bytes in the error message.</span></span>

</dd> <dt>

<span data-ttu-id="2d695-117">*pcbActual*</span><span class="sxs-lookup"><span data-stu-id="2d695-117">*pcbActual*</span></span> 
</dt> <dd>

<span data-ttu-id="2d695-118">Puntatore al numero effettivo di byte letti.</span><span class="sxs-lookup"><span data-stu-id="2d695-118">A pointer to the actual number of bytes read.</span></span>

</dd> <dt>

<span data-ttu-id="2d695-119">*pContextId*</span><span class="sxs-lookup"><span data-stu-id="2d695-119">*pContextId*</span></span> 
</dt> <dd>

<span data-ttu-id="2d695-120">Puntatore all'identificatore di contesto associato al file della guida.</span><span class="sxs-lookup"><span data-stu-id="2d695-120">A pointer to the context identifier that is associated with the help file.</span></span>

</dd> <dt>

<span data-ttu-id="2d695-121">*pwszHelp/file*</span><span class="sxs-lookup"><span data-stu-id="2d695-121">*pwszHelp/file*</span></span> 
</dt> <dd>

<span data-ttu-id="2d695-122">Puntatore a un puntatore al file che spiega l'errore.</span><span class="sxs-lookup"><span data-stu-id="2d695-122">A pointer to a pointer to the file that explains the error.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d695-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2d695-123">Return value</span></span>

<span data-ttu-id="2d695-124">Se la funzione ha esito positivo, restituisce **Jet \_ errSuccess**. in caso contrario, restituisce un messaggio di errore formattato che indica la causa specifica dell'errore.</span><span class="sxs-lookup"><span data-stu-id="2d695-124">If the function succeeds, it returns **JET\_errSuccess**; otherwise, it returns a formatted error message that indicates the specific reason for failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d695-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="2d695-125">Remarks</span></span>

<span data-ttu-id="2d695-126">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="2d695-126">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d695-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2d695-127">Requirements</span></span>



| <span data-ttu-id="2d695-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d695-128">Requirement</span></span> | <span data-ttu-id="2d695-129">Valore</span><span class="sxs-lookup"><span data-stu-id="2d695-129">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2d695-130">DLL</span><span class="sxs-lookup"><span data-stu-id="2d695-130">DLL</span></span><br/> | <dl> <span data-ttu-id="2d695-131"><dt>Msjter40.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d695-131"><dt>Msjter40.dll</dt></span></span> </dl> |



 

 
