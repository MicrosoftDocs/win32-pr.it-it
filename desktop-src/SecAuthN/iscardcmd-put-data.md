---
description: Imposta il campo dati nell'unità dati del protocollo dell'applicazione (APDU).
ms.assetid: 4508e00c-2b1d-4be5-b3a7-083b367a2158
title: 'ISCardCmd: metodo:p ut_Data (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_Data
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 58c1fa7d709eff1ed0618f52a83825f5110c4457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130259"
---
# <a name="iscardcmdput_data-method"></a><span data-ttu-id="f9072-103">ISCardCmd: \_ metodo dati ut:p</span><span class="sxs-lookup"><span data-stu-id="f9072-103">ISCardCmd::put\_Data method</span></span>

<span data-ttu-id="f9072-104">\[Il metodo **put \_ Data** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="f9072-104">\[The **put\_Data** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="f9072-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f9072-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f9072-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="f9072-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="f9072-107">Il metodo **put \_ Data** imposta il campo dati nell' [*unità dati del protocollo dell'applicazione*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="f9072-107">The **put\_Data** method sets the data field in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="f9072-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f9072-108">Syntax</span></span>


```C++
HRESULT put_Data(
  [in] LPBYTEBUFFER pData
);
```



## <a name="parameters"></a><span data-ttu-id="f9072-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f9072-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9072-110">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f9072-110">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9072-111">Puntatore all'oggetto di buffer di byte (**IStream**) da copiare nel campo dati APDU.</span><span class="sxs-lookup"><span data-stu-id="f9072-111">Pointer to the byte buffer object (**IStream**) to be copied into the APDU data field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9072-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f9072-112">Return value</span></span>

<span data-ttu-id="f9072-113">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="f9072-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="f9072-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f9072-114">Return code</span></span>                                                                                   | <span data-ttu-id="f9072-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f9072-115">Description</span></span>                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="f9072-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f9072-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f9072-117">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="f9072-117">Operation completed successfully.</span></span><br/>    |
| <dl> <span data-ttu-id="f9072-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f9072-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="f9072-119">Il parametro *pData* non è valido.</span><span class="sxs-lookup"><span data-stu-id="f9072-119">The *pData* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="f9072-120"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="f9072-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="f9072-121">Un puntatore errato è stato passato in *pData*.</span><span class="sxs-lookup"><span data-stu-id="f9072-121">A bad pointer was passed in *pData*.</span></span><br/> |
| <dl> <span data-ttu-id="f9072-122"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="f9072-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f9072-123">Memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="f9072-123">Out of memory.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="f9072-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="f9072-124">Remarks</span></span>

<span data-ttu-id="f9072-125">Quando si imposta una nuova parte di dati del messaggio, la lunghezza del campo dati viene calcolata e archiviata nel parametro P3 del APDU.</span><span class="sxs-lookup"><span data-stu-id="f9072-125">When you set a new data portion of the message, the length of the data field is calculated and stored in the P3 parameter of the APDU.</span></span> <span data-ttu-id="f9072-126">Per recuperare la lunghezza del campo dati, chiamare [**get \_ P3**](iscardcmd-get-p3.md).</span><span class="sxs-lookup"><span data-stu-id="f9072-126">To retrieve the length of the data field, call [**get\_P3**](iscardcmd-get-p3.md).</span></span>

<span data-ttu-id="f9072-127">Per recuperare il campo dati da APDU, chiamare [**get \_ Data**](iscardcmd-get-data.md).</span><span class="sxs-lookup"><span data-stu-id="f9072-127">To retrieve the data field from the APDU, call [**get\_Data**](iscardcmd-get-data.md).</span></span>

## <a name="examples"></a><span data-ttu-id="f9072-128">Esempio</span><span class="sxs-lookup"><span data-stu-id="f9072-128">Examples</span></span>

<span data-ttu-id="f9072-129">Nell'esempio seguente viene illustrato come impostare il campo dati nell' [*unità dati del protocollo dell'applicazione*](../secgloss/a-gly.md) (APDU).</span><span class="sxs-lookup"><span data-stu-id="f9072-129">The following example shows how to set the data field in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="f9072-130">Nell'esempio si presuppone che pIByteData sia un puntatore valido a un'istanza dell'interfaccia [**IByteBuffer**](ibytebuffer.md) e che pISCardCmd sia un puntatore valido a un'istanza dell'interfaccia [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="f9072-130">The example assumes that pIByteData is a valid pointer to an instance of the [**IByteBuffer**](ibytebuffer.md) interface, and that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT    hr;

// pIByteData is a pointer to an instance of IByteBuffer.
// Set the data.
hr = pISCardCmd->put_Data(pIByteData);
if (FAILED(hr)) 
{
    printf("Failed put_Data.\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="f9072-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f9072-131">Requirements</span></span>



| <span data-ttu-id="f9072-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9072-132">Requirement</span></span> | <span data-ttu-id="f9072-133">Valore</span><span class="sxs-lookup"><span data-stu-id="f9072-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9072-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9072-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f9072-135">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f9072-135">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f9072-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f9072-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f9072-137">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f9072-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f9072-138">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="f9072-138">End of client support</span></span><br/>    | <span data-ttu-id="f9072-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="f9072-139">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="f9072-140">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="f9072-140">End of server support</span></span><br/>    | <span data-ttu-id="f9072-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f9072-141">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="f9072-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f9072-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9072-143"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9072-143"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="f9072-144">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="f9072-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="f9072-145"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f9072-145"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f9072-146">DLL</span><span class="sxs-lookup"><span data-stu-id="f9072-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9072-147"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9072-147"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f9072-148">IID</span><span class="sxs-lookup"><span data-stu-id="f9072-148">IID</span></span><br/>                      | <span data-ttu-id="f9072-149">IID \_ ISCardCmd è definito come D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="f9072-149">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="f9072-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f9072-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9072-151">**recuperare \_ i dati**</span><span class="sxs-lookup"><span data-stu-id="f9072-151">**get\_Data**</span></span>](iscardcmd-get-data.md)
</dt> <dt>

[<span data-ttu-id="f9072-152">**ottenere \_ P3**</span><span class="sxs-lookup"><span data-stu-id="f9072-152">**get\_P3**</span></span>](iscardcmd-get-p3.md)
</dt> <dt>

[<span data-ttu-id="f9072-153">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="f9072-153">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
