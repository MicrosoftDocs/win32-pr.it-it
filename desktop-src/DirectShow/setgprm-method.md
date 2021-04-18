---
description: Il metodo SetGPRM imposta il registro del parametro generale specificato sul valore specificato.
ms.assetid: ded28f2a-5e40-4f76-9ed4-de10296529e1
title: Metodo SetGPRM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e7492c599cde4c074c1a806f897edf3a8fe0a4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303896"
---
# <a name="setgprm-method"></a><span data-ttu-id="2e748-103">Metodo SetGPRM</span><span class="sxs-lookup"><span data-stu-id="2e748-103">SetGPRM Method</span></span>

> [!Note]  
> <span data-ttu-id="2e748-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="2e748-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="2e748-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="2e748-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="2e748-106">Il `SetGPRM` metodo imposta il registro del parametro generale specificato sul valore specificato.</span><span class="sxs-lookup"><span data-stu-id="2e748-106">The `SetGPRM` method sets the specified general parameter register to the specified value.</span></span>

``` syntax
MSWebDVD.SetGPRM(iIndex, nValue)
```

## <a name="parameters"></a><span data-ttu-id="2e748-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="2e748-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e748-108"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span><span class="sxs-lookup"><span data-stu-id="2e748-108"><span id="iIndex"></span><span id="iindex"></span><span id="IINDEX"></span>*iIndex*</span></span>
</dt> <dd>

<span data-ttu-id="2e748-109">Specifica il registro del parametro generale da impostare come Integer.</span><span class="sxs-lookup"><span data-stu-id="2e748-109">Specifies the general parameter register to set as an Integer.</span></span> <span data-ttu-id="2e748-110">Il valore intero deve essere compreso tra 0 e 15.</span><span class="sxs-lookup"><span data-stu-id="2e748-110">The Integer value must range from 0 through 15.</span></span>

</dd> <dt>

<span data-ttu-id="2e748-111"><span id="nValue"></span><span id="nvalue"></span><span id="NVALUE"></span>*nValue*</span><span class="sxs-lookup"><span data-stu-id="2e748-111"><span id="nValue"></span><span id="nvalue"></span><span id="NVALUE"></span>*nValue*</span></span>
</dt> <dd>

<span data-ttu-id="2e748-112">Specifica il nuovo valore per il registro come intero.</span><span class="sxs-lookup"><span data-stu-id="2e748-112">Specifies the new value for the register as an Integer.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2e748-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="2e748-113">Remarks</span></span>

<span data-ttu-id="2e748-114">I registri di parametri generali, o GPRMs, sono registri a 16 bit che ciascun disco può usare in modo univoco per l'archiviazione temporanea dei dati.</span><span class="sxs-lookup"><span data-stu-id="2e748-114">General parameter registers, or GPRMs, are 16-bit registers that each disc can use in unique ways for temporary data storage.</span></span> <span data-ttu-id="2e748-115">Non è necessario che un'applicazione del lettore acceda a questi registri per qualsiasi controllo di riproduzione o navigazione standard usando l'oggetto **mswebdvd** .</span><span class="sxs-lookup"><span data-stu-id="2e748-115">A player application does not need to access these registers for any standard playback or navigation control using the **MSWebDVD** object.</span></span> <span data-ttu-id="2e748-116">Questo metodo viene fornito per le applicazioni del lettore che implementano funzionalità avanzate.</span><span class="sxs-lookup"><span data-stu-id="2e748-116">This method is provided for player applications implementing advanced functionality.</span></span> <span data-ttu-id="2e748-117">Non tentare di modificare direttamente il GPRMs, a meno che non si disponga di una conoscenza approfondita della specifica DVD e delle modalità di utilizzo di GPRMs sul disco specifico da riprodurre.</span><span class="sxs-lookup"><span data-stu-id="2e748-117">Do not attempt to modify the GPRMs directly unless you have a thorough knowledge of the DVD specification and the ways in which the GPRMs are used on the particular disc to be played.</span></span> <span data-ttu-id="2e748-118">La modifica di questi valori può causare un comportamento imprevedibile.</span><span class="sxs-lookup"><span data-stu-id="2e748-118">Changing these values can result in unpredictable behavior.</span></span>

 

 



