---
description: La proprietà Balance imposta o Recupera il saldo del altoparlante per l'output del flusso audio.
ms.assetid: b0e6bf16-b1d1-453d-8b58-272565c3d6e6
title: Proprietà Balance
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1334fcc51695f04ab0026ded8c68c17cb07aa0b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304262"
---
# <a name="balance-property"></a><span data-ttu-id="f34c6-103">Proprietà Balance</span><span class="sxs-lookup"><span data-stu-id="f34c6-103">Balance Property</span></span>

> [!Note]  
> <span data-ttu-id="f34c6-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f34c6-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="f34c6-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="f34c6-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="f34c6-106">La `Balance` proprietà imposta o Recupera il saldo del altoparlante per l'output del flusso audio.</span><span class="sxs-lookup"><span data-stu-id="f34c6-106">The `Balance` property sets or retrieves the speaker balance for the audio stream output.</span></span>

``` syntax
[ iBalance = ] MSWebDVD.Balance
```

## <a name="return-value"></a><span data-ttu-id="f34c6-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f34c6-107">Return Value</span></span>

<span data-ttu-id="f34c6-108">Restituisce un valore intero che rappresenta i livelli di bilanciamento.</span><span class="sxs-lookup"><span data-stu-id="f34c6-108">Returns an integer value representing the balance levels.</span></span> <span data-ttu-id="f34c6-109">L'intervallo di input consentito è compreso tra-10.000 e 10.000.</span><span class="sxs-lookup"><span data-stu-id="f34c6-109">The allowable input range is -10,000 to 10,000.</span></span> <span data-ttu-id="f34c6-110">Un valore pari a 0 imposta un saldo neutro, ovvero gli altoparlanti sinistro e destro ricevono lo stesso segnale audio di ampiezza.</span><span class="sxs-lookup"><span data-stu-id="f34c6-110">A value of 0 sets a neutral balance, that is both left and right speakers are given the same amplitude audio signal.</span></span>

## <a name="remarks"></a><span data-ttu-id="f34c6-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="f34c6-111">Remarks</span></span>

<span data-ttu-id="f34c6-112">Questa proprietà è di lettura/scrittura e il valore predefinito è 0, vale a dire che entrambi gli speaker ricevono segnali audio equivalenti.</span><span class="sxs-lookup"><span data-stu-id="f34c6-112">This property is read/write with a default value of 0, meaning that both speakers receive equivalent audio signals.</span></span> <span data-ttu-id="f34c6-113">Come per la proprietà [**volume**](volume-property.md) , le unità corrispondono a .01 decibel (moltiplicato per-1 quando</span><span class="sxs-lookup"><span data-stu-id="f34c6-113">As with the [**Volume**](volume-property.md) property, units correspond to .01 decibels (multiplied by -1 when</span></span>


```
iBalance
```



<span data-ttu-id="f34c6-114">è un valore positivo).</span><span class="sxs-lookup"><span data-stu-id="f34c6-114">is a positive value).</span></span> <span data-ttu-id="f34c6-115">Ad esempio, il valore 1000 indica 10 dB sul canale destro e 90 dB sul canale sinistro.</span><span class="sxs-lookup"><span data-stu-id="f34c6-115">For example, a value of 1000 indicates 10 dB on the right channel and 90 dB on the left channel.</span></span>

 

 



