---
title: Error. Item (metodo)
description: Il metodo Item recupera un oggetto ErrorItem dalla coda degli errori.
ms.assetid: 3aca21ff-4c6b-4c24-a85d-3d015612a496
keywords:
- Metodo Item Media Player Windows
- Metodo Item Media Player Windows, classe Error
- Classe Error Media Player Windows, metodo Item
topic_type:
- apiref
api_name:
- Error.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5545df50fce05ff5a10a5f870d1ec07648434fe9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324575"
---
# <a name="erroritem-method"></a><span data-ttu-id="1a82f-106">Error. Item (metodo)</span><span class="sxs-lookup"><span data-stu-id="1a82f-106">Error.item method</span></span>

<span data-ttu-id="1a82f-107">Il metodo **Item** recupera un oggetto **ErrorItem** dalla coda degli errori.</span><span class="sxs-lookup"><span data-stu-id="1a82f-107">The **item** method retrieves an **ErrorItem** object from the error queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a82f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1a82f-108">Syntax</span></span>


```JScript
retVal = Error.item(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="1a82f-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="1a82f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a82f-110">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="1a82f-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a82f-111">**Numero** (**Long**) che contiene l'indice dell'oggetto **ErrorItem** da recuperare.</span><span class="sxs-lookup"><span data-stu-id="1a82f-111">**Number** (**long**) containing the index of the **ErrorItem** object to be retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a82f-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1a82f-112">Return value</span></span>

<span data-ttu-id="1a82f-113">Questo metodo restituisce un oggetto **ErrorItem** .</span><span class="sxs-lookup"><span data-stu-id="1a82f-113">This method returns an **ErrorItem** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a82f-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="1a82f-114">Remarks</span></span>

<span data-ttu-id="1a82f-115">Windows Media Player può generare un certo numero di errori in risposta a una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="1a82f-115">Windows Media Player can generate a number of errors in response to an error condition.</span></span> <span data-ttu-id="1a82f-116">Questo metodo consente il recupero di un errore specifico nella coda usando un numero di indice.</span><span class="sxs-lookup"><span data-stu-id="1a82f-116">This method allows the retrieval of a specific error in the queue by using an index number.</span></span> <span data-ttu-id="1a82f-117">I numeri di indice per la coda degli errori iniziano con zero.</span><span class="sxs-lookup"><span data-stu-id="1a82f-117">The index numbers for the error queue begin with zero.</span></span>

<span data-ttu-id="1a82f-118">È necessario impostare *le impostazioni*. **enableErrorDialogs** su false se si sceglie di visualizzare i messaggi di errore personalizzati.</span><span class="sxs-lookup"><span data-stu-id="1a82f-118">You should set *Settings*.**enableErrorDialogs** to false if you choose to display custom error messages.</span></span>

## <a name="examples"></a><span data-ttu-id="1a82f-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="1a82f-119">Examples</span></span>

<span data-ttu-id="1a82f-120">Nell'esempio JScript riportato di seguito viene utilizzato l' *errore*. oggetto **Item** in un gestore eventi per avvertire l'utente dell'errore più recente.</span><span class="sxs-lookup"><span data-stu-id="1a82f-120">The following JScript example uses the *Error*.**item** object in an event handler to alert the user to the most recent error.</span></span> <span data-ttu-id="1a82f-121">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="1a82f-121">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SCRIPT LANGUAGE="JScript"  FOR=Player EVENT=error()>

// Store the most recent error item number.
var max = Player.error.errorCount - 1 

// Store the most recent error in an error item object.
var errItem = Player.error.item(max);

// Use the error item object to store the error info.
errDesc = errItem.errorDescription;
errNum = errItem.errorCode;

// Display the error info.
alert(errNum + "\n" + errDesc);

</SCRIPT> 

```



## <a name="requirements"></a><span data-ttu-id="1a82f-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1a82f-122">Requirements</span></span>



| <span data-ttu-id="1a82f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a82f-123">Requirement</span></span> | <span data-ttu-id="1a82f-124">Valore</span><span class="sxs-lookup"><span data-stu-id="1a82f-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1a82f-125">Versione</span><span class="sxs-lookup"><span data-stu-id="1a82f-125">Version</span></span><br/> | <span data-ttu-id="1a82f-126">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="1a82f-126">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="1a82f-127">DLL</span><span class="sxs-lookup"><span data-stu-id="1a82f-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="1a82f-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a82f-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a82f-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1a82f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a82f-130">**Oggetto Error**</span><span class="sxs-lookup"><span data-stu-id="1a82f-130">**Error Object**</span></span>](error-object.md)
</dt> <dt>

[<span data-ttu-id="1a82f-131">**Oggetto ErrorItem**</span><span class="sxs-lookup"><span data-stu-id="1a82f-131">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> </dl>

 

 





