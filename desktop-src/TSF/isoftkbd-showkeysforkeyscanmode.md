---
title: Metodo ISoftKbd ShowKeysForKeyScanMode (Softkbdc. h)
description: Il metodo ISoftKbd ShowKeysForKeyScanMode Visualizza le chiavi usate per la modalità di analisi della chiave per una tastiera soft.
ms.assetid: bfa76e5b-6f6e-470a-ba3a-7ecff9f67f7b
keywords:
- Framework servizi di testo Metodo ShowKeysForKeyScanMode
- Framework dei servizi di testo del metodo ShowKeysForKeyScanMode, interfaccia ISoftKbd
- ISoftKbd Interface Text Services Framework, metodo ShowKeysForKeyScanMode
topic_type:
- apiref
api_name:
- ISoftKbd.ShowKeysForKeyScanMode
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7c46fbfc103c0ba40294e4c149d5fd427296765
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478203"
---
# <a name="isoftkbdshowkeysforkeyscanmode-method"></a><span data-ttu-id="bde98-106">Metodo ISoftKbd:: ShowKeysForKeyScanMode</span><span class="sxs-lookup"><span data-stu-id="bde98-106">ISoftKbd::ShowKeysForKeyScanMode method</span></span>

<span data-ttu-id="bde98-107">Il metodo **ISoftKbd:: ShowKeysForKeyScanMode** Visualizza le chiavi usate per la modalità di analisi della chiave per una tastiera soft.</span><span class="sxs-lookup"><span data-stu-id="bde98-107">The **ISoftKbd::ShowKeysForKeyScanMode** method displays the keys used for the key scan mode for a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="bde98-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bde98-108">Syntax</span></span>


```C++
HRESULT ShowKeysForKeyScanMode(
  [in] KEYID *lpKeyID,
  [in] INT   iKeyNum,
  [in] BOOL  fHighL
);
```



## <a name="parameters"></a><span data-ttu-id="bde98-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="bde98-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bde98-110">*lpKeyID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bde98-110">*lpKeyID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bde98-111">Puntatore a una matrice di elementi KEYID che indica gli identificatori delle chiavi da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="bde98-111">Pointer to an array of KEYID elements indicating the identifiers of keys to display.</span></span>

</dd> <dt>

<span data-ttu-id="bde98-112">*iKeyNum* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bde98-112">*iKeyNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bde98-113">Numero di chiavi da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="bde98-113">The number of keys to display.</span></span>

</dd> <dt>

<span data-ttu-id="bde98-114">*fHighL* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bde98-114">*fHighL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bde98-115">TRUE se il metodo deve evidenziare le chiavi e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="bde98-115">TRUE if the method is to highlight the keys, and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bde98-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bde98-116">Return value</span></span>

<span data-ttu-id="bde98-117">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="bde98-117">This method can return one of these values.</span></span>



| <span data-ttu-id="bde98-118">Valore</span><span class="sxs-lookup"><span data-stu-id="bde98-118">Value</span></span>                                                                                        | <span data-ttu-id="bde98-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bde98-119">Description</span></span>                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="bde98-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bde98-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="bde98-121">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="bde98-121">The method was successful.</span></span><br/>        |
| <dl> <span data-ttu-id="bde98-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="bde98-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="bde98-123">Uno dei parametri non è valido.</span><span class="sxs-lookup"><span data-stu-id="bde98-123">One of the parameters is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="bde98-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bde98-124">Requirements</span></span>



| <span data-ttu-id="bde98-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="bde98-125">Requirement</span></span> | <span data-ttu-id="bde98-126">Valore</span><span class="sxs-lookup"><span data-stu-id="bde98-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bde98-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bde98-127">Minimum supported client</span></span><br/> | <span data-ttu-id="bde98-128">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bde98-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="bde98-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bde98-129">Minimum supported server</span></span><br/> | <span data-ttu-id="bde98-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bde98-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="bde98-131">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="bde98-131">Redistributable</span></span><br/>          | <span data-ttu-id="bde98-132">TSF 1,0 su Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bde98-132">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="bde98-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bde98-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="bde98-134"><dt>Softkbdc. h</dt></span><span class="sxs-lookup"><span data-stu-id="bde98-134"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="bde98-135">IDL</span><span class="sxs-lookup"><span data-stu-id="bde98-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bde98-136"><dt>Softkbd. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bde98-136"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="bde98-137">DLL</span><span class="sxs-lookup"><span data-stu-id="bde98-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bde98-138"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bde98-138"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bde98-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bde98-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bde98-140">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="bde98-140">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> </dl>

 

 





