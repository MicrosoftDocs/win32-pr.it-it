---
title: Metodo IWMPSettings2 requestMediaAccessRights
description: Il metodo requestMediaAccessRights richiede un livello specificato di accesso alla libreria. | Metodo IWMPSettings2 requestMediaAccessRights
ms.assetid: ea33852c-d1e0-45cf-8954-2a1e2fe51910
keywords:
- Metodo requestMediaAccessRights Windows Media Player
- Metodo requestMediaAccessRights Windows Media Player, interfaccia IWMPSettings2
- Interfaccia IWMPSettings2 Windows Media Player, metodo requestMediaAccessRights
topic_type:
- apiref
api_name:
- IWMPSettings2.requestMediaAccessRights
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c609afffc1d9b228d908d905e0eb1a6ef8741032
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328195"
---
# <a name="iwmpsettings2requestmediaaccessrights-method"></a><span data-ttu-id="82578-107">Metodo IWMPSettings2:: requestMediaAccessRights</span><span class="sxs-lookup"><span data-stu-id="82578-107">IWMPSettings2::requestMediaAccessRights method</span></span>

<span data-ttu-id="82578-108">Il metodo **requestMediaAccessRights** richiede un livello specificato di accesso alla libreria.</span><span class="sxs-lookup"><span data-stu-id="82578-108">The **requestMediaAccessRights** method requests a specified level of access to the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="82578-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="82578-109">Syntax</span></span>


```CSharp
public System.Boolean requestMediaAccessRights(
  System.String bstrDesiredAccess
);
```


```VB

Public Function requestMediaAccessRights( _
  ByVal bstrDesiredAccess As System.String _
) As System.Boolean
Implements IWMPSettings2.requestMediaAccessRights
```





## <a name="parameters"></a><span data-ttu-id="82578-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="82578-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82578-111">*bstrDesiredAccess* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="82578-111">*bstrDesiredAccess* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82578-112">**System. String** che corrisponde a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="82578-112">A **System.String** that is one of the following values.</span></span>



| <span data-ttu-id="82578-113">Valore</span><span class="sxs-lookup"><span data-stu-id="82578-113">Value</span></span> | <span data-ttu-id="82578-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="82578-114">Description</span></span>                      |
|-------|----------------------------------|
| <span data-ttu-id="82578-115">Nessuno</span><span class="sxs-lookup"><span data-stu-id="82578-115">none</span></span>  | <span data-ttu-id="82578-116">Solo diritti di accesso agli elementi correnti.</span><span class="sxs-lookup"><span data-stu-id="82578-116">Current item access rights only.</span></span> |
| <span data-ttu-id="82578-117">lettura</span><span class="sxs-lookup"><span data-stu-id="82578-117">read</span></span>  | <span data-ttu-id="82578-118">Solo diritti di accesso in lettura.</span><span class="sxs-lookup"><span data-stu-id="82578-118">Read access rights only.</span></span>         |
| <span data-ttu-id="82578-119">completi</span><span class="sxs-lookup"><span data-stu-id="82578-119">full</span></span>  | <span data-ttu-id="82578-120">Diritti di accesso in lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="82578-120">Read/Write access rights.</span></span>        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82578-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="82578-121">Return value</span></span>

<span data-ttu-id="82578-122">**System. Boolean** che indica se sono stati concessi i diritti di accesso richiesti.</span><span class="sxs-lookup"><span data-stu-id="82578-122">A **System.Boolean** that indicates whether the requested access rights were granted.</span></span>

## <a name="remarks"></a><span data-ttu-id="82578-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="82578-123">Remarks</span></span>

<span data-ttu-id="82578-124">Una pagina Web deve prima richiedere all'utente l'autorizzazione per la lettura o la scrittura di dati nella libreria.</span><span class="sxs-lookup"><span data-stu-id="82578-124">A webpage must first request permission from the user to read information from or write data to the library.</span></span> <span data-ttu-id="82578-125">La chiamata di questo metodo richiede all'utente una finestra di dialogo che richiede il livello di autorizzazione specificato.</span><span class="sxs-lookup"><span data-stu-id="82578-125">Invoking this method prompts the user with a dialog box that requests the specified permission level.</span></span> <span data-ttu-id="82578-126">Ciò significa che determinati metodi, proprietà ed eventi saranno inaccessibili dal codice se non sono stati concessi i diritti di accesso appropriati.</span><span class="sxs-lookup"><span data-stu-id="82578-126">This means that certain methods, properties, and events will be inaccessible from code if the appropriate access rights have not been granted.</span></span> <span data-ttu-id="82578-127">Il livello dei diritti di accesso corrente può essere recuperato tramite **IWMPSettings2. mediaAccessRights**.</span><span class="sxs-lookup"><span data-stu-id="82578-127">The current access rights level can be retrieved by using **IWMPSettings2.mediaAccessRights**.</span></span>

<span data-ttu-id="82578-128">Per le applicazioni in esecuzione nel computer dell'utente non è necessario usare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="82578-128">Applications running on the user's computer are not required to use this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="82578-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="82578-129">Requirements</span></span>



| <span data-ttu-id="82578-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="82578-130">Requirement</span></span> | <span data-ttu-id="82578-131">Valore</span><span class="sxs-lookup"><span data-stu-id="82578-131">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82578-132">Versione</span><span class="sxs-lookup"><span data-stu-id="82578-132">Version</span></span><br/>   | <span data-ttu-id="82578-133">Windows Media Player 9 serie o versione successiva</span><span class="sxs-lookup"><span data-stu-id="82578-133">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="82578-134">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="82578-134">Namespace</span></span><br/> | <span data-ttu-id="82578-135">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="82578-135">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="82578-136">Assembly</span><span class="sxs-lookup"><span data-stu-id="82578-136">Assembly</span></span><br/>  | <dl> <span data-ttu-id="82578-137"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="82578-137"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82578-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="82578-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82578-139">**Interfaccia IWMPSettings2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="82578-139">**IWMPSettings2 Interface (VB and C#)**</span></span>](iwmpsettings2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="82578-140">**IWMPSettings2. mediaAccessRights (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="82578-140">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





