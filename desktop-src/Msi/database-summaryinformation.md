---
description: La proprietà SummaryInformation dell'oggetto di database restituisce un oggetto SummaryInfo che può essere utilizzato per esaminare, aggiornare e aggiungere proprietà al flusso di informazioni di riepilogo.
ms.assetid: 6892a8c0-c99e-4dcb-b6cb-d470ffceab69
title: Proprietà database. SummaryInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.SummaryInformation
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 524c4fa2fe5014436f122f0a5460aced820e30ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333055"
---
# <a name="databasesummaryinformation-property"></a><span data-ttu-id="525d5-103">Proprietà database. SummaryInformation</span><span class="sxs-lookup"><span data-stu-id="525d5-103">Database.SummaryInformation property</span></span>

<span data-ttu-id="525d5-104">La proprietà **SummaryInformation** dell'oggetto di [**database**](database-object.md) restituisce un oggetto [**SummaryInfo**](summaryinfo-object.md) che può essere utilizzato per esaminare, aggiornare e aggiungere proprietà al flusso di [informazioni di riepilogo](summary-information-stream.md).</span><span class="sxs-lookup"><span data-stu-id="525d5-104">The **SummaryInformation** property of the [**Database**](database-object.md) object returns a [**SummaryInfo**](summaryinfo-object.md) object that can be used to examine, update, and add properties to the [summary information stream](summary-information-stream.md).</span></span>

<span data-ttu-id="525d5-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="525d5-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="525d5-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="525d5-106">Syntax</span></span>


```JScript
propVal = Database.SummaryInformation
```



## <a name="property-value"></a><span data-ttu-id="525d5-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="525d5-107">Property value</span></span>

<span data-ttu-id="525d5-108">Numero massimo di proprietà da aggiungere o modificare.</span><span class="sxs-lookup"><span data-stu-id="525d5-108">The maximum number of properties to be added or modified.</span></span> <span data-ttu-id="525d5-109">Questo parametro è obbligatorio e viene utilizzato per allocare memoria di lavoro sufficiente durante la generazione del flusso.</span><span class="sxs-lookup"><span data-stu-id="525d5-109">This parameter is required and used to allocate sufficient working memory during the stream generation.</span></span> <span data-ttu-id="525d5-110">Non è necessario archiviare questo numero di proprietà.</span><span class="sxs-lookup"><span data-stu-id="525d5-110">It is not required to store this number of properties.</span></span> <span data-ttu-id="525d5-111">Se il database è aperto in sola lettura per impedire l'aggiornamento del flusso, è necessario utilizzare un valore pari a zero.</span><span class="sxs-lookup"><span data-stu-id="525d5-111">A value of zero must be used if the database is opened read-only to prevent the stream from being updated.</span></span>

## <a name="remarks"></a><span data-ttu-id="525d5-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="525d5-112">Remarks</span></span>

<span data-ttu-id="525d5-113">Se viene usato un valore di *maxProperties* maggiore di 0 per aprire un flusso di informazioni di riepilogo esistente, è necessario chiamare il metodo di [**salvataggio permanente**](summaryinfo-persist.md) prima di chiudere l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="525d5-113">If a value of *maxProperties* greater than 0 is used to open an existing summary information stream, the [**Persist**](summaryinfo-persist.md) method must be called before closing the object.</span></span> <span data-ttu-id="525d5-114">In caso contrario, le informazioni sul flusso esistenti andranno perse.</span><span class="sxs-lookup"><span data-stu-id="525d5-114">Failing to do this will lose the existing stream information.</span></span>

<span data-ttu-id="525d5-115">Se la proprietà ha esito negativo, è possibile ottenere informazioni estese sugli errori usando il metodo [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="525d5-115">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="525d5-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="525d5-116">Requirements</span></span>



| <span data-ttu-id="525d5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="525d5-117">Requirement</span></span> | <span data-ttu-id="525d5-118">Valore</span><span class="sxs-lookup"><span data-stu-id="525d5-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="525d5-119">Versione</span><span class="sxs-lookup"><span data-stu-id="525d5-119">Version</span></span><br/> | <span data-ttu-id="525d5-120">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="525d5-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="525d5-121">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="525d5-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="525d5-122">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="525d5-122">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="525d5-123">DLL</span><span class="sxs-lookup"><span data-stu-id="525d5-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="525d5-124"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="525d5-124"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="525d5-125">IID</span><span class="sxs-lookup"><span data-stu-id="525d5-125">IID</span></span><br/>     | <span data-ttu-id="525d5-126">IID \_ iDatabase è definito come 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="525d5-126">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




