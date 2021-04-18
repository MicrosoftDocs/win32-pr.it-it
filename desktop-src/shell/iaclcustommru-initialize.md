---
description: Carica un elenco di stringhe nell'elenco degli ultimi elementi usati (MRU) dal registro di sistema.
title: 'Metodo IACLCustomMRU:: Initialize'
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
ms.openlocfilehash: 768df625cb66c888ddccc85f72de5b8676c20b10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994632"
---
# <a name="iaclcustommruinitialize-method"></a><span data-ttu-id="fd1c7-103">Metodo IACLCustomMRU:: Initialize</span><span class="sxs-lookup"><span data-stu-id="fd1c7-103">IACLCustomMRU::Initialize method</span></span>

<span data-ttu-id="fd1c7-104">Carica un elenco di stringhe nell'elenco degli ultimi elementi usati (MRU) dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="fd1c7-104">Loads a list of strings into the most recently used (MRU) list from the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd1c7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fd1c7-105">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] LPCWSTR pwszMRURegKey,
  [in] DWORD   dwMax
);
```



## <a name="parameters"></a><span data-ttu-id="fd1c7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fd1c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd1c7-107">*pwszMRURegKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd1c7-107">*pwszMRURegKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd1c7-108">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="fd1c7-108">Type: **LPCWSTR**</span></span>

<span data-ttu-id="fd1c7-109">Puntatore a un buffer contenente la chiave del registro di sistema contenente le stringhe per l'elenco MRU.</span><span class="sxs-lookup"><span data-stu-id="fd1c7-109">A pointer to a buffer containing the registry key holding the strings for the MRU list.</span></span>

</dd> <dt>

<span data-ttu-id="fd1c7-110">*dwMax* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fd1c7-110">*dwMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fd1c7-111">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="fd1c7-111">Type: **DWORD**</span></span>

<span data-ttu-id="fd1c7-112">Numero massimo di voci che possono essere ricavate da *pwszMRURegKey*.</span><span class="sxs-lookup"><span data-stu-id="fd1c7-112">The maximum number of entries that can be taken from *pwszMRURegKey*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd1c7-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fd1c7-113">Return value</span></span>

<span data-ttu-id="fd1c7-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="fd1c7-114">Type: **HRESULT**</span></span>

<span data-ttu-id="fd1c7-115">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="fd1c7-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fd1c7-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="fd1c7-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd1c7-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fd1c7-117">Requirements</span></span>



| <span data-ttu-id="fd1c7-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd1c7-118">Requirement</span></span> | <span data-ttu-id="fd1c7-119">Valore</span><span class="sxs-lookup"><span data-stu-id="fd1c7-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fd1c7-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd1c7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fd1c7-121">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="fd1c7-121">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="fd1c7-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fd1c7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fd1c7-123">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fd1c7-123">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 




