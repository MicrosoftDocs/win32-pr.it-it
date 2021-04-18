---
description: La funzione InetGetAutodial restituisce le impostazioni di Autodial dal registro di sistema.
ms.assetid: e36761da-c050-4844-ad94-efdc77702f6f
title: InetGetAutodial (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InetGetAutodial
api_type:
- DllExport
api_location:
- Inetcfg.dll
ms.openlocfilehash: 15267cd00940f0386c8a5d9c0c54b070f2cff509
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331192"
---
# <a name="inetgetautodial-function"></a><span data-ttu-id="47479-103">InetGetAutodial (funzione)</span><span class="sxs-lookup"><span data-stu-id="47479-103">InetGetAutodial function</span></span>

<span data-ttu-id="47479-104">\[Questa funzione non è supportata e può essere modificata o non disponibile nelle versioni future di Windows.</span><span class="sxs-lookup"><span data-stu-id="47479-104">\[This function is unsupported and may be altered or unavailable in future versions of Windows.</span></span> <span data-ttu-id="47479-105">\]</span><span class="sxs-lookup"><span data-stu-id="47479-105">\]</span></span>

<span data-ttu-id="47479-106">La funzione **InetGetAutodial** restituisce le impostazioni di Autodial dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="47479-106">The **InetGetAutodial** function returns the autodial settings from the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="47479-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="47479-107">Syntax</span></span>


```C++
HRESULT InetGetAutodial(
  _Out_ LPBOOL lpfEnable,
  _Out_ LPSTR  lpszEntryName,
  _In_  DWORD  cbEntryNameSize
);
```



## <a name="parameters"></a><span data-ttu-id="47479-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="47479-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47479-109">*lpfEnable* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="47479-109">*lpfEnable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="47479-110">Indica se la connessione automatica è abilitata.</span><span class="sxs-lookup"><span data-stu-id="47479-110">Indicates whether autodial is enabled.</span></span> <span data-ttu-id="47479-111">Il valore **true** al ritorno indica che la connessione automatica è abilitata.</span><span class="sxs-lookup"><span data-stu-id="47479-111">A value of **TRUE** upon return indicates autodial is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="47479-112">*lpszEntryName* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="47479-112">*lpszEntryName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="47479-113">Nell'output restituito è contenuto il nome della voce della rubrica impostata per la selezione automatica.</span><span class="sxs-lookup"><span data-stu-id="47479-113">On return, contains the name of the phone book entry that is set for autodial.</span></span>

</dd> <dt>

<span data-ttu-id="47479-114">*cbEntryNameSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="47479-114">*cbEntryNameSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47479-115">Dimensione del buffer allocato dal chiamante per il nome della voce della rubrica telefonica.</span><span class="sxs-lookup"><span data-stu-id="47479-115">Size of the buffer allocated by the caller for the phone book entry name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47479-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="47479-116">Return value</span></span>

<span data-ttu-id="47479-117">Questa funzione può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="47479-117">This function can return one of these values.</span></span>



| <span data-ttu-id="47479-118">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="47479-118">Return code</span></span>                                                                                                | <span data-ttu-id="47479-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="47479-119">Description</span></span>                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="47479-120"><dt>**ERRORE \_ riuscito**</dt></span><span class="sxs-lookup"><span data-stu-id="47479-120"><dt>**ERROR\_SUCCESS**</dt></span></span> </dl>              | <span data-ttu-id="47479-121">La chiamata è stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="47479-121">The call was successful.</span></span><br/>                                                                                                                       |
| <dl> <span data-ttu-id="47479-122"><dt>**ERRORI \_ argomenti non validi \_**</dt></span><span class="sxs-lookup"><span data-stu-id="47479-122"><dt>**ERROR\_BAD\_ARGUMENTS**</dt></span></span> </dl>       | <span data-ttu-id="47479-123">*lpfEnable* o *lpszEntryName* contiene un puntatore **null** oppure il valore di *cbEntryNameSize* è zero.</span><span class="sxs-lookup"><span data-stu-id="47479-123">*lpfEnable* or *lpszEntryName* contains a **NULL** pointer, or the value of *cbEntryNameSize* is zero.</span></span><br/>                                         |
| <dl> <span data-ttu-id="47479-124"><dt>**ERRORE \_ di \_ memoria insufficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="47479-124"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl>  | <span data-ttu-id="47479-125">Memoria insufficiente per l'allocazione di buffer interni.</span><span class="sxs-lookup"><span data-stu-id="47479-125">There was insufficient memory to allocate internal buffers.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="47479-126"><dt>**ERRORE \_ buffer insufficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="47479-126"><dt>**ERROR\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl> | <span data-ttu-id="47479-127">*cbEntryNameSize* non indica che il buffer a cui punta *lpszEntryName* è sufficientemente grande da ricevere il nome della voce della rubrica telefonica.</span><span class="sxs-lookup"><span data-stu-id="47479-127">*cbEntryNameSize* does not indicate that the buffer pointed to by *lpszEntryName* is large enough to receive the name of the phone book entry.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="47479-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="47479-128">Remarks</span></span>

<span data-ttu-id="47479-129">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="47479-129">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="47479-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="47479-130">Requirements</span></span>



| <span data-ttu-id="47479-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="47479-131">Requirement</span></span> | <span data-ttu-id="47479-132">Valore</span><span class="sxs-lookup"><span data-stu-id="47479-132">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="47479-133">DLL</span><span class="sxs-lookup"><span data-stu-id="47479-133">DLL</span></span><br/> | <dl> <span data-ttu-id="47479-134"><dt>Inetcfg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47479-134"><dt>Inetcfg.dll</dt></span></span> </dl> |



 

 
