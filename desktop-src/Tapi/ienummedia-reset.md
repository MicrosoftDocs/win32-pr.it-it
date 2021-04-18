---
description: Il metodo Reset reimposta l'inizio della sequenza di enumerazione.
ms.assetid: 338e0614-8f18-4ee2-8697-66ff3898f813
title: 'Metodo IEnumMedia:: Reset'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14624d5a048df2f5bc80205f34f262068c53da74
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320649"
---
# <a name="ienummediareset-method"></a><span data-ttu-id="178d8-103">Metodo IEnumMedia:: Reset</span><span class="sxs-lookup"><span data-stu-id="178d8-103">IEnumMedia::Reset method</span></span>

<span data-ttu-id="178d8-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="178d8-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="178d8-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="178d8-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="178d8-106">Il metodo **Reset** Reimposta l'inizio della sequenza di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="178d8-106">The **Reset** method resets to the beginning of enumeration sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="178d8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="178d8-107">Syntax</span></span>


```C++
HRESULT Reset();
```

## <a name="parameters"></a><span data-ttu-id="178d8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="178d8-108">Parameters</span></span>
<span data-ttu-id="178d8-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="178d8-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="178d8-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="178d8-110">Return value</span></span>
<span data-ttu-id="178d8-111">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="178d8-111">This method can return one of these values.</span></span>

| <span data-ttu-id="178d8-112">Valore</span><span class="sxs-lookup"><span data-stu-id="178d8-112">Value</span></span> | <span data-ttu-id="178d8-113">Significato</span><span class="sxs-lookup"><span data-stu-id="178d8-113">Meaning</span></span>                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <span data-ttu-id="178d8-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="178d8-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="178d8-115">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="178d8-115">Method succeeded.</span></span> <br/>         |
