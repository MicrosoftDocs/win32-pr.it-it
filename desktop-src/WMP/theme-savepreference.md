---
title: THEME. savePreference
description: Il metodo savePreference salva una preferenza nel registro di sistema.
ms.assetid: 4c253d8d-15c0-4c18-bb3f-fdbcef79c999
keywords:
- THEME. savePreference Windows Media Player
topic_type:
- apiref
api_name:
- THEME.savePreference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89633d71dd75f4ef5e804aefddc85cf00ad5c03b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331368"
---
# <a name="themesavepreference"></a><span data-ttu-id="ee0ac-104">THEME. savePreference</span><span class="sxs-lookup"><span data-stu-id="ee0ac-104">THEME.savePreference</span></span>

<span data-ttu-id="ee0ac-105">Il metodo **savePreference** salva una preferenza nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="ee0ac-105">The **savePreference** method saves a preference in the registry.</span></span>

``` syntax
        theme.savePreference(theKey, theValue)
```

## <a name="parameters"></a><span data-ttu-id="ee0ac-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ee0ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee0ac-107"><span id="theKey"></span><span id="thekey"></span><span id="THEKEY"></span>*theKey*</span><span class="sxs-lookup"><span data-stu-id="ee0ac-107"><span id="theKey"></span><span id="thekey"></span><span id="THEKEY"></span>*theKey*</span></span>
</dt> <dd>

<span data-ttu-id="ee0ac-108">**Stringa** che specifica la chiave del valore di preferenza da salvare.</span><span class="sxs-lookup"><span data-stu-id="ee0ac-108">A **String** specifying the key of the preference value to save.</span></span>

</dd> <dt>

<span data-ttu-id="ee0ac-109"><span id="theValue"></span><span id="thevalue"></span><span id="THEVALUE"></span>*Ilvalore*</span><span class="sxs-lookup"><span data-stu-id="ee0ac-109"><span id="theValue"></span><span id="thevalue"></span><span id="THEVALUE"></span>*theValue*</span></span>
</dt> <dd>

<span data-ttu-id="ee0ac-110">**Stringa** che specifica il valore da salvare.</span><span class="sxs-lookup"><span data-stu-id="ee0ac-110">A **String** specifying the value to save.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee0ac-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ee0ac-111">Return Value</span></span>

<span data-ttu-id="ee0ac-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="ee0ac-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee0ac-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="ee0ac-113">Remarks</span></span>

<span data-ttu-id="ee0ac-114">Una preferenza è una coppia chiave/valore che può essere archiviata nel registro di sistema per mantenere le informazioni sullo stato delle Media Player di Windows tra le esecuzioni.</span><span class="sxs-lookup"><span data-stu-id="ee0ac-114">A preference is a key/value pair that can be stored in the registry to retain information about the state of Windows Media Player between runs.</span></span> <span data-ttu-id="ee0ac-115">Questa funzionalità può essere usata, ad esempio, per salvare le impostazioni di personalizzazione in modo che non debbano essere immesse di nuovo ogni volta che viene avviato Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="ee0ac-115">This feature can be used, for example, to save customization settings so that they won't have to be re-entered each time Windows Media Player is started.</span></span>

<span data-ttu-id="ee0ac-116">Le preferenze non sono crittografate e pertanto non sono un metodo sicuro per rendere permanente i dati.</span><span class="sxs-lookup"><span data-stu-id="ee0ac-116">Preferences are not encrypted and therefore are not a secure method for persisting data.</span></span> <span data-ttu-id="ee0ac-117">Non usare le preferenze per archiviare i dati privati.</span><span class="sxs-lookup"><span data-stu-id="ee0ac-117">Do not use preferences to store private data.</span></span>

## <a name="examples"></a><span data-ttu-id="ee0ac-118">Esempio</span><span class="sxs-lookup"><span data-stu-id="ee0ac-118">Examples</span></span>


```JScript
<THEME>
  <VIEW 
    id="View1" 
    onclose="jscript:theme.savePreference('drawer1','open');
             theme.savePreference('drawer2','close')">
  </VIEW>
</THEME>
```



## <a name="requirements"></a><span data-ttu-id="ee0ac-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ee0ac-119">Requirements</span></span>



| <span data-ttu-id="ee0ac-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee0ac-120">Requirement</span></span> | <span data-ttu-id="ee0ac-121">Valore</span><span class="sxs-lookup"><span data-stu-id="ee0ac-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="ee0ac-122">Versione</span><span class="sxs-lookup"><span data-stu-id="ee0ac-122">Version</span></span><br/> | <span data-ttu-id="ee0ac-123">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="ee0ac-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ee0ac-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ee0ac-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee0ac-125">**Elemento THEME**</span><span class="sxs-lookup"><span data-stu-id="ee0ac-125">**THEME Element**</span></span>](theme-element.md)
</dt> <dt>

[<span data-ttu-id="ee0ac-126">**THEME. loadPreference**</span><span class="sxs-lookup"><span data-stu-id="ee0ac-126">**THEME.loadPreference**</span></span>](theme-loadpreference.md)
</dt> </dl>

 

 





