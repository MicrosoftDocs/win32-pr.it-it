---
description: Il metodo CollectUserInfo dell'oggetto Installer richiama una sequenza guidata dell'interfaccia utente che raccoglie e archivia sia le informazioni utente sia il codice del prodotto.
ms.assetid: 2faacf38-1af1-4e8a-a3f6-87733104614e
title: Installer. CollectUserInfo, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.CollectUserInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d7286fdbc9fab6b3db6752284bf86db05f920bd7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329029"
---
# <a name="installercollectuserinfo-method"></a><span data-ttu-id="be989-103">Installer. CollectUserInfo, metodo</span><span class="sxs-lookup"><span data-stu-id="be989-103">Installer.CollectUserInfo method</span></span>

<span data-ttu-id="be989-104">Il metodo **CollectUserInfo** dell'oggetto [**Installer**](installer-object.md) richiama una sequenza guidata dell'interfaccia utente che raccoglie e archivia sia le informazioni utente sia il codice del prodotto.</span><span class="sxs-lookup"><span data-stu-id="be989-104">The **CollectUserInfo** method of the [**Installer**](installer-object.md) object invokes a user interface wizard sequence which collects and stores both user information and the product code.</span></span>

## <a name="syntax"></a><span data-ttu-id="be989-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="be989-105">Syntax</span></span>


```JScript
Installer.CollectUserInfo(
  Product
)
```



## <a name="parameters"></a><span data-ttu-id="be989-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="be989-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be989-107">*Prodotto*</span><span class="sxs-lookup"><span data-stu-id="be989-107">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="be989-108">Specifica il [**codice**](productcode.md) del prodotto.</span><span class="sxs-lookup"><span data-stu-id="be989-108">Specifies the [**product code**](productcode.md) of the product.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be989-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="be989-109">Return value</span></span>

<span data-ttu-id="be989-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="be989-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="be989-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="be989-111">Remarks</span></span>

<span data-ttu-id="be989-112">Quando viene eseguita la prima volta, un'applicazione deve chiamare il metodo **CollectUserInfo** .</span><span class="sxs-lookup"><span data-stu-id="be989-112">An application should call the **CollectUserInfo** method the first time it is run.</span></span> <span data-ttu-id="be989-113">Il metodo **CollectUserInfo** apre il pacchetto di installazione del prodotto e richiama una sequenza guidata dell'interfaccia utente creata che raccoglie le informazioni utente.</span><span class="sxs-lookup"><span data-stu-id="be989-113">The **CollectUserInfo** method opens the product's installation package and invokes an authored user interface wizard sequence which collects user information.</span></span> <span data-ttu-id="be989-114">Al termine della sequenza della procedura guidata, le informazioni sull'utente raccolte vengono registrate.</span><span class="sxs-lookup"><span data-stu-id="be989-114">Upon completion of the wizard sequence, the collected user information is registered.</span></span> <span data-ttu-id="be989-115">La proprietà [**UILevel**](installer-uilevel.md) deve essere impostata su msiUILevelFull perché questa API richiede un'interfaccia utente creata.</span><span class="sxs-lookup"><span data-stu-id="be989-115">The [**UILevel**](installer-uilevel.md) property should be set to msiUILevelFull because this API requires an authored user interface.</span></span>

<span data-ttu-id="be989-116">Il metodo **CollectUserInfo** richiama la [finestra di dialogo firstrun](firstrun-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="be989-116">The **CollectUserInfo** method invokes the [FirstRun Dialog](firstrun-dialog.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="be989-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="be989-117">Requirements</span></span>



| <span data-ttu-id="be989-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="be989-118">Requirement</span></span> | <span data-ttu-id="be989-119">Valore</span><span class="sxs-lookup"><span data-stu-id="be989-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be989-120">Versione</span><span class="sxs-lookup"><span data-stu-id="be989-120">Version</span></span><br/> | <span data-ttu-id="be989-121">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="be989-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="be989-122">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="be989-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="be989-123">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="be989-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="be989-124">DLL</span><span class="sxs-lookup"><span data-stu-id="be989-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="be989-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be989-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="be989-126">IID</span><span class="sxs-lookup"><span data-stu-id="be989-126">IID</span></span><br/>     | <span data-ttu-id="be989-127">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="be989-127">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="be989-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="be989-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be989-129">**MsiCollectUserInfo**</span><span class="sxs-lookup"><span data-stu-id="be989-129">**MsiCollectUserInfo**</span></span>](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa)
</dt> </dl>

 

 




