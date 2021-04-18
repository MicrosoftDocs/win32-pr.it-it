---
description: Crea un nuovo elemento figlio. Aggiunge oggetti IWiaItem2 all'albero IWiaItem2 di un dispositivo.
ms.assetid: 525ee788-3ff4-4def-ae71-4a405c04c6a3
title: 'Metodo IWiaItem2:: CreateChildItem (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.CreateChildItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 0002a6110894491a8d6efabb5a142b7c81adc820
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312394"
---
# <a name="iwiaitem2createchilditem-method"></a><span data-ttu-id="5b94e-104">Metodo IWiaItem2:: CreateChildItem</span><span class="sxs-lookup"><span data-stu-id="5b94e-104">IWiaItem2::CreateChildItem method</span></span>

<span data-ttu-id="5b94e-105">Crea un nuovo elemento figlio.</span><span class="sxs-lookup"><span data-stu-id="5b94e-105">Create a new child item.</span></span> <span data-ttu-id="5b94e-106">Aggiunge oggetti [**IWiaItem2**](-wia-iwiaitem2.md) all'albero **IWiaItem2** di un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5b94e-106">Adds [**IWiaItem2**](-wia-iwiaitem2.md) objects to a device's **IWiaItem2** tree.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b94e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5b94e-107">Syntax</span></span>


