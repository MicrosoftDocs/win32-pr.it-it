---
description: Il \_ metodo Get LocalParticipantTypedInfo ottiene informazioni sul partecipante, ad esempio il nome della posta elettronica o la posizione geografica.
ms.assetid: 46bb70a7-7dc9-463d-8416-737122412750
title: 'Metodo ITLocalParticipant:: get_LocalParticipantTypedInfo (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: caabaf503963c09898c06659884fd3ac3858e704
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330375"
---
# <a name="itlocalparticipantget_localparticipanttypedinfo-method"></a><span data-ttu-id="819c7-103">Metodo ITLocalParticipant:: Get \_ LocalParticipantTypedInfo</span><span class="sxs-lookup"><span data-stu-id="819c7-103">ITLocalParticipant::get\_LocalParticipantTypedInfo method</span></span>

<span data-ttu-id="819c7-104">Il metodo **get \_ LocalParticipantTypedInfo** ottiene informazioni sul partecipante, ad esempio il nome della posta elettronica o la posizione geografica.</span><span class="sxs-lookup"><span data-stu-id="819c7-104">The **get\_LocalParticipantTypedInfo** method gets participant information, such as e-mail name or geographical location.</span></span>

## <a name="syntax"></a><span data-ttu-id="819c7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="819c7-105">Syntax</span></span>


```C++
HRESULT get_LocalParticipantTypedInfo(
  [in]  PARTICIPANT_TYPED_INFO InfoType,
  [out] BSTR                   *ppInfo
);
```



## <a name="parameters"></a><span data-ttu-id="819c7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="819c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="819c7-107">*InfoType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="819c7-107">*InfoType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="819c7-108">[**Partecipante \_ Identificatore di \_ informazioni tipizzato**](participant-typed-info.md) di tipo delle informazioni necessarie.</span><span class="sxs-lookup"><span data-stu-id="819c7-108">[**PARTICIPANT\_TYPED\_INFO**](participant-typed-info.md) identifier of type of information required.</span></span>

</dd> <dt>

<span data-ttu-id="819c7-109">*ppInfo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="819c7-109">*ppInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="819c7-110">Puntatore a un **BSTR** che conterrà le informazioni necessarie in seguito a una restituzione corretta del metodo.</span><span class="sxs-lookup"><span data-stu-id="819c7-110">Pointer to a **BSTR** that will contain the required information following a successful return of the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="819c7-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="819c7-111">Return value</span></span>

<span data-ttu-id="819c7-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="819c7-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="819c7-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="819c7-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="819c7-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="819c7-114">Remarks</span></span>

<span data-ttu-id="819c7-115">L'applicazione deve usare [SysFreeString](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) per liberare la memoria allocata per il parametro *ppInfo* .</span><span class="sxs-lookup"><span data-stu-id="819c7-115">The application must use [SysFreeString](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppInfo* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="819c7-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="819c7-116">Requirements</span></span>



| <span data-ttu-id="819c7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="819c7-117">Requirement</span></span> | <span data-ttu-id="819c7-118">Valore</span><span class="sxs-lookup"><span data-stu-id="819c7-118">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="819c7-119">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="819c7-119">TAPI version</span></span><br/> | <span data-ttu-id="819c7-120">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="819c7-120">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="819c7-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="819c7-121">Header</span></span><br/>       | <dl> <span data-ttu-id="819c7-122"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="819c7-122"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="819c7-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="819c7-123">Library</span></span><br/>      | <dl> <span data-ttu-id="819c7-124"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="819c7-124"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="819c7-125">DLL</span><span class="sxs-lookup"><span data-stu-id="819c7-125">DLL</span></span><br/>          | <dl> <span data-ttu-id="819c7-126"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="819c7-126"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="819c7-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="819c7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="819c7-128">**ITLocalParticipant**</span><span class="sxs-lookup"><span data-stu-id="819c7-128">**ITLocalParticipant**</span></span>](itlocalparticipant.md)
</dt> <dt>

[<span data-ttu-id="819c7-129">**\_informazioni digitate del partecipante \_**</span><span class="sxs-lookup"><span data-stu-id="819c7-129">**PARTICIPANT\_TYPED\_INFO**</span></span>](participant-typed-info.md)
</dt> </dl>

 

