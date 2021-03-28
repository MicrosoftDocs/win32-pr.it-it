---
description: Estende l'oggetto IShellDispatch3.
title: Oggetto IShellDispatch4 (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 4fe37e38-ee71-41f0-b620-35fdc18f9dbb
ms.openlocfilehash: 0bdada12a48f9c48749b614e6b45ff5427e62b4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527324"
---
# <a name="ishelldispatch4-object"></a>Oggetto IShellDispatch4

Estende l'oggetto [**IShellDispatch3**](ishelldispatch3.md) . Oltre alle proprietà e ai metodi supportati da **IShellDispatch3**, **IShellDispatch4** supporta quattro metodi aggiuntivi.

> [!Note]  
> **IShellDispatch4** viene implementato e accessibile tramite l'oggetto [**Shell**](shell.md) .

 

## <a name="members"></a>Membri

L'oggetto **IShellDispatch4** dispone di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'oggetto **IShellDispatch4** dispone di questi metodi.



| Metodo                                                     | Descrizione                                                         |
|:-----------------------------------------------------------|:--------------------------------------------------------------------|
| [**ExplorerPolicy**](ishelldispatch4-explorerpolicy.md)   | Ottiene il valore per i criteri di Internet Explorer specificati.<br/> |
| [**GetSetting**](ishelldispatch4-getsetting.md)           | Recupera un'impostazione della shell globale.<br/>                        |
| [**ToggleDesktop**](ishelldispatch4-toggledesktop.md)     | Consente di visualizzare o nascondere il desktop.<br/>                           |
| [**WindowsSecurity**](ishelldispatch4-windowssecurity.md) | Consente di visualizzare la finestra di dialogo **sicurezza di Windows** .<br/>            |



 

## <a name="remarks"></a>Commenti

Per informazioni sui servizi Windows, vedere la documentazione relativa ai [Servizi](../services/services.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                                                   |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 6,0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[**Oggetto Shell**](shell.md)
</dt> <dt>

[**IShellDispatch**](ishelldispatch.md)
</dt> <dt>

[**IShellDispatch2**](ishelldispatch2-object.md)
</dt> <dt>

[**IShellDispatch3**](ishelldispatch3.md)
</dt> </dl>

 

 
