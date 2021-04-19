---
title: THEME. showErrorDialog
description: Il metodo showErrorDialog Visualizza la finestra di dialogo di errore standard.
ms.assetid: cec9ecfd-6665-4b0a-a09c-49120d557a80
keywords:
- THEME. showErrorDialog Windows Media Player
topic_type:
- apiref
api_name:
- THEME.showErrorDialog
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0cdc1f9df13ec460ce780507e1bde38a2996f915
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328387"
---
# <a name="themeshowerrordialog"></a><span data-ttu-id="474c2-104">THEME. showErrorDialog</span><span class="sxs-lookup"><span data-stu-id="474c2-104">THEME.showErrorDialog</span></span>

<span data-ttu-id="474c2-105">Il metodo **showErrorDialog** Visualizza la finestra di dialogo di errore standard.</span><span class="sxs-lookup"><span data-stu-id="474c2-105">The **showErrorDialog** method displays the standard error dialog box.</span></span>

``` syntax
        theme.showErrorDialog()
```

## <a name="parameters"></a><span data-ttu-id="474c2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="474c2-106">Parameters</span></span>

<span data-ttu-id="474c2-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="474c2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="474c2-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="474c2-108">Return Value</span></span>

<span data-ttu-id="474c2-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="474c2-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="474c2-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="474c2-110">Remarks</span></span>

<span data-ttu-id="474c2-111">Se **Settings. enableErrorDialogs** è false, questo metodo può essere utilizzato per visualizzare la finestra di dialogo di errore a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="474c2-111">If **Settings.enableErrorDialogs** is false, this method can be used to programmatically display the error dialog.</span></span> <span data-ttu-id="474c2-112">Se non sono presenti errori nella coda degli errori, la finestra di dialogo di errore non viene visualizzata.</span><span class="sxs-lookup"><span data-stu-id="474c2-112">If there are no errors in the error queue, the error dialog box is not shown.</span></span>

<span data-ttu-id="474c2-113">Per Windows Media Player 9 serie o versioni successive, questo metodo deve essere chiamato dal gestore eventi di errore.</span><span class="sxs-lookup"><span data-stu-id="474c2-113">For Windows Media Player 9 Series or later, this method must be called from the error event handler.</span></span> <span data-ttu-id="474c2-114">Windows Media Player 9 Series o versioni successive Cancella la coda degli errori per le interfacce dopo che è stato generato l'evento di errore.</span><span class="sxs-lookup"><span data-stu-id="474c2-114">Windows Media Player 9 Series or later clears the error queue for skins after the error event has been fired.</span></span>

## <a name="requirements"></a><span data-ttu-id="474c2-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="474c2-115">Requirements</span></span>



| <span data-ttu-id="474c2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="474c2-116">Requirement</span></span> | <span data-ttu-id="474c2-117">Valore</span><span class="sxs-lookup"><span data-stu-id="474c2-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="474c2-118">Versione</span><span class="sxs-lookup"><span data-stu-id="474c2-118">Version</span></span><br/> | <span data-ttu-id="474c2-119">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="474c2-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="474c2-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="474c2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="474c2-121">**Elemento THEME**</span><span class="sxs-lookup"><span data-stu-id="474c2-121">**THEME Element**</span></span>](theme-element.md)
</dt> <dt>

[<span data-ttu-id="474c2-122">**Settings. enableErrorDialogs**</span><span class="sxs-lookup"><span data-stu-id="474c2-122">**Settings.enableErrorDialogs**</span></span>](settings-enableerrordialogs.md)
</dt> </dl>

 

 





