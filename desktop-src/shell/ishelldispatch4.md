---
description: Estende l'oggetto IShellDispatch3.
title: Oggetto IShellDispatch4 (Shldisp.h)
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
ms.openlocfilehash: daec9c922a0bac05154c1108f236ddf336a2e380
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843062"
---
# <a name="ishelldispatch4-object"></a>Oggetto IShellDispatch4

Estende [**l'oggetto IShellDispatch3.**](ishelldispatch3.md) Oltre alle proprietà e ai metodi supportati da **IShellDispatch3,** **IShellDispatch4** supporta quattro metodi aggiuntivi.

> [!Note]  
> **IShellDispatch4 viene** implementato e accessibile tramite [**l'oggetto Shell.**](shell.md)

 

## <a name="members"></a>Membri

**L'oggetto IShellDispatch4** ha questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'oggetto IShellDispatch4** dispone di questi metodi.



| Metodo                                                     | Descrizione                                                         |
|:-----------------------------------------------------------|:--------------------------------------------------------------------|
| [**ExplorerPolicy**](ishelldispatch4-explorerpolicy.md)   | Ottiene il valore per un criterio di Internet Explorer specificati.<br/> |
| [**GetSetting**](ishelldispatch4-getsetting.md)           | Recupera un'impostazione shell globale.<br/>                        |
| [**ToggleDesktop**](ishelldispatch4-toggledesktop.md)     | Visualizza o nasconde il desktop.<br/>                           |
| [**Sicurezza di Windows**](ishelldispatch4-windowssecurity.md) | Consente di visualizzare **Sicurezza di Windows** finestra di dialogo.<br/>            |



 

## <a name="remarks"></a>Commenti

Per una descrizione dei servizi Windows, vedere la [documentazione relativa ai](../services/services.md) servizi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop di Windows XP \[\]<br/>                                                                   |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 6.0 o successiva)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Idispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[**Oggetto shell**](shell.md)
</dt> <dt>

[**IShellDispatch**](ishelldispatch.md)
</dt> <dt>

[**IShellDispatch2**](ishelldispatch2-object.md)
</dt> <dt>

[**IShellDispatch3**](ishelldispatch3.md)
</dt> </dl>

 

 
