---
title: Settings. requestMediaAccessRights, metodo
description: Il metodo requestMediaAccessRights richiede un livello specificato di accesso alla libreria. | Settings. requestMediaAccessRights, metodo
ms.assetid: 076b749b-9b25-483c-aa1f-60fc4367e4e0
keywords:
- Metodo requestMediaAccessRights Windows Media Player
- Metodo requestMediaAccessRights Media Player Windows, classe Settings
- Classe Settings Media Player Windows, metodo requestMediaAccessRights
topic_type:
- apiref
api_name:
- Settings.requestMediaAccessRights
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abfeed45666ee1f63bf995b211030b0b840c4279
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327370"
---
# <a name="settingsrequestmediaaccessrights-method"></a><span data-ttu-id="e51af-107">Settings. requestMediaAccessRights, metodo</span><span class="sxs-lookup"><span data-stu-id="e51af-107">Settings.requestMediaAccessRights method</span></span>

<span data-ttu-id="e51af-108">Il metodo **requestMediaAccessRights** richiede un livello specificato di accesso alla libreria.</span><span class="sxs-lookup"><span data-stu-id="e51af-108">The **requestMediaAccessRights** method requests a specified level of access to the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="e51af-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e51af-109">Syntax</span></span>


```JScript
bRetVal = Settings.requestMediaAccessRights(
  access
)
```



## <a name="parameters"></a><span data-ttu-id="e51af-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="e51af-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e51af-111">*accesso* \[ a in\]</span><span class="sxs-lookup"><span data-stu-id="e51af-111">*access* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e51af-112">**Stringa** che specifica il livello di diritti di accesso desiderato.</span><span class="sxs-lookup"><span data-stu-id="e51af-112">**String** specifying the desired access rights level.</span></span> <span data-ttu-id="e51af-113">Contiene uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="e51af-113">Contains one of the following values.</span></span>



| <span data-ttu-id="e51af-114">string</span><span class="sxs-lookup"><span data-stu-id="e51af-114">String</span></span> | <span data-ttu-id="e51af-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e51af-115">Description</span></span>                      |
|--------|----------------------------------|
| <span data-ttu-id="e51af-116">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e51af-116">none</span></span>   | <span data-ttu-id="e51af-117">Solo diritti di accesso agli elementi correnti.</span><span class="sxs-lookup"><span data-stu-id="e51af-117">Current item access rights only.</span></span> |
| <span data-ttu-id="e51af-118">lettura</span><span class="sxs-lookup"><span data-stu-id="e51af-118">read</span></span>   | <span data-ttu-id="e51af-119">Solo diritti di accesso in lettura.</span><span class="sxs-lookup"><span data-stu-id="e51af-119">Read access rights only.</span></span>         |
| <span data-ttu-id="e51af-120">completi</span><span class="sxs-lookup"><span data-stu-id="e51af-120">full</span></span>   | <span data-ttu-id="e51af-121">Diritti di accesso in lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="e51af-121">Read/Write access rights.</span></span>        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e51af-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e51af-122">Return value</span></span>

<span data-ttu-id="e51af-123">Questo metodo restituisce un valore **booleano** che indica se sono stati concessi i diritti di accesso richiesti.</span><span class="sxs-lookup"><span data-stu-id="e51af-123">This method returns a **Boolean** value indicating whether the requested access rights were granted.</span></span>

## <a name="remarks"></a><span data-ttu-id="e51af-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="e51af-124">Remarks</span></span>

<span data-ttu-id="e51af-125">Una pagina Web deve prima richiedere all'utente l'autorizzazione per la lettura o la scrittura di dati nella libreria.</span><span class="sxs-lookup"><span data-stu-id="e51af-125">A webpage must first request permission from the user to read information from or write data to the library.</span></span> <span data-ttu-id="e51af-126">La chiamata di questo metodo richiede all'utente una finestra di dialogo che richiede il livello di autorizzazione specificato.</span><span class="sxs-lookup"><span data-stu-id="e51af-126">Invoking this method prompts the user with a dialog box that requests the specified permission level.</span></span> <span data-ttu-id="e51af-127">Ciò significa che determinati metodi, proprietà ed eventi saranno inaccessibili dal codice se non sono stati concessi i diritti di accesso appropriati.</span><span class="sxs-lookup"><span data-stu-id="e51af-127">This means that certain methods, properties, and events will be inaccessible from code if the appropriate access rights have not been granted.</span></span> <span data-ttu-id="e51af-128">Il livello dei diritti di accesso corrente può essere recuperato usando *le impostazioni*. **mediaAccessRights**.</span><span class="sxs-lookup"><span data-stu-id="e51af-128">The current access rights level can be retrieved using *Settings*.**mediaAccessRights**.</span></span>

<span data-ttu-id="e51af-129">**Windows Media Player 10 Mobile**: questo metodo restituisce sempre **true**.</span><span class="sxs-lookup"><span data-stu-id="e51af-129">**Windows Media Player 10 Mobile**: This method always returns **true**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e51af-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e51af-130">Requirements</span></span>



| <span data-ttu-id="e51af-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="e51af-131">Requirement</span></span> | <span data-ttu-id="e51af-132">Valore</span><span class="sxs-lookup"><span data-stu-id="e51af-132">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e51af-133">Versione</span><span class="sxs-lookup"><span data-stu-id="e51af-133">Version</span></span><br/> | <span data-ttu-id="e51af-134">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="e51af-134">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="e51af-135">DLL</span><span class="sxs-lookup"><span data-stu-id="e51af-135">DLL</span></span><br/>     | <dl> <span data-ttu-id="e51af-136"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e51af-136"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e51af-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e51af-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e51af-138">**Oggetto Settings**</span><span class="sxs-lookup"><span data-stu-id="e51af-138">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="e51af-139">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="e51af-139">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> </dl>

 

 





