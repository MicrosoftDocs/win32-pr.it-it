---
description: Il metodo OpenPackage dell'oggetto Installer apre un pacchetto di installazione da usare con funzioni che accedono al database del prodotto e installano il motore, restituendo un oggetto Session.
ms.assetid: 22b03bde-29ae-4dd4-a41c-d55b3a4f424c
title: Installer. OpenPackage, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.OpenPackage
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 621fac51155b2ac89eba40d39da6d5af6c305e67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324607"
---
# <a name="installeropenpackage-method"></a><span data-ttu-id="80205-103">Installer. OpenPackage, metodo</span><span class="sxs-lookup"><span data-stu-id="80205-103">Installer.OpenPackage method</span></span>

<span data-ttu-id="80205-104">Il metodo **OpenPackage** dell'oggetto [**Installer**](installer-object.md) apre un pacchetto di installazione da usare con funzioni che accedono al database del prodotto e installano il motore, restituendo un oggetto [**Session**](session-object.md) .</span><span class="sxs-lookup"><span data-stu-id="80205-104">The **OpenPackage** method of the [**Installer**](installer-object.md) object opens an installer package for use with functions that access the product database and install engine, returning an [**Session**](session-object.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="80205-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="80205-105">Syntax</span></span>


```JScript
Installer.OpenPackage(
  packagePath,
  options
)
```



## <a name="parameters"></a><span data-ttu-id="80205-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="80205-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80205-107">*packagePath*</span><span class="sxs-lookup"><span data-stu-id="80205-107">*packagePath*</span></span> 
</dt> <dd>

<span data-ttu-id="80205-108">Stringa obbligatoria contenente il nome del percorso del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="80205-108">Required string containing the path name of the package.</span></span>

</dd> <dt>

<span data-ttu-id="80205-109">*options*</span><span class="sxs-lookup"><span data-stu-id="80205-109">*options*</span></span> 
</dt> <dd>

<span data-ttu-id="80205-110">Valore integer facoltativo che specifica se **OpenPackage** deve ignorare lo stato corrente del computer durante la creazione dell'oggetto sessione.</span><span class="sxs-lookup"><span data-stu-id="80205-110">An optional integer value that specifies whether or not **OpenPackage** should ignore the current computer state when creating the Session object.</span></span> <span data-ttu-id="80205-111">Nessun valore o un valore pari a 0 per le opzioni per impostazione predefinita è il comportamento originale.</span><span class="sxs-lookup"><span data-stu-id="80205-111">No value or a value of 0 for options defaults to the original behavior.</span></span> <span data-ttu-id="80205-112">Quando options è 1, il metodo **OpenPackage** ignora lo stato corrente del computer all'apertura del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="80205-112">When options is 1, the **OpenPackage** Method ignores the current computer state when opening the package.</span></span> <span data-ttu-id="80205-113">Il valore 1 impedisce le modifiche allo stato corrente del computer.</span><span class="sxs-lookup"><span data-stu-id="80205-113">A value of 1 prevents changes to the current computer state.</span></span> <span data-ttu-id="80205-114">Per ulteriori informazioni, vedere [**MsiOpenPackageEx**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa).</span><span class="sxs-lookup"><span data-stu-id="80205-114">For more information, see [**MsiOpenPackageEx**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80205-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="80205-115">Return value</span></span>

<span data-ttu-id="80205-116">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="80205-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="80205-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="80205-117">Remarks</span></span>

<span data-ttu-id="80205-118">Il metodo **OpenPackage** può accettare direttamente l'handle di database anziché la stringa per il percorso del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="80205-118">The **OpenPackage** method can accept the database handle directly instead of the string for the package path.</span></span>

<span data-ttu-id="80205-119">Si noti che solo un oggetto [**sessione**](session-object.md) può essere aperto da un singolo processo.</span><span class="sxs-lookup"><span data-stu-id="80205-119">Note that only one [**Session**](session-object.md) object can be opened by a single process.</span></span> <span data-ttu-id="80205-120">Non è possibile usare **OpenPackage** in un'azione personalizzata perché l'installazione attiva è l'unica sessione consentita.</span><span class="sxs-lookup"><span data-stu-id="80205-120">**OpenPackage** cannot be used in a custom action because the active installation is the only session allowed.</span></span>

<span data-ttu-id="80205-121">Un oggetto [**sessione**](session-object.md) sicuro ignora lo stato corrente del computer quando si apre il pacchetto e impedisce le modifiche allo stato corrente del computer.</span><span class="sxs-lookup"><span data-stu-id="80205-121">A safe [**Session**](session-object.md) object ignores the current computer state when opening the package and prevents changes to the current computer state.</span></span> <span data-ttu-id="80205-122">Per ulteriori informazioni, vedere [**MsiOpenPackageEx**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa).</span><span class="sxs-lookup"><span data-stu-id="80205-122">For more information, see [**MsiOpenPackageEx**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa).</span></span>

## <a name="requirements"></a><span data-ttu-id="80205-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="80205-123">Requirements</span></span>



| <span data-ttu-id="80205-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="80205-124">Requirement</span></span> | <span data-ttu-id="80205-125">Valore</span><span class="sxs-lookup"><span data-stu-id="80205-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80205-126">Versione</span><span class="sxs-lookup"><span data-stu-id="80205-126">Version</span></span><br/> | <span data-ttu-id="80205-127">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="80205-127">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="80205-128">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="80205-128">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="80205-129">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="80205-129">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="80205-130">DLL</span><span class="sxs-lookup"><span data-stu-id="80205-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="80205-131"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80205-131"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="80205-132">IID</span><span class="sxs-lookup"><span data-stu-id="80205-132">IID</span></span><br/>     | <span data-ttu-id="80205-133">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="80205-133">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




