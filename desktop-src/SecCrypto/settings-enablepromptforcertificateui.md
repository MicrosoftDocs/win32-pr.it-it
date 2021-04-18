---
description: Imposta o recupera un valore booleano che specifica se è possibile utilizzare i prompt dell'interfaccia utente per l'identità di un firmatario o di un mittente.
ms.assetid: b9765de4-0b94-4006-aaa8-9ad6858da1f4
title: Proprietà Settings. EnablePromptForCertificateUI
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Settings.EnablePromptForCertificateUI
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e494c98e2a828b512b0bb66dc2a44cba8c37792c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329464"
---
# <a name="settingsenablepromptforcertificateui-property"></a><span data-ttu-id="6c8d0-103">Proprietà Settings. EnablePromptForCertificateUI</span><span class="sxs-lookup"><span data-stu-id="6c8d0-103">Settings.EnablePromptForCertificateUI property</span></span>

<span data-ttu-id="6c8d0-104">\[La proprietà **EnablePromptForCertificateUI** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.\]</span><span class="sxs-lookup"><span data-stu-id="6c8d0-104">\[The **EnablePromptForCertificateUI** property is available for use in the operating systems specified in the Requirements section.\]</span></span>

<span data-ttu-id="6c8d0-105">La proprietà **EnablePromptForCertificateUI** imposta o recupera un valore booleano che specifica se è possibile utilizzare i prompt dell'interfaccia utente per l'identità di un firmatario o di un mittente.</span><span class="sxs-lookup"><span data-stu-id="6c8d0-105">The **EnablePromptForCertificateUI** property sets or retrieves a Boolean value that specifies whether user interface prompts for a signer or sender's identity can be used.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c8d0-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6c8d0-106">Syntax</span></span>


```VB
Settings.EnablePromptForCertificateUI As Boolean
```



## <a name="property-value"></a><span data-ttu-id="6c8d0-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="6c8d0-107">Property value</span></span>

<span data-ttu-id="6c8d0-108">Se è **true**, è possibile usare l'identità dell'interfaccia utente per un firmatario o un mittente.</span><span class="sxs-lookup"><span data-stu-id="6c8d0-108">If **true**, user interface prompts for a signer or sender's identity can be used.</span></span> <span data-ttu-id="6c8d0-109">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="6c8d0-109">The default value is **false**.</span></span>

> [!Note]  
> <span data-ttu-id="6c8d0-110">L'impostazione di questa proprietà non disabilita gli avvisi generati prima che l'utilizzo della chiave privata venga eseguito da un'applicazione basata sul Web.</span><span class="sxs-lookup"><span data-stu-id="6c8d0-110">Setting this property does not disable warnings that are generated before any private key usage is done from a web-based application.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6c8d0-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6c8d0-111">Requirements</span></span>



| <span data-ttu-id="6c8d0-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c8d0-112">Requirement</span></span> | <span data-ttu-id="6c8d0-113">Valore</span><span class="sxs-lookup"><span data-stu-id="6c8d0-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c8d0-114">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="6c8d0-114">Redistributable</span></span><br/> | <span data-ttu-id="6c8d0-115">CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP</span><span class="sxs-lookup"><span data-stu-id="6c8d0-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="6c8d0-116">DLL</span><span class="sxs-lookup"><span data-stu-id="6c8d0-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="6c8d0-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c8d0-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c8d0-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6c8d0-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c8d0-119">**Impostazioni**</span><span class="sxs-lookup"><span data-stu-id="6c8d0-119">**Settings**</span></span>](settings.md)
</dt> </dl>

 

 




