---
description: "Il metodo IWiaItem2:: EnumRegisterEventInfo crea un enumeratore che è possibile usare per ottenere informazioni sugli eventi per i quali è stata registrata un'applicazione."
ms.assetid: 9c25e9ae-bd3e-46a6-b4c2-c0bbcd265d51
title: 'Metodo IWiaItem2:: EnumRegisterEventInfo (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.EnumRegisterEventInfo
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 9b5899b629267f74724129aeae3f66801953d8cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129427"
---
# <a name="iwiaitem2enumregistereventinfo-method"></a><span data-ttu-id="23cf8-103">Metodo IWiaItem2:: EnumRegisterEventInfo</span><span class="sxs-lookup"><span data-stu-id="23cf8-103">IWiaItem2::EnumRegisterEventInfo method</span></span>

<span data-ttu-id="23cf8-104">Il metodo **IWiaItem2:: EnumRegisterEventInfo** crea un enumeratore che è possibile usare per ottenere informazioni sugli eventi per i quali è stata registrata un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="23cf8-104">The **IWiaItem2::EnumRegisterEventInfo** method creates an enumerator that you can use to obtain information about events for which an application is registered.</span></span>

## <a name="syntax"></a><span data-ttu-id="23cf8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="23cf8-105">Syntax</span></span>


```C++
HRESULT EnumRegisterEventInfo(
  [in]        LONG              lFlags,
  [in]  const GUID              *pEventGUID,
  [out]       IEnumWIA_DEV_CAPS **ppIEnum
);
```



## <a name="parameters"></a><span data-ttu-id="23cf8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="23cf8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23cf8-107">*è* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="23cf8-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23cf8-108">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="23cf8-108">Type: **LONG**</span></span>

<span data-ttu-id="23cf8-109">Non usato.</span><span class="sxs-lookup"><span data-stu-id="23cf8-109">Not used.</span></span> <span data-ttu-id="23cf8-110">Impostare su 0.</span><span class="sxs-lookup"><span data-stu-id="23cf8-110">Set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="23cf8-111">*pEventGUID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="23cf8-111">*pEventGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23cf8-112">Tipo: \**const \* GUID* _</span><span class="sxs-lookup"><span data-stu-id="23cf8-112">Type: \**const GUID\** _</span></span>

<span data-ttu-id="23cf8-113">Puntatore a un identificatore che specifica l'evento hardware per il quale si desidera ottenere le informazioni di registrazione.</span><span class="sxs-lookup"><span data-stu-id="23cf8-113">Pointer to an identifier that specifies the hardware event for which you want to obtain registration information.</span></span>

</dd> <dt>

<span data-ttu-id="23cf8-114">_ppIEnum \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="23cf8-114">_ppIEnum\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="23cf8-115">Tipo: **[ **IEnumWIA \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)\*\***</span><span class="sxs-lookup"><span data-stu-id="23cf8-115">Type: **[**IEnumWIA\_DEV\_CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)\*\***</span></span>

<span data-ttu-id="23cf8-116">Indirizzo di un puntatore all'interfaccia [**IEnumWIA \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) .</span><span class="sxs-lookup"><span data-stu-id="23cf8-116">The address of a pointer to the [**IEnumWIA\_DEV\_CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23cf8-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="23cf8-117">Return value</span></span>

<span data-ttu-id="23cf8-118">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="23cf8-118">Type: **HRESULT**</span></span>

<span data-ttu-id="23cf8-119">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="23cf8-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="23cf8-120">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="23cf8-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="23cf8-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="23cf8-121">Remarks</span></span>

<span data-ttu-id="23cf8-122">Un'applicazione chiama questo metodo per creare un oggetto enumeratore per le informazioni sull'evento.</span><span class="sxs-lookup"><span data-stu-id="23cf8-122">An application calls this method to create an enumerator object for the event information.</span></span> <span data-ttu-id="23cf8-123">**IWiaItem2:: EnumRegisterEventInfo** archivia l'indirizzo dell'interfaccia [**IEnumWIA \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) dell'oggetto enumeratore nel parametro *ppIEnum* .</span><span class="sxs-lookup"><span data-stu-id="23cf8-123">**IWiaItem2::EnumRegisterEventInfo** stores the address of the [**IEnumWIA\_DEV\_CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) interface of the enumerator object in the *ppIEnum* parameter.</span></span> <span data-ttu-id="23cf8-124">Il programma usa quindi il puntatore di interfaccia per enumerare le proprietà dell'evento per cui è registrato.</span><span class="sxs-lookup"><span data-stu-id="23cf8-124">The program then uses the interface pointer to enumerate the properties of the event for which it is registered.</span></span>

<span data-ttu-id="23cf8-125">Le applicazioni devono chiamare il metodo [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sui puntatori di interfaccia ricevuti tramite il parametro *ppIEnum* .</span><span class="sxs-lookup"><span data-stu-id="23cf8-125">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers that they receive through the *ppIEnum* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="23cf8-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="23cf8-126">Requirements</span></span>



| <span data-ttu-id="23cf8-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="23cf8-127">Requirement</span></span> | <span data-ttu-id="23cf8-128">Valore</span><span class="sxs-lookup"><span data-stu-id="23cf8-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="23cf8-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="23cf8-129">Minimum supported client</span></span><br/> | <span data-ttu-id="23cf8-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="23cf8-130">Windows Vista \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="23cf8-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="23cf8-131">Minimum supported server</span></span><br/> | <span data-ttu-id="23cf8-132">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="23cf8-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="23cf8-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="23cf8-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="23cf8-134"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="23cf8-134"><dt>Wia.h</dt></span></span> </dl> |



 

 
