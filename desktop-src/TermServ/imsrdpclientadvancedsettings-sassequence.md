---
title: Proprietà SasSequence di IMsRdpClientAdvancedSettings
description: Specifica la sequenza di accesso protetto che il client userà per accedere alla schermata di accesso nel server.
ms.assetid: ec1dc7b1-2bf1-447b-a768-08f28982a995
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà SasSequence
- Servizi Desktop remoto proprietà SasSequence, interfaccia IMsRdpClientAdvancedSettings
- Interfaccia IMsRdpClientAdvancedSettings Servizi Desktop remoto, proprietà SasSequence
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.SasSequence
- IMsRdpClientAdvancedSettings.get_SasSequence
- IMsRdpClientAdvancedSettings.put_SasSequence
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cf38a4e1f048e67613b92b3629aa96cca281b1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475233"
---
# <a name="imsrdpclientadvancedsettingssassequence-property"></a><span data-ttu-id="074b9-106">Proprietà IMsRdpClientAdvancedSettings:: SasSequence</span><span class="sxs-lookup"><span data-stu-id="074b9-106">IMsRdpClientAdvancedSettings::SasSequence property</span></span>

<span data-ttu-id="074b9-107">Specifica la sequenza di accesso protetto che il client userà per accedere alla schermata di accesso nel server.</span><span class="sxs-lookup"><span data-stu-id="074b9-107">Specifies the secure access sequence (SAS) the client will use to access the login screen on the server.</span></span>

<span data-ttu-id="074b9-108">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="074b9-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="074b9-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="074b9-109">Syntax</span></span>


```C++
HRESULT put_SasSequence(
  [in]  LONG sasSequence
);

HRESULT get_SasSequence(
  [out] LONG *psasSequence
);
```



## <a name="property-value"></a><span data-ttu-id="074b9-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="074b9-110">Property value</span></span>

<span data-ttu-id="074b9-111">Valore **Long** che contiene l'indicatore SAS.</span><span class="sxs-lookup"><span data-stu-id="074b9-111">A **LONG** value that contains the SAS indicator.</span></span> <span data-ttu-id="074b9-112">L'unico valore supportato è 0xaa03, che indica la sequenza CTRL + ALT + CANC standard.</span><span class="sxs-lookup"><span data-stu-id="074b9-112">The only supported value is 0xaa03, which indicates the standard CTRL+ALT+DELETE sequence.</span></span>

## <a name="remarks"></a><span data-ttu-id="074b9-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="074b9-113">Remarks</span></span>

<span data-ttu-id="074b9-114">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="074b9-114">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="074b9-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="074b9-115">Requirements</span></span>



| <span data-ttu-id="074b9-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="074b9-116">Requirement</span></span> | <span data-ttu-id="074b9-117">Valore</span><span class="sxs-lookup"><span data-stu-id="074b9-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="074b9-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="074b9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="074b9-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="074b9-119">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="074b9-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="074b9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="074b9-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="074b9-121">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="074b9-122">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="074b9-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="074b9-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="074b9-123"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="074b9-124">DLL</span><span class="sxs-lookup"><span data-stu-id="074b9-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="074b9-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="074b9-125"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="074b9-126">IID</span><span class="sxs-lookup"><span data-stu-id="074b9-126">IID</span></span><br/>                      | <span data-ttu-id="074b9-127">IID \_ IMsRdpClientAdvancedSettings è definito come 3c65b4ab-12b3-465b-aCD4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="074b9-127">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="074b9-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="074b9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="074b9-129">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="074b9-129">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





