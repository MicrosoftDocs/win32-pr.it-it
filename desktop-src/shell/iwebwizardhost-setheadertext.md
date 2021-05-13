---
description: Imposta il titolo e il sottotitolo visualizzati nell'intestazione della procedura guidata. In generale, il client visualizza l'intestazione sopra il codice HTML e sotto la barra del titolo.
title: Metodo WebWizardHost.SetHeaderText (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.SetHeaderText
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: e627de44-9929-4e08-9fd9-ca22743f434a
ms.openlocfilehash: d524f9ae6d1031d518e237d393bbb1dc0d35b2bd
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841832"
---
# <a name="webwizardhostsetheadertext-method"></a><span data-ttu-id="043e9-104">Metodo WebWizardHost.SetHeaderText</span><span class="sxs-lookup"><span data-stu-id="043e9-104">WebWizardHost.SetHeaderText method</span></span>

<span data-ttu-id="043e9-105">Imposta il titolo e il sottotitolo visualizzati nell'intestazione della procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="043e9-105">Sets the title and subtitle that appear in the wizard header.</span></span> <span data-ttu-id="043e9-106">In generale, il client visualizza l'intestazione sopra il codice HTML e sotto la barra del titolo.</span><span class="sxs-lookup"><span data-stu-id="043e9-106">In general, the client will display the header above the HTML and below the title bar.</span></span>

## <a name="syntax"></a><span data-ttu-id="043e9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="043e9-107">Syntax</span></span>


```JScript
iRetVal = WebWizardHost.SetHeaderText(
  bstrHeaderTitle,
  bstrHeaderSubtitle
)
```



## <a name="parameters"></a><span data-ttu-id="043e9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="043e9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="043e9-109">*bstrHeaderTitle* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="043e9-109">*bstrHeaderTitle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="043e9-110">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="043e9-110">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="043e9-111">Stringa contenente il titolo.</span><span class="sxs-lookup"><span data-stu-id="043e9-111">String containing the title.</span></span>

</dd> <dt>

<span data-ttu-id="043e9-112">*bstrHeaderSubtitle* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="043e9-112">*bstrHeaderSubtitle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="043e9-113">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="043e9-113">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="043e9-114">Stringa contenente il sottotitolo.</span><span class="sxs-lookup"><span data-stu-id="043e9-114">String containing the subtitle.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="043e9-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="043e9-115">Requirements</span></span>



| <span data-ttu-id="043e9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="043e9-116">Requirement</span></span> | <span data-ttu-id="043e9-117">Valore</span><span class="sxs-lookup"><span data-stu-id="043e9-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="043e9-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="043e9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="043e9-119">Solo app desktop di Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="043e9-119">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="043e9-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="043e9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="043e9-121">Solo app desktop di Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="043e9-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="043e9-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="043e9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="043e9-123"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="043e9-123"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="043e9-124">Idl</span><span class="sxs-lookup"><span data-stu-id="043e9-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="043e9-125"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="043e9-125"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 