```C++
HRESULT CreateChildItem(
  [in]  LONG      lItemFlags,
  [in]  LONG      lCreationFlags,
  [in]  BSTR      bstrItemName,
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="5b94e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="5b94e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b94e-109">*lItemFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b94e-109">*lItemFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b94e-110">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="5b94e-110">Type: **LONG**</span></span>

<span data-ttu-id="5b94e-111">Specifica il tipo di elemento WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="5b94e-111">Specifies the WIA 2.0 item type.</span></span> <span data-ttu-id="5b94e-112">Vedere i [**flag del tipo di elemento WIA**](-wia-wia-item-type-flags.md).</span><span class="sxs-lookup"><span data-stu-id="5b94e-112">See [**WIA Item Type Flags**](-wia-wia-item-type-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="5b94e-113">*lCreationFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b94e-113">*lCreationFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b94e-114">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="5b94e-114">Type: **LONG**</span></span>

<span data-ttu-id="5b94e-115">Specifica come creare il nuovo elemento.</span><span class="sxs-lookup"><span data-stu-id="5b94e-115">Specifies how to create the new item.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="5b94e-116"><span id="0"></span>**0** (0)</span><span class="sxs-lookup"><span data-stu-id="5b94e-116"><span id="0"></span>**0** (0)</span></span>


</dt> <dd>

<span data-ttu-id="5b94e-117">Impostare i valori predefiniti per le proprietà dell'elemento figlio.</span><span class="sxs-lookup"><span data-stu-id="5b94e-117">Set the default values for the properties of the child.</span></span>

</dd> <dt>

<span id="COPY_PARENT_PROPERTY_VALUES"></span><span id="copy_parent_property_values"></span>

<span data-ttu-id="5b94e-118"><span id="COPY_PARENT_PROPERTY_VALUES"></span><span id="copy_parent_property_values"></span>**Copia \_ di \_ \_ Valori delle proprietà padre** (0x40000000)</span><span class="sxs-lookup"><span data-stu-id="5b94e-118"><span id="COPY_PARENT_PROPERTY_VALUES"></span><span id="copy_parent_property_values"></span>**COPY\_PARENT\_PROPERTY\_VALUES** (0x40000000)</span></span>


</dt> <dd>

<span data-ttu-id="5b94e-119">Copiare i valori di tutte le proprietà di lettura/scrittura dall'elemento padre.</span><span class="sxs-lookup"><span data-stu-id="5b94e-119">Copy the values of all Read/Write properties from the parent.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="5b94e-120">*bstrItemName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5b94e-120">*bstrItemName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b94e-121">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="5b94e-121">Type: **BSTR**</span></span>

<span data-ttu-id="5b94e-122">Specifica il nome dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="5b94e-122">Specifies the item name.</span></span> <span data-ttu-id="5b94e-123">Questo nome viene aggiunto alla fine del nome dell'elemento padre per generare il nome completo dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="5b94e-123">This name is appended to the end of the parent item's name to generate the full item name.</span></span>

</dd> <dt>

<span data-ttu-id="5b94e-124">*ppIWiaItem2* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5b94e-124">*ppIWiaItem2* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b94e-125">Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="5b94e-125">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="5b94e-126">Riceve l'indirizzo di un puntatore all'interfaccia [**IWiaItem2**](-wia-iwiaitem2.md) che imposta il metodo **IWiaItem2:: CreateChildItem** .</span><span class="sxs-lookup"><span data-stu-id="5b94e-126">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface that sets the **IWiaItem2::CreateChildItem** method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b94e-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5b94e-127">Return value</span></span>

<span data-ttu-id="5b94e-128">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="5b94e-128">Type: **HRESULT**</span></span>

<span data-ttu-id="5b94e-129">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5b94e-129">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5b94e-130">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5b94e-130">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b94e-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="5b94e-131">Remarks</span></span>

<span data-ttu-id="5b94e-132">Alcuni dispositivi hardware WIA 2,0 consentono alle applicazioni di creare nuovi elementi nell'albero [**IWiaItem2**](-wia-iwiaitem2.md) che rappresenta il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5b94e-132">Some WIA 2.0 hardware devices allow applications to create new items in the [**IWiaItem2**](-wia-iwiaitem2.md) tree that represents the device.</span></span> <span data-ttu-id="5b94e-133">Le applicazioni devono testare i dispositivi per verificare se supportano questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="5b94e-133">Applications must test the devices to see if they support this capability.</span></span> <span data-ttu-id="5b94e-134">Usare l' \_ interfaccia IEnumWIA dev \_ Caps per enumerare le funzionalità del dispositivo corrente.</span><span class="sxs-lookup"><span data-stu-id="5b94e-134">Use the IEnumWIA\_DEV\_CAPS interface to enumerate the current device's capabilities.</span></span>

<span data-ttu-id="5b94e-135">Se il dispositivo consente la creazione di nuovi elementi nell'albero [**IWiaItem2**](-wia-iwiaitem2.md) , la chiamata a **IWiaItem2:: CreateChildItem** crea un nuovo oggetto **IWiaItem2** che è figlio del nodo corrente.</span><span class="sxs-lookup"><span data-stu-id="5b94e-135">If the device allows the creation of new items in the [**IWiaItem2**](-wia-iwiaitem2.md) tree, invoking **IWiaItem2::CreateChildItem** creates a new **IWiaItem2** object that is a child of the current node.</span></span> <span data-ttu-id="5b94e-136">Passa un puntatore al nuovo nodo all'applicazione tramite il parametro *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="5b94e-136">It passes a pointer to the new node to the application through the *ppIWiaItem2* parameter.</span></span> <span data-ttu-id="5b94e-137">Le applicazioni devono chiamare il metodo [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sui puntatori di interfaccia ricevuti tramite il parametro *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="5b94e-137">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIWiaItem2* parameter.</span></span>

<span data-ttu-id="5b94e-138">Se *lCreationFlags* è \_ la copia \_ dei valori della proprietà padre \_ e *lItemFlags* è zero, la funzione restituisce e \_ INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="5b94e-138">If *lCreationFlags* is COPY\_PARENT\_PROPERTY\_VALUES and *lItemFlags* is zero, the function returns E\_INVALIDARG.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b94e-139">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5b94e-139">Requirements</span></span>



| <span data-ttu-id="5b94e-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b94e-140">Requirement</span></span> | <span data-ttu-id="5b94e-141">Valore</span><span class="sxs-lookup"><span data-stu-id="5b94e-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5b94e-142">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5b94e-142">Minimum supported client</span></span><br/> | <span data-ttu-id="5b94e-143">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5b94e-143">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5b94e-144">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5b94e-144">Minimum supported server</span></span><br/> | <span data-ttu-id="5b94e-145">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5b94e-145">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5b94e-146">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5b94e-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b94e-147"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b94e-147"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="5b94e-148">IDL</span><span class="sxs-lookup"><span data-stu-id="5b94e-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5b94e-149"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5b94e-149"><dt>Wia.idl</dt></span></span> </dl> |



 

 
