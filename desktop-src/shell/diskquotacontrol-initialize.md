---
description: Apre un volume specificato e inizializza il relativo oggetto di controllo della quota.
ms.assetid: 20eae2a3-f602-48a2-bf1c-65570e7a5d21
title: Metodo tialize DiskQuotaControl.Ini
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.Initialize
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 919720f01c67b6df3189b760aa8cefbb29615179
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977175"
---
# <a name="diskquotacontrolinitialize-method"></a><span data-ttu-id="74a1c-103">Metodo tialize DiskQuotaControl.Ini</span><span class="sxs-lookup"><span data-stu-id="74a1c-103">DiskQuotaControl.Initialize method</span></span>

<span data-ttu-id="74a1c-104">Apre un volume specificato e inizializza il relativo oggetto di controllo della quota.</span><span class="sxs-lookup"><span data-stu-id="74a1c-104">Opens a specified volume and initializes its quota control object.</span></span>

## <a name="syntax"></a><span data-ttu-id="74a1c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="74a1c-105">Syntax</span></span>


```JScript
DiskQuotaControl.Initialize(
  sPath,
  bReadWrite
)
```



## <a name="parameters"></a><span data-ttu-id="74a1c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="74a1c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74a1c-107">*sPath*</span><span class="sxs-lookup"><span data-stu-id="74a1c-107">*sPath*</span></span> 
</dt> <dd>

<span data-ttu-id="74a1c-108">Tipo: **stringa**</span><span class="sxs-lookup"><span data-stu-id="74a1c-108">Type: **String**</span></span>

<span data-ttu-id="74a1c-109">Valore stringa che contiene il percorso completo del volume da inizializzare.</span><span class="sxs-lookup"><span data-stu-id="74a1c-109">A string value that contains the fully qualified path of the volume to be initialized.</span></span>

</dd> <dt>

<span data-ttu-id="74a1c-110">*bReadWrite*</span><span class="sxs-lookup"><span data-stu-id="74a1c-110">*bReadWrite*</span></span> 
</dt> <dd>

<span data-ttu-id="74a1c-111">Tipo: **booleano**</span><span class="sxs-lookup"><span data-stu-id="74a1c-111">Type: **Boolean**</span></span>

<span data-ttu-id="74a1c-112">Valore booleano che specifica la modalità di apertura del volume.</span><span class="sxs-lookup"><span data-stu-id="74a1c-112">A Boolean value that specifies how the volume is to be opened.</span></span> <span data-ttu-id="74a1c-113">Impostare *bReadWrite* su **true** per l'accesso in lettura/scrittura o **false** per l'accesso in sola lettura.</span><span class="sxs-lookup"><span data-stu-id="74a1c-113">Set *bReadWrite* to **TRUE** for read/write access or **FALSE** for read-only access.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74a1c-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="74a1c-114">Return value</span></span>

<span data-ttu-id="74a1c-115">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="74a1c-115">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="74a1c-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="74a1c-116">Requirements</span></span>



| <span data-ttu-id="74a1c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="74a1c-117">Requirement</span></span> | <span data-ttu-id="74a1c-118">Valore</span><span class="sxs-lookup"><span data-stu-id="74a1c-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74a1c-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74a1c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="74a1c-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="74a1c-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="74a1c-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="74a1c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="74a1c-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="74a1c-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="74a1c-123">DLL</span><span class="sxs-lookup"><span data-stu-id="74a1c-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74a1c-124"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="74a1c-124"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74a1c-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="74a1c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74a1c-126">**Oggetto DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="74a1c-126">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




