---
title: Metodo GetIcon INapComponentInfo (NapCommon. h)
description: Viene utilizzato dal sistema NAP per ottenere l'icona di un client di integrità.
ms.assetid: 6501fe12-1ec0-43a1-b672-b6cfd9a08d85
keywords:
- Metodo GetIcon (NAP)
- Metodo GetIcon, NAP, interfaccia INapComponentInfo
- Interfaccia INapComponentInfo NAP, Metodo GetIcon
topic_type:
- apiref
api_name:
- INapComponentInfo.GetIcon
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 795ad85f8497262f88fa55d8efb2da7466b8c3a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964835"
---
# <a name="inapcomponentinfogeticon-method"></a><span data-ttu-id="6fcf7-106">Metodo INapComponentInfo:: GetIcon</span><span class="sxs-lookup"><span data-stu-id="6fcf7-106">INapComponentInfo::GetIcon method</span></span>

> [!Note]  
> <span data-ttu-id="6fcf7-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="6fcf7-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="6fcf7-108">Il metodo di callback **INapComponentInfo:: GetIcon** viene utilizzato dal sistema NAP per ottenere l'icona di un client di integrità.</span><span class="sxs-lookup"><span data-stu-id="6fcf7-108">The **INapComponentInfo::GetIcon** callback method is used by the NAP System to get the icon of a health client.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fcf7-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6fcf7-109">Syntax</span></span>


```C++
HRESULT GetIcon(
  [out] CountedString **dllFilePath,
  [out] UINT32        *iconResourceId
);
```



## <a name="parameters"></a><span data-ttu-id="6fcf7-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="6fcf7-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6fcf7-111">*dllFilePath* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6fcf7-111">*dllFilePath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6fcf7-112">Puntatore a un puntatore a un [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) utilizzato per restituire il percorso del file dll che contiene l'icona.</span><span class="sxs-lookup"><span data-stu-id="6fcf7-112">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) used to return the file path of the DLL that contains the icon.</span></span>

</dd> <dt>

<span data-ttu-id="6fcf7-113">*iconResourceId* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6fcf7-113">*iconResourceId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6fcf7-114">Puntatore al valore usato per restituire l'ID risorsa dell'icona da usare.</span><span class="sxs-lookup"><span data-stu-id="6fcf7-114">A pointer to value used to return the resource ID of the icon to be used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6fcf7-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6fcf7-115">Return value</span></span>

<span data-ttu-id="6fcf7-116">Restituisce uno di questi codici di errore in base al risultato di questa operazione.</span><span class="sxs-lookup"><span data-stu-id="6fcf7-116">Return one of these error codes based on the result of this operation.</span></span>



| <span data-ttu-id="6fcf7-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="6fcf7-117">Return code</span></span>                                                                                     | <span data-ttu-id="6fcf7-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6fcf7-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="6fcf7-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6fcf7-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="6fcf7-120">L'operazione è riuscita.</span><span class="sxs-lookup"><span data-stu-id="6fcf7-120">The operation is successful.</span></span><br/>                            |
| <dl> <span data-ttu-id="6fcf7-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="6fcf7-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="6fcf7-122">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="6fcf7-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="6fcf7-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="6fcf7-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="6fcf7-124">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="6fcf7-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6fcf7-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="6fcf7-125">Remarks</span></span>

<span data-ttu-id="6fcf7-126">Le icone devono essere localizzate in base all'ID lingua del thread chiamante.</span><span class="sxs-lookup"><span data-stu-id="6fcf7-126">Icons should be localized according to the calling thread's language-id.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fcf7-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6fcf7-127">Requirements</span></span>



| <span data-ttu-id="6fcf7-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fcf7-128">Requirement</span></span> | <span data-ttu-id="6fcf7-129">Valore</span><span class="sxs-lookup"><span data-stu-id="6fcf7-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fcf7-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6fcf7-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6fcf7-131">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6fcf7-131">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6fcf7-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6fcf7-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6fcf7-133">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6fcf7-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6fcf7-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6fcf7-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fcf7-135"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fcf7-135"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="6fcf7-136">IDL</span><span class="sxs-lookup"><span data-stu-id="6fcf7-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6fcf7-137"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6fcf7-137"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fcf7-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6fcf7-138">See also</span></span>

<dl> <span data-ttu-id="6fcf7-139"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="6fcf7-139"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="6fcf7-140">**INapComponentInfo**</span><span class="sxs-lookup"><span data-stu-id="6fcf7-140">**INapComponentInfo**</span></span>](inapcomponentinfo.md)
</dt> </dl>

 

 





