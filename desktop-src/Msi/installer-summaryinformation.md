---
description: La proprietà SummaryInformation dell'oggetto Installer restituisce un oggetto SummaryInfo che può essere utilizzato per esaminare, aggiornare e aggiungere proprietà al flusso di informazioni di riepilogo di un pacchetto o di una trasformazione.
ms.assetid: 6a1d81b9-d61f-4bff-92c3-35fc436a6a41
title: Proprietà Installer. SummaryInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.SummaryInformation
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1ee593ca2ffebf3ca5574a8e2a6547b9cd81be40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325290"
---
# <a name="installersummaryinformation-property"></a><span data-ttu-id="f08f9-103">Proprietà Installer. SummaryInformation</span><span class="sxs-lookup"><span data-stu-id="f08f9-103">Installer.SummaryInformation property</span></span>

<span data-ttu-id="f08f9-104">La proprietà **SummaryInformation** dell'oggetto [**Installer**](installer-object.md) restituisce un oggetto [**SummaryInfo**](summaryinfo-object.md) che può essere utilizzato per esaminare, aggiornare e aggiungere proprietà al flusso di informazioni di riepilogo di un pacchetto o di una trasformazione.</span><span class="sxs-lookup"><span data-stu-id="f08f9-104">The **SummaryInformation** property of the [**Installer**](installer-object.md) object returns a [**SummaryInfo**](summaryinfo-object.md) object that can be used to examine, update, and add properties to the summary information stream of a package or transform.</span></span>

<span data-ttu-id="f08f9-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="f08f9-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f08f9-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f08f9-106">Syntax</span></span>


```JScript
propVal = Installer.SummaryInformation
```



## <a name="property-value"></a><span data-ttu-id="f08f9-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="f08f9-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="f08f9-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="f08f9-108">Remarks</span></span>

<span data-ttu-id="f08f9-109">Se viene usato un valore di *maxProperties* maggiore di 0 per aprire un flusso di informazioni di riepilogo esistente, è necessario chiamare il metodo di [**salvataggio permanente**](summaryinfo-persist.md) prima di chiudere l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="f08f9-109">If a value of *maxProperties* greater than 0 is used to open an existing summary information stream, the [**Persist**](summaryinfo-persist.md) method must be called before closing the object.</span></span> <span data-ttu-id="f08f9-110">In caso contrario, le informazioni sul flusso esistenti vengono perse.</span><span class="sxs-lookup"><span data-stu-id="f08f9-110">Failing to do this loses the existing stream information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f08f9-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f08f9-111">Requirements</span></span>



| <span data-ttu-id="f08f9-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="f08f9-112">Requirement</span></span> | <span data-ttu-id="f08f9-113">Valore</span><span class="sxs-lookup"><span data-stu-id="f08f9-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f08f9-114">Versione</span><span class="sxs-lookup"><span data-stu-id="f08f9-114">Version</span></span><br/> | <span data-ttu-id="f08f9-115">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f08f9-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f08f9-116">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f08f9-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f08f9-117">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="f08f9-117">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="f08f9-118">DLL</span><span class="sxs-lookup"><span data-stu-id="f08f9-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="f08f9-119"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f08f9-119"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="f08f9-120">IID</span><span class="sxs-lookup"><span data-stu-id="f08f9-120">IID</span></span><br/>     | <span data-ttu-id="f08f9-121">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="f08f9-121">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




