---
description: "Flag utilizzati dai metodi IWiaDevMgr:: GetImageDlg, IWiaDevMgr2:: GetImageDlg, IWiaItem::D eviceDlg e IWiaItem2::D eviceDlg per controllare l'operazione della finestra di dialogo."
ms.assetid: 468a3c9e-64f8-456d-aad9-fa7c6876fbe6
title: WiaFlag (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DEVICE_DIALOG_SINGLE_IMAGE
- WIA_DEVICE_DIALOG_USE_COMMON_UI
- WIA_SELECT_DEVICE_NODEFAULT
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: c906f22e168ca29aadd2e9450fac6225c8b91c17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307294"
---
# <a name="wiaflag"></a><span data-ttu-id="34acd-103">WiaFlag</span><span class="sxs-lookup"><span data-stu-id="34acd-103">WiaFlag</span></span>

<span data-ttu-id="34acd-104">Flag utilizzati dai metodi [**IWiaDevMgr:: GetImageDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg), [**IWiaDevMgr2:: GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md), [**IWiaItem::D eviceDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg)e [**IWiaItem2::D evicedlg**](-wia-iwiaitem2-devicedlg.md) per controllare l'operazione della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="34acd-104">Flags used by the [**IWiaDevMgr::GetImageDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg), [**IWiaDevMgr2::GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md), [**IWiaItem::DeviceDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg), and [**IWiaItem2::DeviceDlg**](-wia-iwiaitem2-devicedlg.md) methods to control the dialog box operation.</span></span>



| <span data-ttu-id="34acd-105">Costante</span><span class="sxs-lookup"><span data-stu-id="34acd-105">Constant</span></span>                                                                                                                                                                                                                | <span data-ttu-id="34acd-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="34acd-106">Description</span></span>                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WIA_DEVICE_DIALOG_SINGLE_IMAGE"></span><span id="wia_device_dialog_single_image"></span><dl> <span data-ttu-id="34acd-107"><dt>**\_ \_ immagine singola della finestra di dialogo del dispositivo WIA \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="34acd-107"><dt>**WIA\_DEVICE\_DIALOG\_SINGLE\_IMAGE**</dt></span></span> </dl>     | <span data-ttu-id="34acd-108">Limitare la selezione delle immagini a una singola immagine nella finestra di dialogo acquisizione immagine del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="34acd-108">Restrict image selection to a single image in the device image acquisition dialog box.</span></span><br/>                                                                                                           |
| <span id="WIA_DEVICE_DIALOG_USE_COMMON_UI"></span><span id="wia_device_dialog_use_common_ui"></span><dl> <span data-ttu-id="34acd-109"><dt>**\_finestra di dialogo del dispositivo WIA usare l' \_ \_ \_ \_ interfaccia utente comune**</dt></span><span class="sxs-lookup"><span data-stu-id="34acd-109"><dt>**WIA\_DEVICE\_DIALOG\_USE\_COMMON\_UI**</dt></span></span> </dl> | <span data-ttu-id="34acd-110">Utilizzare l'interfaccia utente di sistema, se disponibile, anziché l'interfaccia utente fornita dal fornitore.</span><span class="sxs-lookup"><span data-stu-id="34acd-110">Use the system UI, if available, rather than the vendor-supplied UI.</span></span> <span data-ttu-id="34acd-111">Se l'interfaccia utente del sistema non è disponibile, viene utilizzata l'interfaccia utente del fornitore.</span><span class="sxs-lookup"><span data-stu-id="34acd-111">If the system UI is not available, the vendor UI is used.</span></span> <span data-ttu-id="34acd-112">Se nessuna delle due interfacce è disponibile, la funzione restituisce E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="34acd-112">If neither UI is available, the function returns E\_NOTIMPL.</span></span><br/>      |
| <span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span><dl> <span data-ttu-id="34acd-113"><dt>**WIA \_ selezionare il \_ dispositivo \_ NODEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="34acd-113"><dt>**WIA\_SELECT\_DEVICE\_NODEFAULT**</dt></span></span> </dl>               | <span data-ttu-id="34acd-114">Forzare il metodo [**IWiaDevMgr:: GetImageDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg) o [**IWiaDevMgr2:: GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md) per visualizzare la finestra di dialogo **Seleziona dispositivo** .</span><span class="sxs-lookup"><span data-stu-id="34acd-114">Force the [**IWiaDevMgr::GetImageDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg) or [**IWiaDevMgr2::GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md) method to display the **Select Device** dialog box.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="34acd-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="34acd-115">Requirements</span></span>



| <span data-ttu-id="34acd-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="34acd-116">Requirement</span></span> | <span data-ttu-id="34acd-117">Valore</span><span class="sxs-lookup"><span data-stu-id="34acd-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="34acd-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="34acd-118">Minimum supported client</span></span><br/> | <span data-ttu-id="34acd-119">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="34acd-119">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="34acd-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="34acd-120">Minimum supported server</span></span><br/> | <span data-ttu-id="34acd-121">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="34acd-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="34acd-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="34acd-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="34acd-123"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="34acd-123"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




