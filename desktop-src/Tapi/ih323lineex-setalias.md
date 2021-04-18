---
description: Il metodo sealias configura un alias H. 323 predefinito per l'indirizzo. Questo alias verrà usato nello scambio di configurazione della chiamata H. 323, in modo che l'altra parte conosca il nome di questa entità.
ms.assetid: 09608214-7346-4ee8-bbfd-0877d3ad0766
title: 'Metodo IH323LineEx:: sealias (H323priv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7341d177297cf95f46d07e503244f06b2c4dea71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326149"
---
# <a name="ih323lineexsetalias-method"></a><span data-ttu-id="53512-104">Metodo IH323LineEx:: sealias</span><span class="sxs-lookup"><span data-stu-id="53512-104">IH323LineEx::SetAlias method</span></span>

<span data-ttu-id="53512-105">\[L' **alias** non è disponibile per l'utilizzo in Windows Vista, windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="53512-105">\[**SetAlias** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="53512-106">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="53512-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="53512-107">Il metodo **sealias** configura un alias H. 323 predefinito per l'indirizzo.</span><span class="sxs-lookup"><span data-stu-id="53512-107">The **SetAlias** method configures a default H.323 alias for the address.</span></span> <span data-ttu-id="53512-108">Questo alias verrà usato nello scambio di configurazione della chiamata H. 323, in modo che l'altra parte conosca il nome di questa entità.</span><span class="sxs-lookup"><span data-stu-id="53512-108">This alias will be used in the H.323 call setup exchange so that the other party knows the name of this party.</span></span>

<span data-ttu-id="53512-109">Se si chiama questo metodo una seconda volta, l'alias precedente verrà sovrascritto.</span><span class="sxs-lookup"><span data-stu-id="53512-109">Calling this method a second time will overwrite the previous alias.</span></span>

<span data-ttu-id="53512-110">Il set di alias su questa interfaccia verrà utilizzato solo quando non esiste un altro modo per trovare un alias appropriato da parte del TSP.</span><span class="sxs-lookup"><span data-stu-id="53512-110">The alias set on this interface will be used only when there is no other way for the TSP to find a proper alias.</span></span> <span data-ttu-id="53512-111">In futuro, quando viene aggiunto il supporto per gatekeeper nel TSP, l'alias registrato sul gatekeeper o assegnato dal Gatekeeper eseguirà l'override di qualsiasi valore impostato tramite questo metodo.</span><span class="sxs-lookup"><span data-stu-id="53512-111">In the future, when gatekeeper support is added into the TSP, the alias registered to the gatekeeper or assigned by the gatekeeper will override whatever is set through this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="53512-112">Sintassi</span><span class="sxs-lookup"><span data-stu-id="53512-112">Syntax</span></span>


```C++
HRESULT SetAlias(
  [in] WCHAR *strAlias,
  [in] DWORD dwLength
);
```



## <a name="parameters"></a><span data-ttu-id="53512-113">Parametri</span><span class="sxs-lookup"><span data-stu-id="53512-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53512-114">*strAlias* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53512-114">*strAlias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53512-115">Alias da utilizzare in Unicode.</span><span class="sxs-lookup"><span data-stu-id="53512-115">The alias to be used, in Unicode.</span></span> <span data-ttu-id="53512-116">Non è necessaria la terminazione **null** .</span><span class="sxs-lookup"><span data-stu-id="53512-116">**Null** termination is not required.</span></span>

</dd> <dt>

<span data-ttu-id="53512-117">*dwLength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="53512-117">*dwLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53512-118">Lunghezza del nome alias in numero di caratteri, incluso il terminatore **null** .</span><span class="sxs-lookup"><span data-stu-id="53512-118">The length of the alias name in number of characters, including the **null** terminator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53512-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="53512-119">Return value</span></span>

<span data-ttu-id="53512-120">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="53512-120">This method can return one of these values.</span></span>



| <span data-ttu-id="53512-121">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="53512-121">Return code</span></span>                                                                               | <span data-ttu-id="53512-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="53512-122">Description</span></span>                                                                                                                      |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="53512-123"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="53512-123"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="53512-124">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="53512-124">Method succeeded.</span></span><br/>                                                                                                     |
| <dl> <span data-ttu-id="53512-125"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="53512-125"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="53512-126">Il numero di caratteri indicato in *dwLength* supera il numero effettivo di caratteri nel parametro *strAlias* .</span><span class="sxs-lookup"><span data-stu-id="53512-126">The number of characters indicated in *dwLength* exceeds the actual number of characters in the *strAlias* parameter.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="53512-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="53512-127">Requirements</span></span>



| <span data-ttu-id="53512-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="53512-128">Requirement</span></span> | <span data-ttu-id="53512-129">Valore</span><span class="sxs-lookup"><span data-stu-id="53512-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="53512-130">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="53512-130">TAPI version</span></span><br/> | <span data-ttu-id="53512-131">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="53512-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="53512-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="53512-132">Header</span></span><br/>       | <dl> <span data-ttu-id="53512-133"><dt>H323priv. h</dt></span><span class="sxs-lookup"><span data-stu-id="53512-133"><dt>H323priv.h</dt></span></span> </dl> |
| <span data-ttu-id="53512-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="53512-134">Library</span></span><br/>      | <dl> <span data-ttu-id="53512-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="53512-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="53512-136">DLL</span><span class="sxs-lookup"><span data-stu-id="53512-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="53512-137"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53512-137"><dt>Tapi3.dll</dt></span></span> </dl>  |



 

 




