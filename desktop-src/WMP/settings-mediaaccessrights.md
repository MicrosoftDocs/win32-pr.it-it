---
title: Settings. mediaAccessRights
description: La proprietà mediaAccessRights recupera un valore che indica i diritti attualmente concessi per l'accesso alla libreria.
ms.assetid: 744e696d-29d2-44b1-a296-5b5d007b689f
keywords:
- Impostazioni. mediaAccessRights Windows Media Player
topic_type:
- apiref
api_name:
- Settings.mediaAccessRights
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36bcfb667a1aa09e84ae90324736291d421a3941
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327381"
---
# <a name="settingsmediaaccessrights"></a><span data-ttu-id="6600f-104">Settings. mediaAccessRights</span><span class="sxs-lookup"><span data-stu-id="6600f-104">Settings.mediaAccessRights</span></span>

<span data-ttu-id="6600f-105">La proprietà **mediaAccessRights** recupera un valore che indica i diritti attualmente concessi per l'accesso alla libreria.</span><span class="sxs-lookup"><span data-stu-id="6600f-105">The **mediaAccessRights** property retrieves a value indicating the rights currently granted for library access.</span></span>

## <a name="syntax"></a><span data-ttu-id="6600f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6600f-106">Syntax</span></span>

<span data-ttu-id="6600f-107">Player. Settings. mediaAccessRights</span><span class="sxs-lookup"><span data-stu-id="6600f-107">player.settings.mediaAccessRights</span></span>

## <a name="possible-values"></a><span data-ttu-id="6600f-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="6600f-108">Possible Values</span></span>

<span data-ttu-id="6600f-109">Questa proprietà è una **stringa** di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="6600f-109">This property is a read-only **String**.</span></span>



| <span data-ttu-id="6600f-110">Valore</span><span class="sxs-lookup"><span data-stu-id="6600f-110">Value</span></span> | <span data-ttu-id="6600f-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6600f-111">Description</span></span>                      |
|-------|----------------------------------|
| <span data-ttu-id="6600f-112">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6600f-112">none</span></span>  | <span data-ttu-id="6600f-113">Solo diritti di accesso agli elementi correnti.</span><span class="sxs-lookup"><span data-stu-id="6600f-113">Current item access rights only.</span></span> |
| <span data-ttu-id="6600f-114">lettura</span><span class="sxs-lookup"><span data-stu-id="6600f-114">read</span></span>  | <span data-ttu-id="6600f-115">Solo diritti di accesso in lettura.</span><span class="sxs-lookup"><span data-stu-id="6600f-115">Read access rights only.</span></span>         |
| <span data-ttu-id="6600f-116">completi</span><span class="sxs-lookup"><span data-stu-id="6600f-116">full</span></span>  | <span data-ttu-id="6600f-117">Diritti di accesso in lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="6600f-117">Read/Write access rights.</span></span>        |



 

## <a name="remarks"></a><span data-ttu-id="6600f-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="6600f-118">Remarks</span></span>

<span data-ttu-id="6600f-119">Una pagina Web deve prima richiedere all'utente l'autorizzazione per la lettura o la scrittura di dati nella libreria.</span><span class="sxs-lookup"><span data-stu-id="6600f-119">A webpage must first request permission from the user to read information from or write data to the library.</span></span> <span data-ttu-id="6600f-120">Ciò significa che determinati metodi, proprietà ed eventi saranno inaccessibili dal codice se non sono stati concessi i diritti di accesso appropriati.</span><span class="sxs-lookup"><span data-stu-id="6600f-120">This means that certain methods, properties, and events will be inaccessible from code if the appropriate access rights have not been granted.</span></span> <span data-ttu-id="6600f-121">Per ottenere i diritti di accesso, l'applicazione chiama *le impostazioni*. **requestMediaAccessRights**, passando un parametro che specifica il livello di diritti di accesso desiderato.</span><span class="sxs-lookup"><span data-stu-id="6600f-121">To obtain access rights, the application calls *Settings*.**requestMediaAccessRights**, passing a parameter that specifies the desired access rights level.</span></span>

<span data-ttu-id="6600f-122">**Windows Media Player 10 Mobile**: questa proprietà restituisce sempre **full**.</span><span class="sxs-lookup"><span data-stu-id="6600f-122">**Windows Media Player 10 Mobile**: This property always returns **full**.</span></span>

## <a name="requirements"></a><span data-ttu-id="6600f-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6600f-123">Requirements</span></span>



| <span data-ttu-id="6600f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="6600f-124">Requirement</span></span> | <span data-ttu-id="6600f-125">Valore</span><span class="sxs-lookup"><span data-stu-id="6600f-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6600f-126">Versione</span><span class="sxs-lookup"><span data-stu-id="6600f-126">Version</span></span><br/> | <span data-ttu-id="6600f-127">Windows Media Player 9 serie o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="6600f-127">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="6600f-128">DLL</span><span class="sxs-lookup"><span data-stu-id="6600f-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="6600f-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6600f-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6600f-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6600f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6600f-131">**Oggetto Settings**</span><span class="sxs-lookup"><span data-stu-id="6600f-131">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="6600f-132">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="6600f-132">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





