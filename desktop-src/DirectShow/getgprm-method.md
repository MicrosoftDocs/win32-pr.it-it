---
description: Il metodo GetGPRM Recupera il registro del parametro generale specificato.
ms.assetid: 66afd2a5-6aa1-4280-93cf-dd3cfed2499d
title: Metodo GetGPRM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d82522f834a6f3bda8abefb492d5cc8b568872e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522313"
---
# <a name="getgprm-method"></a><span data-ttu-id="81511-103">Metodo GetGPRM</span><span class="sxs-lookup"><span data-stu-id="81511-103">GetGPRM Method</span></span>

> [!Note]  
> <span data-ttu-id="81511-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="81511-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="81511-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="81511-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="81511-106">Il `GetGPRM` metodo recupera il registro del parametro generale specificato.</span><span class="sxs-lookup"><span data-stu-id="81511-106">The `GetGPRM` method retrieves the specified general parameter register.</span></span>

``` syntax
[ iGPRM = ] MSWebDVD.GetGPRM(iIndex)
```

## <a name="parameters"></a><span data-ttu-id="81511-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="81511-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81511-108"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span><span class="sxs-lookup"><span data-stu-id="81511-108"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span></span>
</dt> <dd>

<span data-ttu-id="81511-109">Specifica il registro da recuperare come Integer.</span><span class="sxs-lookup"><span data-stu-id="81511-109">Specifies the register to retrieve as an Integer.</span></span> <span data-ttu-id="81511-110">Il valore deve essere compreso tra 0 e 15.</span><span class="sxs-lookup"><span data-stu-id="81511-110">The value must range from 0 through 15.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81511-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="81511-111">Return Value</span></span>

<span data-ttu-id="81511-112">Restituisce un valore intero che rappresenta il registro specificato.</span><span class="sxs-lookup"><span data-stu-id="81511-112">Returns an integer value representing the specified register.</span></span>

## <a name="remarks"></a><span data-ttu-id="81511-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="81511-113">Remarks</span></span>

<span data-ttu-id="81511-114">Questo metodo non è necessario per le funzionalità di navigazione o riproduzione DVD con l'oggetto **mswebdvd** .</span><span class="sxs-lookup"><span data-stu-id="81511-114">This method is not required for any DVD navigation or playback functionality using the **MSWebDVD** object.</span></span> <span data-ttu-id="81511-115">Viene fornito per gli utenti con una conoscenza approfondita della specifica DVD che desiderano implementare funzionalità avanzate.</span><span class="sxs-lookup"><span data-stu-id="81511-115">It is provided for those with a thorough understanding of the DVD specification who want to implement advanced features.</span></span> <span data-ttu-id="81511-116">GPRMs può essere usato per contenere qualsiasi valore, in modo che possano essere impostati e letti liberamente.</span><span class="sxs-lookup"><span data-stu-id="81511-116">GPRMs can be used to hold any values, so they can be freely set and read.</span></span> <span data-ttu-id="81511-117">Tuttavia, poiché GPRMs vengono usati anche per archiviare i comandi del disco, la modifica dei valori usando [**SetGPRM**](setgprm-method.md) può causare un comportamento imprevedibile.</span><span class="sxs-lookup"><span data-stu-id="81511-117">But since GPRMs are used to store disc commands as well, changing their values using [**SetGPRM**](setgprm-method.md) can result in unpredictable behavior.</span></span>

## <a name="see-also"></a><span data-ttu-id="81511-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="81511-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81511-119">**SetGPRM**</span><span class="sxs-lookup"><span data-stu-id="81511-119">**SetGPRM**</span></span>](setgprm-method.md)
</dt> </dl>

 

 



