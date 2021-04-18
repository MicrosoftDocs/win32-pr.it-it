---
title: THEME. openDialog
description: Il metodo openDialog apre una finestra di dialogo file.
ms.assetid: d7f4549c-a5c3-4902-b13b-51f3d4444ea9
keywords:
- THEME. openDialog Windows Media Player
topic_type:
- apiref
api_name:
- THEME.openDialog
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 79b9478b6b970b1d8d18b6f40975479e4755fa6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333918"
---
# <a name="themeopendialog"></a><span data-ttu-id="a30df-104">THEME. openDialog</span><span class="sxs-lookup"><span data-stu-id="a30df-104">THEME.openDialog</span></span>

<span data-ttu-id="a30df-105">Il metodo **openDialog** apre una finestra di dialogo file.</span><span class="sxs-lookup"><span data-stu-id="a30df-105">The **openDialog** method opens a file dialog box.</span></span>

``` syntax
        theme.openDialog(dialogType, parameters)
```

## <a name="parameters"></a><span data-ttu-id="a30df-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a30df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a30df-107"><span id="dialogType"></span><span id="dialogtype"></span><span id="DIALOGTYPE"></span>*dialogType*</span><span class="sxs-lookup"><span data-stu-id="a30df-107"><span id="dialogType"></span><span id="dialogtype"></span><span id="DIALOGTYPE"></span>*dialogType*</span></span>
</dt> <dd>

<span data-ttu-id="a30df-108">**Stringa** che specifica il tipo di finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="a30df-108">A **String** that specifies the type of dialog box.</span></span> <span data-ttu-id="a30df-109">Deve essere impostato su "FILE \_ aperto".</span><span class="sxs-lookup"><span data-stu-id="a30df-109">Must be set to "FILE\_OPEN".</span></span>

</dd> <dt>

<span data-ttu-id="a30df-110"><span id="parameters"></span><span id="PARAMETERS"></span>*parametri*</span><span class="sxs-lookup"><span data-stu-id="a30df-110"><span id="parameters"></span><span id="PARAMETERS"></span>*parameters*</span></span>
</dt> <dd>

<span data-ttu-id="a30df-111">**Stringa** che può essere utilizzata per informazioni aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="a30df-111">A **String** that can be used for additional information.</span></span> <span data-ttu-id="a30df-112">Deve essere impostato su "FILES \_ ALLMEDIA".</span><span class="sxs-lookup"><span data-stu-id="a30df-112">Must be set to "FILES\_ALLMEDIA".</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a30df-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a30df-113">Return Value</span></span>

<span data-ttu-id="a30df-114">Questo metodo restituisce una **stringa** contenente l'URL del file selezionato o "" (stringa vuota) se l'utente fa clic su Annulla.</span><span class="sxs-lookup"><span data-stu-id="a30df-114">This method returns a **String** containing the URL of the selected file or "" (empty string) if the user clicks cancel.</span></span>

## <a name="remarks"></a><span data-ttu-id="a30df-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="a30df-115">Remarks</span></span>

<span data-ttu-id="a30df-116">Questo metodo può essere utilizzato per i file nei dischi rigidi locali o nelle unità di rete.</span><span class="sxs-lookup"><span data-stu-id="a30df-116">This method can be used for files on the local hard drives or on network drives.</span></span>

## <a name="examples"></a><span data-ttu-id="a30df-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="a30df-117">Examples</span></span>


```JScript
<THEME>
  <VIEW id="View1" 
    backgroundImage="greenstone.bmp" 
    width=500 height=300 author="Microsoft Corp.">
    <BUTTON 
      id="Open" 
      image="Open.png" 
      onclick="jscript:
        player.URL = theme.openDialog('FILE_OPEN','FILES_ALLMEDIA')">
    </BUTTON>
  </VIEW>
</THEME>
```



## <a name="requirements"></a><span data-ttu-id="a30df-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a30df-118">Requirements</span></span>



| <span data-ttu-id="a30df-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a30df-119">Requirement</span></span> | <span data-ttu-id="a30df-120">Valore</span><span class="sxs-lookup"><span data-stu-id="a30df-120">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="a30df-121">Versione</span><span class="sxs-lookup"><span data-stu-id="a30df-121">Version</span></span><br/> | <span data-ttu-id="a30df-122">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="a30df-122">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a30df-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a30df-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a30df-124">**Elemento THEME**</span><span class="sxs-lookup"><span data-stu-id="a30df-124">**THEME Element**</span></span>](theme-element.md)
</dt> </dl>

 

 





