---
title: UI_ALL_COMMANDS (UIRibbon. h)
description: Specifica una costante che identifica la raccolta di comandi dichiarati nel file di risorse di markup.
ms.assetid: b0046d8c-bb54-4231-90f0-c0b2c8790b1a
topic_type:
- apiref
api_name:
- UI_ALL_COMMANDS
api_location:
- Uiribbon.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cce287d6ee03734ecbb0dd84e020ec542a83f04b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301399"
---
# <a name="ui_all_commands"></a><span data-ttu-id="a0b92-103">\_tutti i comandi dell'interfaccia utente \_</span><span class="sxs-lookup"><span data-stu-id="a0b92-103">UI\_ALL\_COMMANDS</span></span>

<span data-ttu-id="a0b92-104">Specifica una costante che identifica la raccolta di comandi dichiarati nel file di risorse di markup.</span><span class="sxs-lookup"><span data-stu-id="a0b92-104">Specifies a constant that identifies the collection of Commands declared in the Markup resource file.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0b92-105">Commenti</span><span class="sxs-lookup"><span data-stu-id="a0b92-105">Remarks</span></span>

<span data-ttu-id="a0b92-106">**Interfaccia utente \_ TUTTI i \_ comandi** sono utili quando è necessario accedere a proprietà simili in tutti i comandi.</span><span class="sxs-lookup"><span data-stu-id="a0b92-106">**UI\_ALL\_COMMANDS** is useful when it is necessary to access similar properties across all Commands.</span></span> <span data-ttu-id="a0b92-107">Ad esempio, **\_ tutti i \_ comandi dell'interfaccia utente** possono essere passati a [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) per invalidare e aggiornare tutti i comandi della barra multifunzione eseguendo una query sull'applicazione host per i nuovi valori delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="a0b92-107">For example, **UI\_ALL\_COMMANDS** can be passed to [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) to invalidate and refresh all Ribbon Commands by querying the host application for new property values.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0b92-108">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a0b92-108">Requirements</span></span>



| <span data-ttu-id="a0b92-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0b92-109">Requirement</span></span> | <span data-ttu-id="a0b92-110">Valore</span><span class="sxs-lookup"><span data-stu-id="a0b92-110">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0b92-111">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0b92-111">Minimum supported client</span></span><br/> | <span data-ttu-id="a0b92-112">Windows 7, Windows Vista con SP2 e aggiornamento della piattaforma solo per le applicazioni desktop di Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="a0b92-112">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a0b92-113">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a0b92-113">Minimum supported server</span></span><br/> | <span data-ttu-id="a0b92-114">Windows Server 2008 R2, Windows Server 2008 con SP2 e aggiornamento della piattaforma solo per le \[ app desktop Windows server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a0b92-114">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a0b92-115">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a0b92-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="a0b92-116"><dt>UIRibbon. h</dt></span><span class="sxs-lookup"><span data-stu-id="a0b92-116"><dt>Uiribbon.h</dt></span></span> </dl>                                             |
| <span data-ttu-id="a0b92-117">IDL</span><span class="sxs-lookup"><span data-stu-id="a0b92-117">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a0b92-118"><dt>UIRibbon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a0b92-118"><dt>Uiribbon.idl</dt></span></span> </dl>                                           |



## <a name="see-also"></a><span data-ttu-id="a0b92-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a0b92-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0b92-120">Costanti ed enumerazioni</span><span class="sxs-lookup"><span data-stu-id="a0b92-120">Constants and Enumerations</span></span>](windowsribbon-reference-enumerations.md)
</dt> </dl>

 

