---
description: Specifica l'indirizzo del nodo (NAD) da usare con l'interfaccia ISCardCmd.
ms.assetid: 49de8264-9491-41a4-a8e0-68d0db088ded
title: 'ISCardCmd: metodo:p ut_Nad (Scarddat. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_Nad
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 64ed9c502811db5666e561a1f290cc234e6c81e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879909"
---
# <a name="iscardcmdput_nad-method"></a><span data-ttu-id="cfb7c-103">ISCardCmd::p \_ Metodo UT nad</span><span class="sxs-lookup"><span data-stu-id="cfb7c-103">ISCardCmd::put\_Nad method</span></span>

<span data-ttu-id="cfb7c-104">\[Il metodo **put \_ nad** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="cfb7c-104">\[The **put\_Nad** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="cfb7c-105">Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="cfb7c-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="cfb7c-106">I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="cfb7c-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="cfb7c-107">Il metodo **put \_ nad** specifica l'indirizzo del nodo (NAD) da usare con l'interfaccia [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="cfb7c-107">The **put\_Nad** method specifies the node address (Nad) to use with the [**ISCardCmd**](iscardcmd.md) interface.</span></span> <span data-ttu-id="cfb7c-108">Questo vale per le comunicazioni usando solo le comunicazioni di [*protocollo T = 1*](../secgloss/t-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="cfb7c-108">This applies to communications using the [*T=1 protocol*](../secgloss/t-gly.md) communications only.</span></span> <span data-ttu-id="cfb7c-109">Per impostazione predefinita, l'oggetto [**ISCardCmd**](iscardcmd.md) usa un valore nad pari a zero.</span><span class="sxs-lookup"><span data-stu-id="cfb7c-109">By default, the [**ISCardCmd**](iscardcmd.md) object uses a Nad of zero.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfb7c-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cfb7c-110">Syntax</span></span>


```C++
HRESULT put_Nad(
  [in] BYTE bNad
);
```



## <a name="parameters"></a><span data-ttu-id="cfb7c-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="cfb7c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfb7c-112">*bNad* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cfb7c-112">*bNad* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfb7c-113">Byte che rappresenta il nad da usare.</span><span class="sxs-lookup"><span data-stu-id="cfb7c-113">Byte representing the Nad to use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfb7c-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cfb7c-114">Return value</span></span>

<span data-ttu-id="cfb7c-115">Il metodo restituisce uno dei valori possibili seguenti.</span><span class="sxs-lookup"><span data-stu-id="cfb7c-115">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="cfb7c-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="cfb7c-116">Return code</span></span>                                                                                  | <span data-ttu-id="cfb7c-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cfb7c-117">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="cfb7c-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cfb7c-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="cfb7c-119">Operazione completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="cfb7c-119">Operation was completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="cfb7c-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="cfb7c-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="cfb7c-121">Il parametro *bNad* non è valido.</span><span class="sxs-lookup"><span data-stu-id="cfb7c-121">The *bNad* parameter is not valid.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="cfb7c-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="cfb7c-122">Remarks</span></span>

<span data-ttu-id="cfb7c-123">Questo metodo deve essere chiamato solo quando è necessario usare un valore diverso da zero per il nad.</span><span class="sxs-lookup"><span data-stu-id="cfb7c-123">This method should be called only when it is necessary to use a value other than zero for the Nad.</span></span>

## <a name="examples"></a><span data-ttu-id="cfb7c-124">Esempio</span><span class="sxs-lookup"><span data-stu-id="cfb7c-124">Examples</span></span>

<span data-ttu-id="cfb7c-125">Nell'esempio seguente viene illustrato come specificare un indirizzo di nodo da utilizzare con l'interfaccia [**ISCardCmd**](iscardcmd.md) .</span><span class="sxs-lookup"><span data-stu-id="cfb7c-125">The following example shows how to specify a node address to use with the [**ISCardCmd**](iscardcmd.md) interface.</span></span> <span data-ttu-id="cfb7c-126">Nell'esempio si presuppone che byNadValue sia una variabile di tipo **byte** a cui è stato precedentemente assegnato un valore e che pISCardCmd è un puntatore valido a un'istanza dell'interfaccia **ISCardCmd** .</span><span class="sxs-lookup"><span data-stu-id="cfb7c-126">The example assumes that byNadValue is a variable of type **BYTE** that was previously assigned a value, and that pISCardCmd is a valid pointer to an instance of the **ISCardCmd** interface.</span></span>


```C++
HRESULT  hr;

// Set the Nad.
// byNadValue is a previously assigned BYTE value.
hr = pISCardCmd->put_Nad(byNadValue);
if (FAILED(hr))
{
  printf("Failed put_Nad\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="cfb7c-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cfb7c-127">Requirements</span></span>



| <span data-ttu-id="cfb7c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfb7c-128">Requirement</span></span> | <span data-ttu-id="cfb7c-129">Valore</span><span class="sxs-lookup"><span data-stu-id="cfb7c-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cfb7c-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cfb7c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="cfb7c-131">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="cfb7c-131">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="cfb7c-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cfb7c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="cfb7c-133">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="cfb7c-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cfb7c-134">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="cfb7c-134">End of client support</span></span><br/>    | <span data-ttu-id="cfb7c-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="cfb7c-135">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="cfb7c-136">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="cfb7c-136">End of server support</span></span><br/>    | <span data-ttu-id="cfb7c-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cfb7c-137">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="cfb7c-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cfb7c-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfb7c-139"><dt>Scarddat. h</dt></span><span class="sxs-lookup"><span data-stu-id="cfb7c-139"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="cfb7c-140">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="cfb7c-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="cfb7c-141"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="cfb7c-141"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="cfb7c-142">DLL</span><span class="sxs-lookup"><span data-stu-id="cfb7c-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cfb7c-143"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cfb7c-143"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="cfb7c-144">IID</span><span class="sxs-lookup"><span data-stu-id="cfb7c-144">IID</span></span><br/>                      | <span data-ttu-id="cfb7c-145">IID \_ ISCardCmd è definito come D5778AE3-43DE-11D0-9171-00AA00C18068</span><span class="sxs-lookup"><span data-stu-id="cfb7c-145">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="cfb7c-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cfb7c-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfb7c-147">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="cfb7c-147">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
