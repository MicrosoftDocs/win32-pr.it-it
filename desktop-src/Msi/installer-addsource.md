---
description: Il metodo AddSource dell'oggetto Installer aggiunge un'origine all'elenco di origini di rete valide nell'elenco di origine.
ms.assetid: e24c8484-fe84-4f97-9c06-c063bb7c6810
title: Installer. AddSource, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.AddSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3067ae287311c6ed26b509545523db75a3fed4cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328066"
---
# <a name="installeraddsource-method"></a><span data-ttu-id="07e56-103">Installer. AddSource, metodo</span><span class="sxs-lookup"><span data-stu-id="07e56-103">Installer.AddSource method</span></span>

<span data-ttu-id="07e56-104">Il metodo **addsource** dell'oggetto [**Installer**](installer-object.md) aggiunge un'origine all'elenco di origini di rete valide nell'elenco di origine.</span><span class="sxs-lookup"><span data-stu-id="07e56-104">The **AddSource** method of the [**Installer**](installer-object.md) object adds a source to the list of valid network sources in the sourcelist.</span></span>

## <a name="syntax"></a><span data-ttu-id="07e56-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="07e56-105">Syntax</span></span>


```JScript
Installer.AddSource(
  Product,
  User,
  Source
)
```



## <a name="parameters"></a><span data-ttu-id="07e56-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="07e56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07e56-107">*Prodotto*</span><span class="sxs-lookup"><span data-stu-id="07e56-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="07e56-108">Specifica il codice del prodotto.</span><span class="sxs-lookup"><span data-stu-id="07e56-108">Specifies the product code.</span></span>

</dd> <dt>

<span data-ttu-id="07e56-109">*Utente*</span><span class="sxs-lookup"><span data-stu-id="07e56-109">*User*</span></span> 
</dt> <dd>

<span data-ttu-id="07e56-110">Nome utente per l'installazione per utente; stringa null o vuota per l'installazione per computer.</span><span class="sxs-lookup"><span data-stu-id="07e56-110">User name for per-user installation; null or empty string for per-machine installation.</span></span>

</dd> <dt>

<span data-ttu-id="07e56-111">*Origine*</span><span class="sxs-lookup"><span data-stu-id="07e56-111">*Source*</span></span> 
</dt> <dd>

<span data-ttu-id="07e56-112">Puntatore alla stringa che specifica l'origine.</span><span class="sxs-lookup"><span data-stu-id="07e56-112">Pointer to the string specifying the source.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07e56-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="07e56-113">Return value</span></span>

<span data-ttu-id="07e56-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="07e56-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="07e56-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="07e56-115">Requirements</span></span>



| <span data-ttu-id="07e56-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="07e56-116">Requirement</span></span> | <span data-ttu-id="07e56-117">Valore</span><span class="sxs-lookup"><span data-stu-id="07e56-117">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07e56-118">Versione</span><span class="sxs-lookup"><span data-stu-id="07e56-118">Version</span></span><br/> | <span data-ttu-id="07e56-119">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="07e56-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="07e56-120">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="07e56-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="07e56-121">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="07e56-121">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="07e56-122">DLL</span><span class="sxs-lookup"><span data-stu-id="07e56-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="07e56-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07e56-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="07e56-124">IID</span><span class="sxs-lookup"><span data-stu-id="07e56-124">IID</span></span><br/>     | <span data-ttu-id="07e56-125">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="07e56-125">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="07e56-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="07e56-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07e56-127">**MsiSourceListAddSource**</span><span class="sxs-lookup"><span data-stu-id="07e56-127">**MsiSourceListAddSource**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea)
</dt> <dt>

[<span data-ttu-id="07e56-128">resilienza di origine</span><span class="sxs-lookup"><span data-stu-id="07e56-128">source resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 




