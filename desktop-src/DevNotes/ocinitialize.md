---
description: Inizializza il gestore di componenti facoltativo.
ms.assetid: 9a7ddca6-a6c8-4d96-81bb-66158b83ab68
title: OcInitialize (funzione)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OcInitialize
api_type:
- DllExport
api_location:
- OcManage.dll
ms.openlocfilehash: aad102ac9881a801f693a429aab5dae07d09b5e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326087"
---
# <a name="ocinitialize-function"></a><span data-ttu-id="4d827-103">OcInitialize (funzione)</span><span class="sxs-lookup"><span data-stu-id="4d827-103">OcInitialize function</span></span>

<span data-ttu-id="4d827-104">Inizializza il gestore di componenti facoltativo.</span><span class="sxs-lookup"><span data-stu-id="4d827-104">Initializes the optional component manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d827-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4d827-105">Syntax</span></span>


```C++
PVOID OcInitialize(
  _In_  POCM_CLIENT_CALLBACKS Callbacks,
  _In_  LPCTSTR               MasterOcInfName,
  _In_  UINT                  Flags,
  _Out_ PBOOL                 ShowError,
  _In_  PVOID                 Log
);
```



## <a name="parameters"></a><span data-ttu-id="4d827-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4d827-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d827-107">*Callback di* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4d827-107">*Callbacks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d827-108">Puntatore a una struttura [**di \_ \_ callback del client OCM**](ocm-client-callbacks.md) che specifica le funzioni di callback che devono essere utilizzate dal gestore OC per eseguire varie attività.</span><span class="sxs-lookup"><span data-stu-id="4d827-108">A pointer to an [**OCM\_CLIENT\_CALLBACKS**](ocm-client-callbacks.md) structure that specifies the callback functions to be used by the OC manager to perform various tasks.</span></span>

</dd> <dt>

<span data-ttu-id="4d827-109">*MasterOcInfName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4d827-109">*MasterOcInfName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d827-110">Percorso del file master OC. inf.</span><span class="sxs-lookup"><span data-stu-id="4d827-110">The path of the master OC .inf file.</span></span>

</dd> <dt>

<span data-ttu-id="4d827-111">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4d827-111">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d827-112">Il parametro può essere costituito da uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="4d827-112">This parameter can be one or more of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="4d827-113"><span id="OCINIT_FORCENEWINF"></span><span id="ocinit_forcenewinf"></span>**OCINIT \_ FORCENEWINF** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="4d827-113"><span id="OCINIT_FORCENEWINF"></span><span id="ocinit_forcenewinf"></span>**OCINIT\_FORCENEWINF** (0x00000001)</span></span>
</dt> <dt>

<span data-ttu-id="4d827-114"><span id="OCINIT_KILLSUBCOMPS"></span><span id="ocinit_killsubcomps"></span>**OCINIT \_ KILLSUBCOMPS** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="4d827-114"><span id="OCINIT_KILLSUBCOMPS"></span><span id="ocinit_killsubcomps"></span>**OCINIT\_KILLSUBCOMPS** (0x00000002)</span></span>
</dt> <dt>

<span data-ttu-id="4d827-115"><span id="OCINIT_RUNQUIET"></span><span id="ocinit_runquiet"></span>**OCINIT \_ RUNQUIET** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="4d827-115"><span id="OCINIT_RUNQUIET"></span><span id="ocinit_runquiet"></span>**OCINIT\_RUNQUIET** (0x00000004)</span></span>
</dt> <dt>

<span data-ttu-id="4d827-116"><span id="OCINIT_LANGUAGEAWARE"></span><span id="ocinit_languageaware"></span>**OCINIT \_ LANGUAGEAWARE** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="4d827-116"><span id="OCINIT_LANGUAGEAWARE"></span><span id="ocinit_languageaware"></span>**OCINIT\_LANGUAGEAWARE** (0x00000008)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="4d827-117">*ShowError* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4d827-117">*ShowError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4d827-118">Se la funzione ha esito negativo, questo parametro indica se visualizzare o meno un messaggio di errore.</span><span class="sxs-lookup"><span data-stu-id="4d827-118">If the function fails, this parameter indicates whether to display an error message.</span></span>

</dd> <dt>

<span data-ttu-id="4d827-119">*Log* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="4d827-119">*Log* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d827-120">Handle per il log.</span><span class="sxs-lookup"><span data-stu-id="4d827-120">A handle to the log.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d827-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4d827-121">Return value</span></span>

<span data-ttu-id="4d827-122">La funzione restituisce il valore di contesto di gestione OC.</span><span class="sxs-lookup"><span data-stu-id="4d827-122">The function returns the OC manager context value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d827-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="4d827-123">Remarks</span></span>

<span data-ttu-id="4d827-124">A questa funzione non è associato alcun file di intestazione o libreria di importazione. è necessario chiamarla usando le funzioni [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="4d827-124">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d827-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4d827-125">Requirements</span></span>



| <span data-ttu-id="4d827-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d827-126">Requirement</span></span> | <span data-ttu-id="4d827-127">Valore</span><span class="sxs-lookup"><span data-stu-id="4d827-127">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d827-128">DLL</span><span class="sxs-lookup"><span data-stu-id="4d827-128">DLL</span></span><br/> | <dl> <span data-ttu-id="4d827-129"><dt>OcManage.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d827-129"><dt>OcManage.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d827-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4d827-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d827-131">**\_callback client \_ OCM**</span><span class="sxs-lookup"><span data-stu-id="4d827-131">**OCM\_CLIENT\_CALLBACKS**</span></span>](ocm-client-callbacks.md)
</dt> <dt>

[<span data-ttu-id="4d827-132">**OcTerminate**</span><span class="sxs-lookup"><span data-stu-id="4d827-132">**OcTerminate**</span></span>](octerminate.md)
</dt> </dl>

 

 
