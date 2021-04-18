---
title: THEME. loadPreference
description: Il metodo loadPreference carica una preferenza dal registro di sistema.
ms.assetid: 51d6b0f8-f1fd-4999-a575-0b7c177b2bc8
keywords:
- THEME. loadPreference Windows Media Player
topic_type:
- apiref
api_name:
- THEME.loadPreference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d92135113495ac32ca81f602ea5836332159164c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333827"
---
# <a name="themeloadpreference"></a><span data-ttu-id="eabe5-104">THEME. loadPreference</span><span class="sxs-lookup"><span data-stu-id="eabe5-104">THEME.loadPreference</span></span>

<span data-ttu-id="eabe5-105">Il metodo **loadPreference** carica una preferenza dal registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="eabe5-105">The **loadPreference** method loads a preference from the registry.</span></span>

``` syntax
        theme.loadPreference(theKey)
```

## <a name="parameters"></a><span data-ttu-id="eabe5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="eabe5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eabe5-107"><span id="theKey"></span><span id="thekey"></span><span id="THEKEY"></span>*theKey*</span><span class="sxs-lookup"><span data-stu-id="eabe5-107"><span id="theKey"></span><span id="thekey"></span><span id="THEKEY"></span>*theKey*</span></span>
</dt> <dd>

<span data-ttu-id="eabe5-108">**Stringa** che specifica la chiave del valore di preferenza da caricare.</span><span class="sxs-lookup"><span data-stu-id="eabe5-108">A **String** specifying the key of the preference value to load.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eabe5-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eabe5-109">Return Value</span></span>

<span data-ttu-id="eabe5-110">Questo metodo restituisce una **stringa**.</span><span class="sxs-lookup"><span data-stu-id="eabe5-110">This method returns a **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="eabe5-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="eabe5-111">Remarks</span></span>

<span data-ttu-id="eabe5-112">Una preferenza è una coppia chiave/valore che può essere archiviata nel registro di sistema per mantenere le informazioni sullo stato del Media Player di Windows tra le esecuzioni.</span><span class="sxs-lookup"><span data-stu-id="eabe5-112">A preference is a key/value pair that can be stored in the registry to retain information about the state of the Windows Media Player between runs.</span></span> <span data-ttu-id="eabe5-113">Questa funzionalità può essere usata, ad esempio, per salvare le impostazioni di personalizzazione in modo che non debbano essere immesse di nuovo ogni volta che viene avviato Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="eabe5-113">This feature can be used, for example, to save customization settings so that they won't have to be re-entered each time Windows Media Player is started.</span></span>

<span data-ttu-id="eabe5-114">Le preferenze non sono crittografate e pertanto non sono un metodo sicuro per rendere permanente i dati.</span><span class="sxs-lookup"><span data-stu-id="eabe5-114">Preferences are not encrypted and therefore are not a secure method for persisting data.</span></span> <span data-ttu-id="eabe5-115">Non usare le preferenze per archiviare i dati privati.</span><span class="sxs-lookup"><span data-stu-id="eabe5-115">Do not use preferences to store private data.</span></span>

## <a name="requirements"></a><span data-ttu-id="eabe5-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eabe5-116">Requirements</span></span>



| <span data-ttu-id="eabe5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="eabe5-117">Requirement</span></span> | <span data-ttu-id="eabe5-118">Valore</span><span class="sxs-lookup"><span data-stu-id="eabe5-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="eabe5-119">Versione</span><span class="sxs-lookup"><span data-stu-id="eabe5-119">Version</span></span><br/> | <span data-ttu-id="eabe5-120">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="eabe5-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="eabe5-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eabe5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eabe5-122">**Elemento THEME**</span><span class="sxs-lookup"><span data-stu-id="eabe5-122">**THEME Element**</span></span>](theme-element.md)
</dt> <dt>

[<span data-ttu-id="eabe5-123">**THEME. savePreference**</span><span class="sxs-lookup"><span data-stu-id="eabe5-123">**THEME.savePreference**</span></span>](theme-savepreference.md)
</dt> </dl>

 

 





