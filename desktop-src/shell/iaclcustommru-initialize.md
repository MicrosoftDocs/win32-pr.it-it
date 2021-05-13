---
description: Carica un elenco di stringhe nell'elenco MRU (Most Recently Used) dal Registro di sistema.
title: Metodo IACLCustomMRU::Initialize
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IACLCustomMRU.Initialize
api_type:
- COM
api_location: ''
ms.assetid: 358921b0-46c4-4428-b0b5-57a44fc3247b
ms.openlocfilehash: 715c6991021070dd132942de0bb18c8b77684860
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841232"
---
# <a name="iaclcustommruinitialize-method"></a><span data-ttu-id="89da6-103">Metodo IACLCustomMRU::Initialize</span><span class="sxs-lookup"><span data-stu-id="89da6-103">IACLCustomMRU::Initialize method</span></span>

<span data-ttu-id="89da6-104">Carica un elenco di stringhe nell'elenco degli ultimi caratteri usati dal Registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="89da6-104">Loads a list of strings into the most recently used (MRU) list from the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="89da6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="89da6-105">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] LPCWSTR pwszMRURegKey,
  [in] DWORD   dwMax
);
```



## <a name="parameters"></a><span data-ttu-id="89da6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="89da6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89da6-107">*pwszMRURegKey* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="89da6-107">*pwszMRURegKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89da6-108">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="89da6-108">Type: **LPCWSTR**</span></span>

<span data-ttu-id="89da6-109">Puntatore a un buffer contenente la chiave del Registro di sistema contenente le stringhe per l'elenco MRU.</span><span class="sxs-lookup"><span data-stu-id="89da6-109">A pointer to a buffer containing the registry key holding the strings for the MRU list.</span></span>

</dd> <dt>

<span data-ttu-id="89da6-110">*dwMax* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="89da6-110">*dwMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89da6-111">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="89da6-111">Type: **DWORD**</span></span>

<span data-ttu-id="89da6-112">Numero massimo di voci che possono essere prese da *pwszMRURegKey*.</span><span class="sxs-lookup"><span data-stu-id="89da6-112">The maximum number of entries that can be taken from *pwszMRURegKey*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89da6-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="89da6-113">Return value</span></span>

<span data-ttu-id="89da6-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="89da6-114">Type: **HRESULT**</span></span>

<span data-ttu-id="89da6-115">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="89da6-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="89da6-116">In caso contrario, restituisce un **codice di errore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="89da6-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="89da6-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="89da6-117">Requirements</span></span>



| <span data-ttu-id="89da6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="89da6-118">Requirement</span></span> | <span data-ttu-id="89da6-119">Valore</span><span class="sxs-lookup"><span data-stu-id="89da6-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="89da6-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89da6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="89da6-121">Solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="89da6-121">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="89da6-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89da6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="89da6-123">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="89da6-123">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 




