---
title: Metodo GetObjectDataOnClearChannel
description: Il metodo GetObjectDataOnClearChannel trasferisce di nuovo un blocco di dati oggetto su un canale non crittografato a Windows Media Gestione dispositivi.
ms.assetid: 62122415-b45b-436e-8c5f-28be759ba8c0
keywords:
- Metodo GetObjectDataOnClearChannel Windows Media Gestione dispositivi
topic_type:
- apiref
api_name:
- GetObjectDataOnClearChannel
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25b72df0dd27289153a97221fefbcb58f3a5ad13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324123"
---
# <a name="getobjectdataonclearchannel-method"></a><span data-ttu-id="603aa-104">Metodo GetObjectDataOnClearChannel</span><span class="sxs-lookup"><span data-stu-id="603aa-104">GetObjectDataOnClearChannel method</span></span>

<span data-ttu-id="603aa-105">Il metodo **GetObjectDataOnClearChannel** trasferisce di nuovo un blocco di dati oggetto su un canale non crittografato a Windows Media Gestione dispositivi.</span><span class="sxs-lookup"><span data-stu-id="603aa-105">The **GetObjectDataOnClearChannel** method transfers a block of object data on a clear channel back to Windows Media Device Manager.</span></span>

<span data-ttu-id="603aa-106">Questo metodo è identico a [**ISCPSecureExchange:: objectdata**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) , ad eccezione del fatto che i dati restituiti da questo metodo non sono crittografati.</span><span class="sxs-lookup"><span data-stu-id="603aa-106">This method is identical to [**ISCPSecureExchange::ObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) except that the data returned by this method is not encrypted.</span></span> <span data-ttu-id="603aa-107">Di conseguenza, questo metodo è più efficiente.</span><span class="sxs-lookup"><span data-stu-id="603aa-107">Consequently this method is more efficient.</span></span>

## <a name="syntax"></a><span data-ttu-id="603aa-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="603aa-108">Syntax</span></span>


```C++
HRESULT GetObjectDataOnClearChannel(
   IMDSPDevice *pDevice,
   BYTE        *pData,
   DWORD       *pdwSize
);
```



## <a name="parameters"></a><span data-ttu-id="603aa-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="603aa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="603aa-110">*pDevice*</span><span class="sxs-lookup"><span data-stu-id="603aa-110">*pDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="603aa-111">Puntatore all'oggetto dispositivo.</span><span class="sxs-lookup"><span data-stu-id="603aa-111">Pointer to the device object.</span></span>

</dd> <dt>

<span data-ttu-id="603aa-112">*pData*</span><span class="sxs-lookup"><span data-stu-id="603aa-112">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="603aa-113">Puntatore a un buffer per la ricezione dei dati.</span><span class="sxs-lookup"><span data-stu-id="603aa-113">Pointer to a buffer to receive data.</span></span>

</dd> <dt>

<span data-ttu-id="603aa-114">*pdwSize*</span><span class="sxs-lookup"><span data-stu-id="603aa-114">*pdwSize*</span></span> 
</dt> <dd>

<span data-ttu-id="603aa-115">Puntatore a un **valore DWORD** che contiene la dimensione di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="603aa-115">Pointer to a **DWORD** containing the transfer size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="603aa-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="603aa-116">Return value</span></span>

<span data-ttu-id="603aa-117">Se il metodo ha esito positivo, restituisce S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="603aa-117">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="603aa-118">Se il metodo ha esito negativo, viene restituito un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="603aa-118">If the method fails, it returns an **HRESULT** error code.</span></span>



