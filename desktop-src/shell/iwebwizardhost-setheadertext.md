---
description: Imposta il titolo e il sottotitolo visualizzati nell'intestazione della procedura guidata. In generale, il client visualizzerà l'intestazione sopra il codice HTML e sotto la barra del titolo.
title: Metodo WebWizardHost. SetHeaderText (shldisp. h)
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
ms.openlocfilehash: 92e23fab94cfedd8bbc62e31086759af48238a95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980255"
---
# <a name="webwizardhostsetheadertext-method"></a><span data-ttu-id="1f27e-104">WebWizardHost. SetHeaderText, metodo</span><span class="sxs-lookup"><span data-stu-id="1f27e-104">WebWizardHost.SetHeaderText method</span></span>

<span data-ttu-id="1f27e-105">Imposta il titolo e il sottotitolo visualizzati nell'intestazione della procedura guidata.</span><span class="sxs-lookup"><span data-stu-id="1f27e-105">Sets the title and subtitle that appear in the wizard header.</span></span> <span data-ttu-id="1f27e-106">In generale, il client visualizzerà l'intestazione sopra il codice HTML e sotto la barra del titolo.</span><span class="sxs-lookup"><span data-stu-id="1f27e-106">In general, the client will display the header above the HTML and below the title bar.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f27e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1f27e-107">Syntax</span></span>


```JScript
iRetVal = WebWizardHost.SetHeaderText(
  bstrHeaderTitle,
  bstrHeaderSubtitle
)
```



## <a name="parameters"></a><span data-ttu-id="1f27e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="1f27e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f27e-109">*bstrHeaderTitle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1f27e-109">*bstrHeaderTitle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f27e-110">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="1f27e-110">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="1f27e-111">Stringa contenente il titolo.</span><span class="sxs-lookup"><span data-stu-id="1f27e-111">String containing the title.</span></span>

</dd> <dt>

<span data-ttu-id="1f27e-112">*bstrHeaderSubtitle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1f27e-112">*bstrHeaderSubtitle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1f27e-113">Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span><span class="sxs-lookup"><span data-stu-id="1f27e-113">Type: **[**BSTR**](/previous-versions/windows/desktop/automat/bstr)**</span></span>

<span data-ttu-id="1f27e-114">Stringa contenente il sottotitolo.</span><span class="sxs-lookup"><span data-stu-id="1f27e-114">String containing the subtitle.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1f27e-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1f27e-115">Requirements</span></span>



| <span data-ttu-id="1f27e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f27e-116">Requirement</span></span> | <span data-ttu-id="1f27e-117">Valore</span><span class="sxs-lookup"><span data-stu-id="1f27e-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1f27e-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1f27e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1f27e-119">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1f27e-119">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="1f27e-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1f27e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1f27e-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1f27e-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="1f27e-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1f27e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f27e-123"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f27e-123"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="1f27e-124">IDL</span><span class="sxs-lookup"><span data-stu-id="1f27e-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1f27e-125"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1f27e-125"><dt>Shldisp.idl</dt></span></span> </dl> |



 

 
