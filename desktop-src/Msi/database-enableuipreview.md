---
description: Il metodo EnableUIPreview dell'oggetto di database semplifica la creazione di finestre di dialogo e Billboard, fornendo il supporto necessario per visualizzare le finestre di dialogo dell'interfaccia utente archiviate nel database del programma di installazione.
ms.assetid: c4687de7-8ab4-4377-ac5c-1fed7c915519
title: Metodo database. EnableUIPreview
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Database.EnableUIPreview
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1224bb100e0403e8df9f3bdb0cc0b5dbe017233f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331609"
---
# <a name="databaseenableuipreview-method"></a><span data-ttu-id="88e15-103">Metodo database. EnableUIPreview</span><span class="sxs-lookup"><span data-stu-id="88e15-103">Database.EnableUIPreview method</span></span>

<span data-ttu-id="88e15-104">Il metodo **EnableUIPreview** dell'oggetto di [**database**](database-object.md) semplifica la creazione di finestre di dialogo e Billboard, fornendo il supporto necessario per visualizzare le finestre di dialogo dell'interfaccia utente archiviate nel database del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="88e15-104">The **EnableUIPreview** method of the [**Database**](database-object.md) object facilitates the authoring of dialog boxes and billboards by providing the support needed to view user interface dialog boxes stored in the installer database.</span></span> <span data-ttu-id="88e15-105">Il metodo avvia la modalità di anteprima restituendo un oggetto di **database** di anteprima.</span><span class="sxs-lookup"><span data-stu-id="88e15-105">The method starts the preview mode by returning a preview **Database** object.</span></span> <span data-ttu-id="88e15-106">La modalità di anteprima termina quando viene rilasciato l'oggetto di anteprima.</span><span class="sxs-lookup"><span data-stu-id="88e15-106">The preview mode ends when the preview object is released.</span></span>

## <a name="syntax"></a><span data-ttu-id="88e15-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="88e15-107">Syntax</span></span>


```JScript
Database.EnableUIPreview()
```



## <a name="parameters"></a><span data-ttu-id="88e15-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="88e15-108">Parameters</span></span>

<span data-ttu-id="88e15-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="88e15-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="88e15-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="88e15-110">Return value</span></span>

<span data-ttu-id="88e15-111">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="88e15-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="88e15-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="88e15-112">Requirements</span></span>



| <span data-ttu-id="88e15-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="88e15-113">Requirement</span></span> | <span data-ttu-id="88e15-114">Valore</span><span class="sxs-lookup"><span data-stu-id="88e15-114">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88e15-115">Versione</span><span class="sxs-lookup"><span data-stu-id="88e15-115">Version</span></span><br/> | <span data-ttu-id="88e15-116">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="88e15-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="88e15-117">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="88e15-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="88e15-118">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="88e15-118">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="88e15-119">DLL</span><span class="sxs-lookup"><span data-stu-id="88e15-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="88e15-120"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88e15-120"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="88e15-121">IID</span><span class="sxs-lookup"><span data-stu-id="88e15-121">IID</span></span><br/>     | <span data-ttu-id="88e15-122">IID \_ iDatabase è definito come 000C109D-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="88e15-122">IID\_IDatabase is defined as 000C109D-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                            |



 

 