| <span data-ttu-id="603aa-119">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="603aa-119">Return code</span></span>                                                                                                | <span data-ttu-id="603aa-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="603aa-120">Description</span></span>                                                                                 |
|------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="603aa-121"><dt>**Verifica di WMDM \_ E \_ Mac \_ \_ non riuscita**</dt></span><span class="sxs-lookup"><span data-stu-id="603aa-121"><dt>**WMDM\_E\_MAC\_CHECK\_FAILED**</dt></span></span> </dl> | <span data-ttu-id="603aa-122">Il codice di autenticazione del messaggio non è valido.</span><span class="sxs-lookup"><span data-stu-id="603aa-122">The message authentication code is not valid.</span></span><br/>                                    |
| <dl> <span data-ttu-id="603aa-123"><dt>**WMDM \_ E \_ norights**</dt></span><span class="sxs-lookup"><span data-stu-id="603aa-123"><dt>**WMDM\_E\_NORIGHTS**</dt></span></span> </dl>           | <span data-ttu-id="603aa-124">Il chiamante non dispone dei diritti necessari per eseguire l'operazione richiesta.</span><span class="sxs-lookup"><span data-stu-id="603aa-124">The caller does not have the rights required to perform the requested operation.</span></span><br/> |
| <dl> <span data-ttu-id="603aa-125"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="603aa-125"><dt>**S\_FALSE**</dt></span></span> </dl>                    | <span data-ttu-id="603aa-126">Il metodo non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="603aa-126">The method failed.</span></span> <span data-ttu-id="603aa-127">Termina l'interazione con il provider di contenuti.</span><span class="sxs-lookup"><span data-stu-id="603aa-127">Terminate interaction with the content provider.</span></span><br/>              |
| <dl> <span data-ttu-id="603aa-128"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="603aa-128"><dt>**E\_INVALIDARG**</dt></span></span> </dl>               | <span data-ttu-id="603aa-129">Un parametro è un puntatore **null** o non valido.</span><span class="sxs-lookup"><span data-stu-id="603aa-129">A parameter is an invalid or **NULL** pointer.</span></span><br/>                                   |
| <dl> <span data-ttu-id="603aa-130"><dt>**E \_ non riescono**</dt></span><span class="sxs-lookup"><span data-stu-id="603aa-130"><dt>**E\_FAIL**</dt></span></span> </dl>                     | <span data-ttu-id="603aa-131">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="603aa-131">An unspecified error occurred.</span></span><br/>                                                   |



 

## <a name="remarks"></a><span data-ttu-id="603aa-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="603aa-132">Remarks</span></span>

<span data-ttu-id="603aa-133">Per trasferire dati, Windows Media Gestione dispositivi chiama il metodo [TransferContainerDataOnClearChannel](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange3-transfercontainerdataonclearchannel) per ottenere i dati del contenitore.</span><span class="sxs-lookup"><span data-stu-id="603aa-133">To transfer data, Windows Media Device Manager calls the [TransferContainerDataOnClearChannel](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange3-transfercontainerdataonclearchannel) method to obtain the container data.</span></span> <span data-ttu-id="603aa-134">**GetObjectDataOnClearChannel** viene quindi chiamato per trasferire i blocchi di dati oggetto dal provider di contenuti a Windows Media Gestione dispositivi.</span><span class="sxs-lookup"><span data-stu-id="603aa-134">**GetObjectDataOnClearChannel** is then called to transfer blocks of object data from the content provider to Windows Media Device Manager.</span></span> <span data-ttu-id="603aa-135">Se \_ viene restituito S OK con *pdwSize* impostato su zero, Windows Media Gestione dispositivi non richiederà altri dati.</span><span class="sxs-lookup"><span data-stu-id="603aa-135">If S\_OK is returned with *pdwSize* set to zero, Windows Media Device Manager will request no further data.</span></span>

<span data-ttu-id="603aa-136">Questo metodo è identico a [**ISCPSecureExchange:: objectdata**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) , ad eccezione del fatto che i dati restituiti da questo metodo non sono crittografati.</span><span class="sxs-lookup"><span data-stu-id="603aa-136">This method is identical to [**ISCPSecureExchange::ObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata) except that the data returned by this method is not encrypted.</span></span> <span data-ttu-id="603aa-137">Di conseguenza, questo metodo è più efficiente.</span><span class="sxs-lookup"><span data-stu-id="603aa-137">Consequently this method is more efficient.</span></span>

## <a name="requirements"></a><span data-ttu-id="603aa-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="603aa-138">Requirements</span></span>



| <span data-ttu-id="603aa-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="603aa-139">Requirement</span></span> | <span data-ttu-id="603aa-140">Valore</span><span class="sxs-lookup"><span data-stu-id="603aa-140">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="603aa-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="603aa-141">Header</span></span><br/>  | <dl> <span data-ttu-id="603aa-142"><dt>WMSCP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="603aa-142"><dt>WMSCP.idl</dt></span></span> </dl>    |
| <span data-ttu-id="603aa-143">Libreria</span><span class="sxs-lookup"><span data-stu-id="603aa-143">Library</span></span><br/> | <dl> <span data-ttu-id="603aa-144"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="603aa-144"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="603aa-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="603aa-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="603aa-146">**ISCPSecureExchange:: ObjectData**</span><span class="sxs-lookup"><span data-stu-id="603aa-146">**ISCPSecureExchange::ObjectData**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange-objectdata)
</dt> <dt>

[<span data-ttu-id="603aa-147">**Interfaccia ISCPSecureExchange3**</span><span class="sxs-lookup"><span data-stu-id="603aa-147">**ISCPSecureExchange3 Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange3)
</dt> </dl>

 

 





