---
title: External. showPopup, metodo
description: Si noti che in questo argomento viene descritta la funzionalità progettata per l'utilizzo da punti vendita online. | External. showPopup, metodo
ms.assetid: 17958543-dbed-45a5-9b02-4800a07cb820
keywords:
- Metodo showPopup Windows Media Player
- Metodo showPopup Windows Media Player, classe esterna
- Classe esterna Media Player Windows, metodo showPopup
topic_type:
- apiref
api_name:
- External.showPopup
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acaecb559e7df60067e89ec754ec9432233500f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326008"
---
# <a name="externalshowpopup-method"></a><span data-ttu-id="21740-107">External. showPopup, metodo</span><span class="sxs-lookup"><span data-stu-id="21740-107">External.showPopup method</span></span>

> [!Note]  
> <span data-ttu-id="21740-108">Questo argomento descrive la funzionalità progettata per l'uso da punti vendita online.</span><span class="sxs-lookup"><span data-stu-id="21740-108">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="21740-109">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="21740-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="21740-110">Il metodo **ShowPopup** indica a Windows Media Player di visualizzare una pagina Web popup. ovvero una pagina Web visualizzata in una finestra separata.</span><span class="sxs-lookup"><span data-stu-id="21740-110">The **showPopup** method instructs Windows Media Player to display a pop-up webpage; that is, a webpage that appears in a separate window.</span></span>

## <a name="syntax"></a><span data-ttu-id="21740-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="21740-111">Syntax</span></span>


```JScript
External.showPopup(
  PopupIndex,
  Parameters
)
```



## <a name="parameters"></a><span data-ttu-id="21740-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="21740-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21740-113">*PopupIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="21740-113">*PopupIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21740-114">**Numero** (**Long**) che specifica l'indice della pagina Web popup.</span><span class="sxs-lookup"><span data-stu-id="21740-114">**Number** (**long**) that specifies the index of the pop-up webpage.</span></span>

</dd> <dt>

<span data-ttu-id="21740-115">*Parametri* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="21740-115">*Parameters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21740-116">**Stringa** che Windows Media Player aggiunge all'URL della pagina Web.</span><span class="sxs-lookup"><span data-stu-id="21740-116">**String** that Windows Media Player appends to the URL of the webpage.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21740-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="21740-117">Return value</span></span>

<span data-ttu-id="21740-118">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="21740-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="21740-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="21740-119">Remarks</span></span>

<span data-ttu-id="21740-120">L'indice popup non è interpretato da Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="21740-120">The pop-up index is not interpreted by Windows Media Player.</span></span> <span data-ttu-id="21740-121">Gli indici che identificano le pagine Web popup vengono creati dallo Store online e hanno un significato solo per lo Store online.</span><span class="sxs-lookup"><span data-stu-id="21740-121">Indexes that identify pop-up webpages are created by the online store, and have meaning only to the online store.</span></span>

<span data-ttu-id="21740-122">Nei passaggi seguenti viene illustrato il modo in cui Windows Media Player utilizza i parametri del metodo **ShowPopup** per creare un URL per la finestra popup.</span><span class="sxs-lookup"><span data-stu-id="21740-122">The following steps show how Windows Media Player uses the parameters of the **showPopup** method to create a URL for the popup window.</span></span>

1.  <span data-ttu-id="21740-123">Script in una pagina di individuazione chiama **ShowPopup**, passando un Integer in *PopupIndex* e una stringa in *Parameters*.</span><span class="sxs-lookup"><span data-stu-id="21740-123">Script on a discovery page calls **showPopup**, passing an integer in *PopupIndex* and a string in *Parameters*.</span></span>

2.  <span data-ttu-id="21740-124">Windows Media Player passa l'indice a [IWMPContentPartner:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) per recuperare l'URL della pagina Web da visualizzare.</span><span class="sxs-lookup"><span data-stu-id="21740-124">Windows Media Player passes the index to [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) to retrieve the URL of the webpage to be displayed.</span></span>

3.  <span data-ttu-id="21740-125">Windows Media Player aggiunge i *parametri* all'URL come stringa di query.</span><span class="sxs-lookup"><span data-stu-id="21740-125">Windows Media Player appends *Parameters* to the URL as a query string.</span></span> <span data-ttu-id="21740-126">Se, ad esempio, **GetItemInfo** restituisce " https://www.Proseware.com/Pages/Popup1.htm " e *Parameters* è uguale a "DlgX = 800&DlgY = 400&Greeting = Hi", Windows Media Player crea l'URL seguente:</span><span class="sxs-lookup"><span data-stu-id="21740-126">For example, if **GetItemInfo** returns "https://www.Proseware.com/Pages/Popup1.htm" and *Parameters* is equal to "DlgX=800&DlgY=400&Greeting=Hi", Windows Media Player creates the following URL:</span></span>

    https://www.Proseware.com/Pages/Popup1.htm?DlgX=800&DlgY=400&Greeting=Hi

<span data-ttu-id="21740-127">È possibile usare i *parametri* per specificare le dimensioni della finestra popup.</span><span class="sxs-lookup"><span data-stu-id="21740-127">You can use *Parameters* to specify the size of the pop-up window.</span></span> <span data-ttu-id="21740-128">Se ad esempio si impostano i *parametri* su "DlgX = 800&DlgY = 400", la finestra popup avrà una dimensione di 800 pixel per 400 pixel.</span><span class="sxs-lookup"><span data-stu-id="21740-128">For example, if you set *Parameters* to "DlgX=800&DlgY=400", the pop-up window will have a size of 800 pixels by 400 pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="21740-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="21740-129">Requirements</span></span>



| <span data-ttu-id="21740-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="21740-130">Requirement</span></span> | <span data-ttu-id="21740-131">Valore</span><span class="sxs-lookup"><span data-stu-id="21740-131">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="21740-132">Versione</span><span class="sxs-lookup"><span data-stu-id="21740-132">Version</span></span><br/> | <span data-ttu-id="21740-133">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="21740-133">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="21740-134">DLL</span><span class="sxs-lookup"><span data-stu-id="21740-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="21740-135"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21740-135"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21740-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="21740-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21740-137">**Oggetto esterno per i negozi di tipo 1 online**</span><span class="sxs-lookup"><span data-stu-id="21740-137">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





