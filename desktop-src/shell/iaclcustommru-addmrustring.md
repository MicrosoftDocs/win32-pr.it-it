---
description: Aggiunge una voce all'elenco degli ultimi elementi usati (MRU).
title: 'Metodo IACLCustomMRU:: AddMRUString'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IACLCustomMRU.AddMRUString
api_type:
- COM
api_location: ''
ms.assetid: d8fb8fa5-452b-45fd-b015-d9bf3d0c642e
ms.openlocfilehash: d2f444041f466b367f3d4532f65029bcc69c3683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994637"
---
# <a name="iaclcustommruaddmrustring-method"></a><span data-ttu-id="80302-103">Metodo IACLCustomMRU:: AddMRUString</span><span class="sxs-lookup"><span data-stu-id="80302-103">IACLCustomMRU::AddMRUString method</span></span>

<span data-ttu-id="80302-104">Aggiunge una voce all'elenco degli ultimi elementi usati (MRU).</span><span class="sxs-lookup"><span data-stu-id="80302-104">Adds an entry to the most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="80302-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="80302-105">Syntax</span></span>


```C++
HRESULT AddMRUString(
  [in] LPCWSTR pwszEntry
);
```



## <a name="parameters"></a><span data-ttu-id="80302-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="80302-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80302-107">*pwszEntry* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80302-107">*pwszEntry* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80302-108">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="80302-108">Type: **LPCWSTR**</span></span>

<span data-ttu-id="80302-109">Puntatore a un buffer contenente la nuova voce.</span><span class="sxs-lookup"><span data-stu-id="80302-109">A pointer to a buffer containing the new entry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80302-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="80302-110">Return value</span></span>

<span data-ttu-id="80302-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="80302-111">Type: **HRESULT**</span></span>

<span data-ttu-id="80302-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="80302-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="80302-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="80302-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="80302-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="80302-114">Requirements</span></span>



| <span data-ttu-id="80302-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="80302-115">Requirement</span></span> | <span data-ttu-id="80302-116">Valore</span><span class="sxs-lookup"><span data-stu-id="80302-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="80302-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="80302-117">Minimum supported client</span></span><br/> | <span data-ttu-id="80302-118">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="80302-118">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="80302-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="80302-119">Minimum supported server</span></span><br/> | <span data-ttu-id="80302-120">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="80302-120">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 




