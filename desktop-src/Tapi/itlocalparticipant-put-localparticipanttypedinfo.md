---
description: Il \_ metodo Put LocalParticipantTypedInfo imposta le informazioni sul partecipante.
ms.assetid: c4afd1d3-6fe4-4e5b-a9bf-81b7dffa9914
title: 'ITLocalParticipant: metodo:p ut_LocalParticipantTypedInfo (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77809a9a3858b6a098fa3ff6a93878cf38518f92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330372"
---
# <a name="itlocalparticipantput_localparticipanttypedinfo-method"></a><span data-ttu-id="7dcfa-103">ITLocalParticipant::p UT \_ LocalParticipantTypedInfo metodo</span><span class="sxs-lookup"><span data-stu-id="7dcfa-103">ITLocalParticipant::put\_LocalParticipantTypedInfo method</span></span>

<span data-ttu-id="7dcfa-104">Il metodo **put \_ LocalParticipantTypedInfo** imposta le informazioni sul partecipante.</span><span class="sxs-lookup"><span data-stu-id="7dcfa-104">The **put\_LocalParticipantTypedInfo** method sets participant information.</span></span>

## <a name="syntax"></a><span data-ttu-id="7dcfa-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7dcfa-105">Syntax</span></span>


```C++
HRESULT put_LocalParticipantTypedInfo(
  [in] PARTICIPANT_TYPED_INFO InfoType,
  [in] BSTR                   ppInfo
);
```



## <a name="parameters"></a><span data-ttu-id="7dcfa-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7dcfa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7dcfa-107">*InfoType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7dcfa-107">*InfoType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7dcfa-108">[**Partecipante \_ Identificatore \_ info tipizzato**](participant-typed-info.md) del tipo di informazioni richieste.</span><span class="sxs-lookup"><span data-stu-id="7dcfa-108">[**PARTICIPANT\_TYPED\_INFO**](participant-typed-info.md) identifier of the type of information required.</span></span>

</dd> <dt>

<span data-ttu-id="7dcfa-109">*ppInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7dcfa-109">*ppInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7dcfa-110">**BSTR** che contiene il nuovo valore necessario per le informazioni.</span><span class="sxs-lookup"><span data-stu-id="7dcfa-110">**BSTR** containing the required new value for the information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7dcfa-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7dcfa-111">Return value</span></span>

<span data-ttu-id="7dcfa-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7dcfa-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7dcfa-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7dcfa-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7dcfa-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="7dcfa-114">Remarks</span></span>

<span data-ttu-id="7dcfa-115">L'applicazione deve usare [SysAllocString](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) per allocare memoria per il parametro *PpInfo* e usare [SysFreeString](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria quando la variabile non è più necessaria.</span><span class="sxs-lookup"><span data-stu-id="7dcfa-115">The application must use [SysAllocString](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *ppInfo* parameter and use [SysFreeString](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="7dcfa-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7dcfa-116">Requirements</span></span>



| <span data-ttu-id="7dcfa-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7dcfa-117">Requirement</span></span> | <span data-ttu-id="7dcfa-118">Valore</span><span class="sxs-lookup"><span data-stu-id="7dcfa-118">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7dcfa-119">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="7dcfa-119">TAPI version</span></span><br/> | <span data-ttu-id="7dcfa-120">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="7dcfa-120">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="7dcfa-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7dcfa-121">Header</span></span><br/>       | <dl> <span data-ttu-id="7dcfa-122"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="7dcfa-122"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="7dcfa-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="7dcfa-123">Library</span></span><br/>      | <dl> <span data-ttu-id="7dcfa-124"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7dcfa-124"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="7dcfa-125">DLL</span><span class="sxs-lookup"><span data-stu-id="7dcfa-125">DLL</span></span><br/>          | <dl> <span data-ttu-id="7dcfa-126"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7dcfa-126"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="7dcfa-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7dcfa-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dcfa-128">**ITLocalParticipant**</span><span class="sxs-lookup"><span data-stu-id="7dcfa-128">**ITLocalParticipant**</span></span>](itlocalparticipant.md)
</dt> <dt>

[<span data-ttu-id="7dcfa-129">**\_informazioni digitate del partecipante \_**</span><span class="sxs-lookup"><span data-stu-id="7dcfa-129">**PARTICIPANT\_TYPED\_INFO**</span></span>](participant-typed-info.md)
</dt> </dl>

 

