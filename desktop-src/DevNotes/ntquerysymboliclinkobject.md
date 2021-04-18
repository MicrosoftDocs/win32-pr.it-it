---
description: Recupera la destinazione di un collegamento simbolico.
ms.assetid: 10a6676c-96f7-4758-8868-bbccd37b5019
title: NtQuerySymbolicLinkObject (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQuerySymbolicLinkObject
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: c79b7b40e0d3c8622ee263d96836f738d76942ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326088"
---
# <a name="ntquerysymboliclinkobject-function"></a><span data-ttu-id="4fe2c-103">NtQuerySymbolicLinkObject (funzione)</span><span class="sxs-lookup"><span data-stu-id="4fe2c-103">NtQuerySymbolicLinkObject function</span></span>

<span data-ttu-id="4fe2c-104">\[Questa funzione può essere modificata o non disponibile in futuro.\]</span><span class="sxs-lookup"><span data-stu-id="4fe2c-104">\[This function may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="4fe2c-105">Recupera la destinazione di un collegamento simbolico.</span><span class="sxs-lookup"><span data-stu-id="4fe2c-105">Retrieves the target of a symbolic link.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fe2c-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4fe2c-106">Syntax</span></span>


```C++
NTSTATUS WINAPI NtQuerySymbolicLinkObject(
  _In_      HANDLE          LinkHandle,
  _Inout_   PUNICODE_STRING LinkTarget,
  _Out_opt_ PULONG          ReturnedLength
);
```



## <a name="parameters"></a><span data-ttu-id="4fe2c-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="4fe2c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fe2c-108">*LinkHandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4fe2c-108">*LinkHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fe2c-109">Handle per l'oggetto di collegamento simbolico.</span><span class="sxs-lookup"><span data-stu-id="4fe2c-109">A handle to the symbolic link object.</span></span>

</dd> <dt>

<span data-ttu-id="4fe2c-110">*LinkTarget* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="4fe2c-110">*LinkTarget* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4fe2c-111">Puntatore a una stringa Unicode inizializzata che riceve la destinazione del collegamento simbolico.</span><span class="sxs-lookup"><span data-stu-id="4fe2c-111">A pointer to an initialized Unicode string that receives the target of the symbolic link.</span></span> <span data-ttu-id="4fe2c-112">Se la chiamata ha esito negativo, è necessario impostare i membri **MaximumLength** e **buffer** .</span><span class="sxs-lookup"><span data-stu-id="4fe2c-112">The **MaximumLength** and **Buffer** members must be set if the call fails.</span></span>

</dd> <dt>

<span data-ttu-id="4fe2c-113">*ReturnedLength* \[ out, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="4fe2c-113">*ReturnedLength* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4fe2c-114">Puntatore a una variabile che riceve la lunghezza della stringa Unicode restituita nel parametro *LinkTarget* .</span><span class="sxs-lookup"><span data-stu-id="4fe2c-114">A pointer to a variable that receives the length of the Unicode string returned in the *LinkTarget* parameter.</span></span> <span data-ttu-id="4fe2c-115">Se la funzione restituisce **un \_ buffer di stato \_ troppo \_ piccolo**, questa variabile riceve le dimensioni del buffer richieste.</span><span class="sxs-lookup"><span data-stu-id="4fe2c-115">If the function returns **STATUS\_BUFFER\_TOO\_SMALL**, this variable receives the required buffer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fe2c-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4fe2c-116">Return value</span></span>

<span data-ttu-id="4fe2c-117">La funzione restituisce lo stato di **\_ esito positivo** o uno stato di errore.</span><span class="sxs-lookup"><span data-stu-id="4fe2c-117">The function returns **STATUS\_SUCCESS** or an error status.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fe2c-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="4fe2c-118">Remarks</span></span>

<span data-ttu-id="4fe2c-119">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="4fe2c-119">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fe2c-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4fe2c-120">Requirements</span></span>



| <span data-ttu-id="4fe2c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4fe2c-121">Requirement</span></span> | <span data-ttu-id="4fe2c-122">Valore</span><span class="sxs-lookup"><span data-stu-id="4fe2c-122">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4fe2c-123">DLL</span><span class="sxs-lookup"><span data-stu-id="4fe2c-123">DLL</span></span><br/> | <dl> <span data-ttu-id="4fe2c-124"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4fe2c-124"><dt>Ntdll.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fe2c-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4fe2c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fe2c-126">**NtOpenSymbolicLinkObject**</span><span class="sxs-lookup"><span data-stu-id="4fe2c-126">**NtOpenSymbolicLinkObject**</span></span>](ntopensymboliclinkobject.md)
</dt> </dl>

 

 
