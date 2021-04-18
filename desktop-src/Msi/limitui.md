---
description: Se la proprietà LIMITUI è impostata, il livello di interfaccia utente utilizzato durante l'installazione del pacchetto è limitato a Basic.
ms.assetid: 1a75e66b-958a-4fa8-b13c-ced976c9508e
title: Proprietà LIMITUI
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e564e82a2daba4b6d5a91cb05acd74e1efc26c84
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325029"
---
# <a name="limitui-property"></a><span data-ttu-id="88015-103">Proprietà LIMITUI</span><span class="sxs-lookup"><span data-stu-id="88015-103">LIMITUI property</span></span>

<span data-ttu-id="88015-104">Se la proprietà **LIMITUI** è impostata, il livello di interfaccia utente utilizzato durante l'installazione del pacchetto è limitato a Basic.</span><span class="sxs-lookup"><span data-stu-id="88015-104">If the **LIMITUI** property is set, the user interface (UI) level used when installing the package is restricted to Basic.</span></span> <span data-ttu-id="88015-105">Questa proprietà è obbligatoria nei pacchetti che non dispongono di un'interfaccia utente creata, ma che contengono ancora tabelle dell'interfaccia utente, ad esempio la [tabella della finestra di dialogo](dialog-table.md).</span><span class="sxs-lookup"><span data-stu-id="88015-105">This property is required in packages that have no authored UI but still contain UI tables such as the [Dialog table](dialog-table.md).</span></span> <span data-ttu-id="88015-106">Per una descrizione dei livelli dell'interfaccia utente, vedere [ **MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)</span><span class="sxs-lookup"><span data-stu-id="88015-106">For a description of UI levels, see [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)</span></span>

## <a name="remarks"></a><span data-ttu-id="88015-107">Commenti</span><span class="sxs-lookup"><span data-stu-id="88015-107">Remarks</span></span>

<span data-ttu-id="88015-108">I pacchetti di installazione contenenti la proprietà **LIMITUI** devono anche contenere la proprietà [**ARPNOMODIFY**](arpnomodify.md) .</span><span class="sxs-lookup"><span data-stu-id="88015-108">Installation packages containing the **LIMITUI** property must also contain the [**ARPNOMODIFY**](arpnomodify.md) property.</span></span> <span data-ttu-id="88015-109">Questa operazione è necessaria affinché un utente ottenga il comportamento corretto da **Installazione applicazioni** nell'utilità del **Pannello di controllo** quando si tenta di configurare un prodotto.</span><span class="sxs-lookup"><span data-stu-id="88015-109">This is required for a user to obtain the correct behavior from the **Add or Remove Programs** in the **Control Panel** utility when attempting to configure a product.</span></span>

## <a name="requirements"></a><span data-ttu-id="88015-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="88015-110">Requirements</span></span>



| <span data-ttu-id="88015-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="88015-111">Requirement</span></span> | <span data-ttu-id="88015-112">Valore</span><span class="sxs-lookup"><span data-stu-id="88015-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88015-113">Versione</span><span class="sxs-lookup"><span data-stu-id="88015-113">Version</span></span><br/> | <span data-ttu-id="88015-114">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="88015-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="88015-115">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="88015-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="88015-116">Windows Installer in Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="88015-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="88015-117">Vedere i [requisiti di Run-Time Windows Installer](windows-installer-portal.md) per informazioni sul Service Pack minimo di Windows richiesto da una versione Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="88015-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="88015-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="88015-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88015-119">Proprietà</span><span class="sxs-lookup"><span data-stu-id="88015-119">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="88015-120">**MsiSetInternalUI**</span><span class="sxs-lookup"><span data-stu-id="88015-120">**MsiSetInternalUI**</span></span>](/windows/desktop/api/Msi/nf-msi-msisetinternalui)
</dt> <dt>

[<span data-ttu-id="88015-121">**ARPNOMODIFY**</span><span class="sxs-lookup"><span data-stu-id="88015-121">**ARPNOMODIFY**</span></span>](arpnomodify.md)
</dt> </dl>

 

 




