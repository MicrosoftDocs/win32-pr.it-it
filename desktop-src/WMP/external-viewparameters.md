---
title: External. viewParameters
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. | External. viewParameters
ms.assetid: 0afabe35-2857-413a-a662-1a76d3fb75fe
keywords:
- Media Player di Windows External. viewParameters
topic_type:
- apiref
api_name:
- External.viewParameters
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea0adec580a68bd3f6b92beef1de814729848179
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328396"
---
# <a name="externalviewparameters"></a><span data-ttu-id="395cd-105">External. viewParameters</span><span class="sxs-lookup"><span data-stu-id="395cd-105">External.viewParameters</span></span>

> [!Note]  
> <span data-ttu-id="395cd-106">Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online.</span><span class="sxs-lookup"><span data-stu-id="395cd-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="395cd-107">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="395cd-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="395cd-108">La proprietà **viewParameters** recupera i parametri associati alla visualizzazione corrente in Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="395cd-108">The **viewParameters** property retrieves parameters associated with the current view in Windows Media Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="395cd-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="395cd-109">Syntax</span></span>

<span data-ttu-id="395cd-110">**finestra. External. viewParameters**</span><span class="sxs-lookup"><span data-stu-id="395cd-110">**window.external.viewParameters**</span></span>

## <a name="possible-values"></a><span data-ttu-id="395cd-111">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="395cd-111">Possible Values</span></span>

<span data-ttu-id="395cd-112">Questa proprietà restituisce una **stringa** di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="395cd-112">This property returns a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="395cd-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="395cd-113">Remarks</span></span>

<span data-ttu-id="395cd-114">Questa proprietà recupera i parametri impostati in precedenza dal negozio online.</span><span class="sxs-lookup"><span data-stu-id="395cd-114">This property retrieves parameters that were previously set by the online store.</span></span> <span data-ttu-id="395cd-115">Ad esempio, l'archivio online può specificare i parametri di visualizzazione nel parametro *ViewParams* del metodo [changeView](external-changeview.md) o il parametro *params* del metodo [changeViewOnlineList](external-changeviewonlinelist.md) .</span><span class="sxs-lookup"><span data-stu-id="395cd-115">For example, the online store can specify view parameters in the *ViewParams* parameter of the [changeView](external-changeview.md) method or the *Params* parameter of the [changeViewOnlineList](external-changeviewonlinelist.md) method.</span></span>

<span data-ttu-id="395cd-116">I parametri di visualizzazione non vengono interpretati da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="395cd-116">View parameters are not interpreted by Windows Media Player.</span></span> <span data-ttu-id="395cd-117">Vengono creati dal negozio online e hanno un significato solo per lo Store online.</span><span class="sxs-lookup"><span data-stu-id="395cd-117">They are created by the online store and have meaning only to the online store.</span></span>

## <a name="requirements"></a><span data-ttu-id="395cd-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="395cd-118">Requirements</span></span>



| <span data-ttu-id="395cd-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="395cd-119">Requirement</span></span> | <span data-ttu-id="395cd-120">Valore</span><span class="sxs-lookup"><span data-stu-id="395cd-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="395cd-121">Versione</span><span class="sxs-lookup"><span data-stu-id="395cd-121">Version</span></span><br/> | <span data-ttu-id="395cd-122">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="395cd-122">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="395cd-123">DLL</span><span class="sxs-lookup"><span data-stu-id="395cd-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="395cd-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="395cd-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="395cd-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="395cd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="395cd-126">**Oggetto esterno per i negozi di tipo 1 online**</span><span class="sxs-lookup"><span data-stu-id="395cd-126">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





