---
description: Imposta il nome descrittivo del profilo.
ms.assetid: a0a2de8b-ab7b-49a8-b513-32af0052975f
title: 'Metodo IScanProfile:: SetValue (scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.SetName
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: bd5fbe0e723fea7f7fa75f838b898beceebed0a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312436"
---
# <a name="iscanprofilesetname-method"></a><span data-ttu-id="eb2d1-103">Metodo IScanProfile:: SetValue</span><span class="sxs-lookup"><span data-stu-id="eb2d1-103">IScanProfile::SetName method</span></span>

<span data-ttu-id="eb2d1-104">Imposta il nome descrittivo del profilo.</span><span class="sxs-lookup"><span data-stu-id="eb2d1-104">Sets the friendly name of the profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb2d1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eb2d1-105">Syntax</span></span>


```C++
HRESULT SetName(
  [in] BSTR bstrName
);
```



## <a name="parameters"></a><span data-ttu-id="eb2d1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="eb2d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb2d1-107">*bstrName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="eb2d1-107">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb2d1-108">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="eb2d1-108">Type: **BSTR**</span></span>

<span data-ttu-id="eb2d1-109">Nome descrittivo del profilo.</span><span class="sxs-lookup"><span data-stu-id="eb2d1-109">The friendly name of the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb2d1-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eb2d1-110">Return value</span></span>

<span data-ttu-id="eb2d1-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="eb2d1-111">Type: **HRESULT**</span></span>

<span data-ttu-id="eb2d1-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="eb2d1-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="eb2d1-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="eb2d1-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb2d1-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="eb2d1-114">Remarks</span></span>

<span data-ttu-id="eb2d1-115">Questo metodo è necessario perché non è possibile usare il GUID di un profilo per visualizzare il profilo di analisi a un utente.</span><span class="sxs-lookup"><span data-stu-id="eb2d1-115">This method is required because the GUID of a profile cannot be used to display the scan profile to a user.</span></span>

<span data-ttu-id="eb2d1-116">Un utente può modificare il nome descrittivo di un profilo con il metodo [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) .</span><span class="sxs-lookup"><span data-stu-id="eb2d1-116">A user can change the friendly name of a profile with the [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) method.</span></span>

<span data-ttu-id="eb2d1-117">Le modifiche apportate a un profilo non vengono salvate su disco fino a quando l'applicazione non chiama il metodo [**IScanProfile:: Save**](-wia-iscanprofile-save.md) .</span><span class="sxs-lookup"><span data-stu-id="eb2d1-117">Changes to a profile are not saved to disk until the application calls the [**IScanProfile::Save**](-wia-iscanprofile-save.md) method.</span></span>

<span data-ttu-id="eb2d1-118">Se due applicazioni creano oggetti del profilo di analisi dallo stesso file XML e ogni applicazione scrive le modifiche nel relativo oggetto, solo le modifiche apportate dall'applicazione che chiama [**IScanProfile:: Save**](-wia-iscanprofile-save.md) Last vengono salvate su disco.</span><span class="sxs-lookup"><span data-stu-id="eb2d1-118">If two applications create scan profile objects from the same XML file, and each application writes changes to its object, only the changes made by the application that calls [**IScanProfile::Save**](-wia-iscanprofile-save.md) last are saved to disk.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb2d1-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eb2d1-119">Requirements</span></span>



| <span data-ttu-id="eb2d1-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb2d1-120">Requirement</span></span> | <span data-ttu-id="eb2d1-121">Valore</span><span class="sxs-lookup"><span data-stu-id="eb2d1-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb2d1-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eb2d1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="eb2d1-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="eb2d1-123">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="eb2d1-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eb2d1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="eb2d1-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="eb2d1-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eb2d1-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eb2d1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb2d1-127"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb2d1-127"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="eb2d1-128">IDL</span><span class="sxs-lookup"><span data-stu-id="eb2d1-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="eb2d1-129"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="eb2d1-129"><dt>Scanprofiles.idl</dt></span></span> </dl> |



 

 




