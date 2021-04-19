---
description: La proprietà QualifierDescription di sola lettura restituisce una stringa di testo che descrive il componente completo.
ms.assetid: 43615bd9-824b-4b84-a8f2-eef30cc7619a
title: Proprietà Installer. QualifierDescription
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.QualifierDescription
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8937e0a1fee89bb3ebe1b6402c94778bdd2a0915
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332170"
---
# <a name="installerqualifierdescription-property"></a><span data-ttu-id="df4e6-103">Proprietà Installer. QualifierDescription</span><span class="sxs-lookup"><span data-stu-id="df4e6-103">Installer.QualifierDescription property</span></span>

<span data-ttu-id="df4e6-104">La proprietà **QualifierDescription** di sola lettura restituisce una stringa di testo che descrive il componente completo.</span><span class="sxs-lookup"><span data-stu-id="df4e6-104">The read-only **QualifierDescription** property returns a text string describing the qualified component.</span></span> <span data-ttu-id="df4e6-105">Questa stringa localizzabile viene creata nella colonna AppData della [tabella PublishComponent](publishcomponent-table.md) e può essere visualizzata all'utente.</span><span class="sxs-lookup"><span data-stu-id="df4e6-105">This localizable string is authored into the AppData column of the [PublishComponent table](publishcomponent-table.md) and can be displayed to the user.</span></span> <span data-ttu-id="df4e6-106">Il qualificatore distingue più forme dello stesso componente, ad esempio un componente implementato in più lingue.</span><span class="sxs-lookup"><span data-stu-id="df4e6-106">The qualifier distinguishes multiple forms of the same component, such as a component that is implemented in multiple languages.</span></span>

<span data-ttu-id="df4e6-107">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="df4e6-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="df4e6-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="df4e6-108">Syntax</span></span>


```JScript
propVal = Installer.QualifierDescription
```



## <a name="property-value"></a><span data-ttu-id="df4e6-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="df4e6-109">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="df4e6-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="df4e6-110">Requirements</span></span>



| <span data-ttu-id="df4e6-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="df4e6-111">Requirement</span></span> | <span data-ttu-id="df4e6-112">Valore</span><span class="sxs-lookup"><span data-stu-id="df4e6-112">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df4e6-113">Versione</span><span class="sxs-lookup"><span data-stu-id="df4e6-113">Version</span></span><br/> | <span data-ttu-id="df4e6-114">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="df4e6-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="df4e6-115">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="df4e6-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="df4e6-116">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="df4e6-116">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="df4e6-117">DLL</span><span class="sxs-lookup"><span data-stu-id="df4e6-117">DLL</span></span><br/>     | <dl> <span data-ttu-id="df4e6-118"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df4e6-118"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="df4e6-119">IID</span><span class="sxs-lookup"><span data-stu-id="df4e6-119">IID</span></span><br/>     | <span data-ttu-id="df4e6-120">IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="df4e6-120">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



## <a name="see-also"></a><span data-ttu-id="df4e6-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="df4e6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df4e6-122">**MsiEnumComponentQualifiers**</span><span class="sxs-lookup"><span data-stu-id="df4e6-122">**MsiEnumComponentQualifiers**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)
</dt> <dt>

[<span data-ttu-id="df4e6-123">Componenti qualificati</span><span class="sxs-lookup"><span data-stu-id="df4e6-123">Qualified Components</span></span>](qualified-components.md)
</dt> </dl>

 

 




