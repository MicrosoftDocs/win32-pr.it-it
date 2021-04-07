---
title: Metodo ISearchDesktop ExecuteSQLQuery
description: Accetta un puntatore a una stringa che contiene una query Structured Query Language (SQL) e i relativi attributi e restituisce un puntatore al set restituito.
ms.assetid: df3f473b-0bee-4035-abf8-dbe5249ef0ed
keywords:
- Funzionalità dell'ambiente Windows legacy del metodo ExecuteSQLQuery
- Funzionalità dell'ambiente Windows legacy del metodo ExecuteSQLQuery, interfaccia ISearchDesktop
- Funzionalità dell'ambiente Windows legacy dell'interfaccia ISearchDesktop, metodo ExecuteSQLQuery
topic_type:
- apiref
api_name:
- ISearchDesktop.ExecuteSQLQuery
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f0b13ff361d07f99efe1366e2201d610eac10523
ms.sourcegitcommit: b9a94cea8f83153214af4c09509e1cc61a1bb616
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/19/2020
ms.locfileid: "103724012"
---
# <a name="isearchdesktopexecutesqlquery-method"></a><span data-ttu-id="4c5ac-106">Metodo ISearchDesktop:: ExecuteSQLQuery</span><span class="sxs-lookup"><span data-stu-id="4c5ac-106">ISearchDesktop::ExecuteSQLQuery method</span></span>

> [!NOTE]
> <span data-ttu-id="4c5ac-107">Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="4c5ac-107">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="4c5ac-108">Nelle versioni successive usare invece l' [API di ricerca di Windows](../search/-search-reference-entry-page.md) .</span><span class="sxs-lookup"><span data-stu-id="4c5ac-108">On later releases, use the [Windows Search API](../search/-search-reference-entry-page.md) instead.</span></span> 

<span data-ttu-id="4c5ac-109">Accetta un puntatore a una stringa che contiene una query Structured Query Language (SQL) e i relativi attributi e restituisce un puntatore al set restituito.</span><span class="sxs-lookup"><span data-stu-id="4c5ac-109">Takes a pointer to a string that contains a Structured Query Language (SQL) query and its attributes and returns a pointer to the return set.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c5ac-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4c5ac-110">Syntax</span></span>


```C++
HRESULT ExecuteSQLQuery(
  [in]  LPCWSTR *pdwAttributes,
  [in]  LPCWSTR pwszURL,
  [out] ppidUrl *ppidUrl
);
```



## <a name="parameters"></a><span data-ttu-id="4c5ac-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="4c5ac-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c5ac-112">*pdwAttributes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4c5ac-112">*pdwAttributes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c5ac-113">Tipo: **LPCWSTR \***</span><span class="sxs-lookup"><span data-stu-id="4c5ac-113">Type: **LPCWSTR\***</span></span>

<span data-ttu-id="4c5ac-114">Stringa contenente gli altri attributi per la query.</span><span class="sxs-lookup"><span data-stu-id="4c5ac-114">A string that contains the other attributes for the query.</span></span>

</dd> <dt>

<span data-ttu-id="4c5ac-115">*pwszURL* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4c5ac-115">*pwszURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c5ac-116">Tipo: **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="4c5ac-116">Type: **LPCWSTR**</span></span>

<span data-ttu-id="4c5ac-117">Stringa che contiene la query SQL.</span><span class="sxs-lookup"><span data-stu-id="4c5ac-117">A string that contains the SQL query.</span></span>

</dd> <dt>

<span data-ttu-id="4c5ac-118">*ppidUrl* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4c5ac-118">*ppidUrl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c5ac-119">Tipo: **ppidUrl \***</span><span class="sxs-lookup"><span data-stu-id="4c5ac-119">Type: **ppidUrl\***</span></span>

<span data-ttu-id="4c5ac-120">Quando questo metodo viene restituito correttamente, contiene un puntatore al recordset restituito.</span><span class="sxs-lookup"><span data-stu-id="4c5ac-120">When this method returns successfully, contains a pointer to the returned recordset.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c5ac-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4c5ac-121">Return value</span></span>

<span data-ttu-id="4c5ac-122">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4c5ac-122">Type: **HRESULT**</span></span>

<span data-ttu-id="4c5ac-123">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4c5ac-123">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4c5ac-124">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4c5ac-124">Otherwise, it returns an **HRESULT** error code.</span></span>

 

 




