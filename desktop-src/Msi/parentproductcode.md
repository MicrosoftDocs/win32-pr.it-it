---
description: Durante un'installazione simultanea, il programma di installazione imposta la proprietà ParentProductCode nella sessione dell'installazione simultanea sullo stesso valore della proprietà ProductCode nella sessione dell'installazione padre.
ms.assetid: 7bf2b9b1-9efd-4d47-9fa3-253421f1ba4f
title: Proprietà ParentProductCode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82385a4df94d3a044f0ee6a77461d69e63cc6d46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329740"
---
# <a name="parentproductcode-property"></a><span data-ttu-id="f668c-103">Proprietà ParentProductCode</span><span class="sxs-lookup"><span data-stu-id="f668c-103">ParentProductCode property</span></span>

<span data-ttu-id="f668c-104">Durante un'installazione simultanea, il programma di installazione imposta la proprietà **ParentProductCode** nella sessione dell'installazione simultanea sullo stesso valore della proprietà [**ProductCode**](productcode.md) nella sessione dell'installazione padre.</span><span class="sxs-lookup"><span data-stu-id="f668c-104">During a concurrent installation, the installer sets the **ParentProductCode** property in the concurrent installation's session to the same value as the [**ProductCode**](productcode.md) property in the parent installation's session.</span></span> <span data-ttu-id="f668c-105">Le installazioni padre eseguono le azioni di installazione simultanee per eseguire un'installazione simultanea.</span><span class="sxs-lookup"><span data-stu-id="f668c-105">Parent installations run the concurrent installation actions to perform a concurrent installation.</span></span> <span data-ttu-id="f668c-106">Un pacchetto di installazione può determinare se viene installato da un'azione di installazione simultanea controllando il valore di questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="f668c-106">An installation package can determine whether it is being installed by a concurrent installation action by checking the value of this property.</span></span>

> [!Note]  
> <span data-ttu-id="f668c-107">Le installazioni simultanee non sono consigliate per l'installazione di applicazioni destinate al rilascio al pubblico.</span><span class="sxs-lookup"><span data-stu-id="f668c-107">Concurrent Installations are not recommended for the installation of applications intended for release to the public.</span></span> <span data-ttu-id="f668c-108">Per informazioni sulle installazioni simultanee, vedere [installazioni simultanee](concurrent-installations.md).</span><span class="sxs-lookup"><span data-stu-id="f668c-108">For information about concurrent installations please see [Concurrent Installations](concurrent-installations.md).</span></span>

 

> [!Note]  
> <span data-ttu-id="f668c-109">Questa proprietà non viene impostata se l'installazione simultanea viene eseguita dall'azione [RemoveExistingProducts](removeexistingproducts-action.md) .</span><span class="sxs-lookup"><span data-stu-id="f668c-109">This property is not set if the concurrent installation is being run by the [RemoveExistingProducts](removeexistingproducts-action.md) action.</span></span>

 

## <a name="remarks"></a><span data-ttu-id="f668c-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="f668c-110">Remarks</span></span>

<span data-ttu-id="f668c-111">Per impedire l'installazione di un pacchetto come installazione simultanea, aggiungere una delle seguenti istruzioni condizionali alla tabella [LaunchCondition](launchcondition-table.md) .</span><span class="sxs-lookup"><span data-stu-id="f668c-111">To prevent a package from ever being installed as a concurrent installation, add either of the following conditional statements to the [LaunchCondition](launchcondition-table.md) table.</span></span> <span data-ttu-id="f668c-112">In questo modo si impedisce che il pacchetto venga installato da un'azione di installazione simultanea eseguita da un'altra installazione.</span><span class="sxs-lookup"><span data-stu-id="f668c-112">This prevents the package from ever being installed by a concurrent installation action run by another installation.</span></span> <span data-ttu-id="f668c-113">Questo non impedisce l'installazione del pacchetto tramite l'azione [RemoveExistingProducts](removeexistingproducts-action.md) .</span><span class="sxs-lookup"><span data-stu-id="f668c-113">This does not prevent the package from being installed by the [RemoveExistingProducts](removeexistingproducts-action.md) action.</span></span>

``` syntax
"Not ParentProductCode"
```

``` syntax
"Not ParentOriginalDatabase"
```

## <a name="requirements"></a><span data-ttu-id="f668c-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f668c-114">Requirements</span></span>



| <span data-ttu-id="f668c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f668c-115">Requirement</span></span> | <span data-ttu-id="f668c-116">Valore</span><span class="sxs-lookup"><span data-stu-id="f668c-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f668c-117">Versione</span><span class="sxs-lookup"><span data-stu-id="f668c-117">Version</span></span><br/> | <span data-ttu-id="f668c-118">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f668c-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f668c-119">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f668c-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f668c-120">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f668c-120">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="f668c-121">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="f668c-121">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f668c-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f668c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f668c-123">Proprietà</span><span class="sxs-lookup"><span data-stu-id="f668c-123">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="f668c-124">**ParentOriginalDatabase**</span><span class="sxs-lookup"><span data-stu-id="f668c-124">**ParentOriginalDatabase**</span></span>](parentoriginaldatabase.md)
</dt> </dl>

 

 




