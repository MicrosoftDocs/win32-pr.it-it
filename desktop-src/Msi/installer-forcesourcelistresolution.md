---
description: Il metodo ForceSourceListResolution dell'oggetto Installer impone all'Windows Installer di eseguire la ricerca nell'elenco di origine di una fonte di prodotto valida.
ms.assetid: d5097331-8cf5-494f-9e88-bcffcad3fe5d
title: Installer. ForceSourceListResolution, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ForceSourceListResolution
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cadc27f3eaa90cd6fb2729f73d07cbcfa1f96b73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324619"
---
# <a name="installerforcesourcelistresolution-method"></a><span data-ttu-id="aaaff-103">Installer. ForceSourceListResolution, metodo</span><span class="sxs-lookup"><span data-stu-id="aaaff-103">Installer.ForceSourceListResolution method</span></span>

<span data-ttu-id="aaaff-104">Il metodo **ForceSourceListResolution** dell'oggetto [**Installer**](installer-object.md) impone al programma di installazione di eseguire la ricerca nell'elenco di origine di una fonte di prodotto valida la volta successiva che è necessaria un'origine, ad esempio quando il programma di installazione esegue un'installazione o una reinstallazione o quando richiede il percorso di un componente impostato per l'esecuzione dall'origine.</span><span class="sxs-lookup"><span data-stu-id="aaaff-104">The **ForceSourceListResolution** method of the [**Installer**](installer-object.md) object forces the installer to search the source list for a valid product source the next time a source is needed, such as when the installer performs an installation or a reinstallation, or when it needs the path for a component set to run from source.</span></span>

## <a name="syntax"></a><span data-ttu-id="aaaff-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aaaff-105">Syntax</span></span>


```JScript
Installer.ForceSourceListResolution(
  Product,
  User
)
```



## <a name="parameters"></a><span data-ttu-id="aaaff-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="aaaff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aaaff-107">*Prodotto*</span><span class="sxs-lookup"><span data-stu-id="aaaff-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="aaaff-108">Specifica il codice del prodotto.</span><span class="sxs-lookup"><span data-stu-id="aaaff-108">Specifies the product code.</span></span>

</dd> <dt>

<span data-ttu-id="aaaff-109">*Utente*</span><span class="sxs-lookup"><span data-stu-id="aaaff-109">*User*</span></span> 
</dt> <dd>

<span data-ttu-id="aaaff-110">Nome utente per l'installazione per utente; stringa null o vuota per l'installazione per computer.</span><span class="sxs-lookup"><span data-stu-id="aaaff-110">User name for per-user installation; null or empty string for per-machine installation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aaaff-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aaaff-111">Return value</span></span>

<span data-ttu-id="aaaff-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="aaaff-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="aaaff-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aaaff-113">Requirements</span></span>



| <span data-ttu-id="aaaff-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="aaaff-114">Requirement</span></span> | <span data-ttu-id="aaaff-115">Valore</span><span class="sxs-lookup"><span data-stu-id="aaaff-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aaaff-116">Versione</span><span class="sxs-lookup"><span data-stu-id="aaaff-116">Version</span></span><br/> | <span data-ttu-id="aaaff-117">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="aaaff-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="aaaff-118">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="aaaff-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="aaaff-119">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="aaaff-119">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="aaaff-120">DLL</span><span class="sxs-lookup"><span data-stu-id="aaaff-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="aaaff-121"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aaaff-121"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="aaaff-122">IID</span><span class="sxs-lookup"><span data-stu-id="aaaff-122">IID</span></span><br/>     | <span data-ttu-id="aaaff-123">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="aaaff-123">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="aaaff-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aaaff-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aaaff-125">**MsiSourceListForceResolution**</span><span class="sxs-lookup"><span data-stu-id="aaaff-125">**MsiSourceListForceResolution**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)
</dt> <dt>

[<span data-ttu-id="aaaff-126">Resilienza di origine</span><span class="sxs-lookup"><span data-stu-id="aaaff-126">Source Resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 




