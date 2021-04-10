---
description: Il metodo CanStep determina se il decodificatore MPEG-2 nel sistema locale può eseguire lo stepping del frame in una direzione specificata.
ms.assetid: 21721722-0bf4-4cc7-a0e4-96b353888948
title: Metodo CanStep
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 506e7436e5ec79947aceeca69891e52074cf2ea7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104048913"
---
# <a name="canstep-method"></a><span data-ttu-id="2c110-103">Metodo CanStep</span><span class="sxs-lookup"><span data-stu-id="2c110-103">CanStep Method</span></span>

> [!Note]  
> <span data-ttu-id="2c110-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="2c110-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="2c110-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="2c110-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="2c110-106">Il `CanStep` metodo determina se il decodificatore MPEG-2 nel sistema locale può eseguire lo stepping del frame in una direzione specificata.</span><span class="sxs-lookup"><span data-stu-id="2c110-106">The `CanStep` method determines whether the MPEG-2 decoder on the local system can perform frame stepping in a specified direction.</span></span>

``` syntax
[ bCanStep = ] MSWebDVD.CanStep(bDirection)
```

## <a name="parameters"></a><span data-ttu-id="2c110-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="2c110-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c110-108"><span id="bDirection"></span><span id="bdirection"></span><span id="BDIRECTION"></span>*bDirection*</span><span class="sxs-lookup"><span data-stu-id="2c110-108"><span id="bDirection"></span><span id="bdirection"></span><span id="BDIRECTION"></span>*bDirection*</span></span>
</dt> <dd>

<span data-ttu-id="2c110-109">Valore booleano usato come flag per specificare la direzione, avanti o indietro, della capacità di esecuzione dei frame del decodificatore.</span><span class="sxs-lookup"><span data-stu-id="2c110-109">Boolean used as a flag to specify the direction, forward or backward, of decoder's frame-stepping ability.</span></span>



| <span data-ttu-id="2c110-110">Valore</span><span class="sxs-lookup"><span data-stu-id="2c110-110">Value</span></span> | <span data-ttu-id="2c110-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c110-111">Description</span></span>                                          |
|-------|------------------------------------------------------|
| <span data-ttu-id="2c110-112">true</span><span class="sxs-lookup"><span data-stu-id="2c110-112">true</span></span>  | <span data-ttu-id="2c110-113">È possibile eseguire il passaggio del decodificatore indietro?</span><span class="sxs-lookup"><span data-stu-id="2c110-113">Can decoder step backward?</span></span>                           |
| <span data-ttu-id="2c110-114">false</span><span class="sxs-lookup"><span data-stu-id="2c110-114">false</span></span> | <span data-ttu-id="2c110-115">Il decodificatore può andare avanti?</span><span class="sxs-lookup"><span data-stu-id="2c110-115">Can decoder step forward?</span></span> <span data-ttu-id="2c110-116">Si tratta del valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="2c110-116">This is the default value.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c110-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2c110-117">Return Value</span></span>

<span data-ttu-id="2c110-118">Restituisce un valore booleano true se il decodificatore può eseguire un'istruzione nella direzione specificata e false in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="2c110-118">Returns a Boolean value of true if the decoder can step in the specified direction, and false otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c110-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="2c110-119">Remarks</span></span>

<span data-ttu-id="2c110-120">Non tutti i decodificatori MPEG-2 hardware supportano le nuove funzionalità di avanzamento dei frame in DirectShow® 8,0.</span><span class="sxs-lookup"><span data-stu-id="2c110-120">Not all hardware MPEG-2 decoders support the new frame stepping capabilities in DirectShow® 8.0.</span></span> <span data-ttu-id="2c110-121">Questo metodo esegue una query sul decodificatore per le funzionalità di avanzamento dei frame.</span><span class="sxs-lookup"><span data-stu-id="2c110-121">This method queries the decoder for its frame stepping capabilities.</span></span> <span data-ttu-id="2c110-122">Se il decodificatore è in grado di eseguire l'esecuzione dei frame, un'applicazione può usare il metodo [**Step**](step-method.md) per scorrere i frame.</span><span class="sxs-lookup"><span data-stu-id="2c110-122">If the decoder can perform frame stepping, an application can use the [**Step**](step-method.md) method to step through frames.</span></span> <span data-ttu-id="2c110-123">Questo metodo restituirà sempre **true** se viene usato un decodificatore software.</span><span class="sxs-lookup"><span data-stu-id="2c110-123">This method will always return **true** if a software decoder is being used.</span></span>

 

 



