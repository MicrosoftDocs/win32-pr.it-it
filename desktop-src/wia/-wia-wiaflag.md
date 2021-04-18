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
# <a name="wiaflag"></a>WiaFlag

Flag utilizzati dai metodi [**IWiaDevMgr:: GetImageDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg), [**IWiaDevMgr2:: GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md), [**IWiaItem::D eviceDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg)e [**IWiaItem2::D evicedlg**](-wia-iwiaitem2-devicedlg.md) per controllare l'operazione della finestra di dialogo.



| Costante                                                                                                                                                                                                                | Descrizione                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WIA_DEVICE_DIALOG_SINGLE_IMAGE"></span><span id="wia_device_dialog_single_image"></span><dl> <dt>**\_ \_ immagine singola della finestra di dialogo del dispositivo WIA \_ \_**</dt> </dl>     | Limitare la selezione delle immagini a una singola immagine nella finestra di dialogo acquisizione immagine del dispositivo.<br/>                                                                                                           |
| <span id="WIA_DEVICE_DIALOG_USE_COMMON_UI"></span><span id="wia_device_dialog_use_common_ui"></span><dl> <dt>**\_finestra di dialogo del dispositivo WIA usare l' \_ \_ \_ \_ interfaccia utente comune**</dt> </dl> | Utilizzare l'interfaccia utente di sistema, se disponibile, anziché l'interfaccia utente fornita dal fornitore. Se l'interfaccia utente del sistema non è disponibile, viene utilizzata l'interfaccia utente del fornitore. Se nessuna delle due interfacce è disponibile, la funzione restituisce E \_ NOTIMPL.<br/>      |
| <span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span><dl> <dt>**WIA \_ selezionare il \_ dispositivo \_ NODEFAULT**</dt> </dl>               | Forzare il metodo [**IWiaDevMgr:: GetImageDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg) o [**IWiaDevMgr2:: GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md) per visualizzare la finestra di dialogo **Seleziona dispositivo** .<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 




