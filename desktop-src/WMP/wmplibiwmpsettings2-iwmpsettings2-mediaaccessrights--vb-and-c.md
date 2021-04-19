---
title: Proprietà mediaAccessRights di IWMPSettings2
description: La proprietà mediaAccessRights ottiene un valore che indica le autorizzazioni attualmente concesse per l'accesso alla libreria.
ms.assetid: c4289a2c-e343-405d-9bf5-0e97f6617916
keywords:
- Finestra delle proprietà di mediaAccessRights Media Player
- Proprietà di mediaAccessRights Media Player Windows, interfaccia IWMPSettings2
- Interfaccia IWMPSettings2 Windows Media Player, proprietà mediaAccessRights
topic_type:
- apiref
api_name:
- IWMPSettings2.mediaAccessRights
- IWMPSettings2.get_mediaAccessRights
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96cca06b9618767e7748b4b1308ed97860c7c80b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324065"
---
# <a name="iwmpsettings2mediaaccessrights-property"></a><span data-ttu-id="84bad-106">Proprietà IWMPSettings2:: mediaAccessRights</span><span class="sxs-lookup"><span data-stu-id="84bad-106">IWMPSettings2::mediaAccessRights property</span></span>

<span data-ttu-id="84bad-107">La proprietà **mediaAccessRights** ottiene un valore che indica le autorizzazioni attualmente concesse per l'accesso alla libreria.</span><span class="sxs-lookup"><span data-stu-id="84bad-107">The **mediaAccessRights** property gets a value indicating the permissions currently granted for library access.</span></span>

<span data-ttu-id="84bad-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="84bad-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="84bad-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="84bad-109">Syntax</span></span>


```CSharp
public System.String mediaAccessRights {get;}
```


```VB

Public ReadOnly Property mediaAccessRights As System.String
```





## <a name="property-value"></a><span data-ttu-id="84bad-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="84bad-110">Property value</span></span>

<span data-ttu-id="84bad-111">**System. String** che corrisponde a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="84bad-111">A **System.String** that is one of the following values.</span></span>



| <span data-ttu-id="84bad-112">Valore</span><span class="sxs-lookup"><span data-stu-id="84bad-112">Value</span></span> | <span data-ttu-id="84bad-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="84bad-113">Description</span></span>                      |
|-------|----------------------------------|
| <span data-ttu-id="84bad-114">Nessuno</span><span class="sxs-lookup"><span data-stu-id="84bad-114">none</span></span>  | <span data-ttu-id="84bad-115">Solo diritti di accesso agli elementi correnti.</span><span class="sxs-lookup"><span data-stu-id="84bad-115">Current item access rights only.</span></span> |
| <span data-ttu-id="84bad-116">lettura</span><span class="sxs-lookup"><span data-stu-id="84bad-116">read</span></span>  | <span data-ttu-id="84bad-117">Solo diritti di accesso in lettura.</span><span class="sxs-lookup"><span data-stu-id="84bad-117">Read access rights only.</span></span>         |
| <span data-ttu-id="84bad-118">completi</span><span class="sxs-lookup"><span data-stu-id="84bad-118">full</span></span>  | <span data-ttu-id="84bad-119">Diritti di accesso in lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="84bad-119">Read/Write access rights.</span></span>        |



 

## <a name="remarks"></a><span data-ttu-id="84bad-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="84bad-120">Remarks</span></span>

<span data-ttu-id="84bad-121">Una pagina Web deve prima richiedere all'utente l'autorizzazione per la lettura o la scrittura di dati nella libreria.</span><span class="sxs-lookup"><span data-stu-id="84bad-121">A webpage must first request permission from the user to read information from or write data to the library.</span></span> <span data-ttu-id="84bad-122">Ciò significa che determinati metodi, proprietà ed eventi saranno inaccessibili dal codice se non sono stati concessi i diritti di accesso appropriati.</span><span class="sxs-lookup"><span data-stu-id="84bad-122">This means that certain methods, properties, and events will be inaccessible from code if the appropriate access rights have not been granted.</span></span> <span data-ttu-id="84bad-123">Per ottenere i diritti di accesso, l'applicazione chiama **IWMPSettings2. Get \_ requestMediaAccessRights**, passando un parametro che specifica il livello di diritti di accesso desiderato.</span><span class="sxs-lookup"><span data-stu-id="84bad-123">To obtain access rights, the application calls **IWMPSettings2.get\_requestMediaAccessRights**, passing a parameter that specifies the desired access rights level.</span></span>

<span data-ttu-id="84bad-124">Le applicazioni in esecuzione nel computer dell'utente dispongono sempre dei diritti di accesso completi.</span><span class="sxs-lookup"><span data-stu-id="84bad-124">Applications running on the user's computer always have full access rights.</span></span>

## <a name="requirements"></a><span data-ttu-id="84bad-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="84bad-125">Requirements</span></span>



| <span data-ttu-id="84bad-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="84bad-126">Requirement</span></span> | <span data-ttu-id="84bad-127">Valore</span><span class="sxs-lookup"><span data-stu-id="84bad-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84bad-128">Versione</span><span class="sxs-lookup"><span data-stu-id="84bad-128">Version</span></span><br/>   | <span data-ttu-id="84bad-129">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="84bad-129">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="84bad-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="84bad-130">Namespace</span></span><br/> | <span data-ttu-id="84bad-131">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="84bad-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="84bad-132">Assembly</span><span class="sxs-lookup"><span data-stu-id="84bad-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="84bad-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="84bad-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84bad-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="84bad-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84bad-135">**Interfaccia IWMPSettings2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="84bad-135">**IWMPSettings2 Interface (VB and C#)**</span></span>](iwmpsettings2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="84bad-136">**IWMPSettings2. requestMediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="84bad-136">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





