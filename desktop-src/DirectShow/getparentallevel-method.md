---
description: Il metodo DVDAdm. GetParentalLevel Recupera il livello padre che è stato salvato per ultimo nel registro di sistema.
ms.assetid: 2aadcf41-2c65-4f3a-8ce8-0fc9aa580ad9
title: Metodo GetParentalLevel
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdfa2c2193a9d02249076b2be2225fc50cd1edd5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401077"
---
# <a name="getparentallevel-method"></a><span data-ttu-id="f1893-103">Metodo GetParentalLevel</span><span class="sxs-lookup"><span data-stu-id="f1893-103">GetParentalLevel Method</span></span>

> [!Note]  
> <span data-ttu-id="f1893-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f1893-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="f1893-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="f1893-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="f1893-106">Il `DVDAdm.GetParentalLevel` metodo recupera il livello padre che è stato salvato per ultimo nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="f1893-106">The `DVDAdm.GetParentalLevel` method retrieves the parental level that was last saved to the registry.</span></span>

``` syntax
[ iParentalLevel = ] DVD.DVDAdm.GetParentalLevel()
```

## <a name="return-value"></a><span data-ttu-id="f1893-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f1893-107">Return Value</span></span>

<span data-ttu-id="f1893-108">Restituisce un numero intero compreso tra 1 e 8 che indica il livello padre predefinito.</span><span class="sxs-lookup"><span data-stu-id="f1893-108">Returns an Integer from 1 through 8 indicating the default parental level.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1893-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="f1893-109">Remarks</span></span>

<span data-ttu-id="f1893-110">Il livello padre recuperato da questo metodo non è necessariamente lo stesso livello attualmente archiviato nel controllo MSWebDVD. per ottenere il livello attualmente archiviato nel controllo, chiamare il metodo [**GetPlayerParentalLevel**](getplayerparentallevel-method.md) .</span><span class="sxs-lookup"><span data-stu-id="f1893-110">The parental level this method retrieves is not necessarily the same level currently stored in the MSWebDVD control; to get the level currently stored in the control, call the [**GetPlayerParentalLevel**](getplayerparentallevel-method.md) method.</span></span> <span data-ttu-id="f1893-111">Il valore-1 indica che la gestione padre è disabilitata.</span><span class="sxs-lookup"><span data-stu-id="f1893-111">A value of -1 indicates that parental management is disabled.</span></span>

## <a name="see-also"></a><span data-ttu-id="f1893-112">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f1893-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1893-113">Oggetto MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="f1893-113">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 



