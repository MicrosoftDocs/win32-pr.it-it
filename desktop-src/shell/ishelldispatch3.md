---
description: Estende l'oggetto IShellDispatch2.
ms.assetid: 89d0aa4d-844d-497d-82bb-bcc2bcf9c78b
title: Oggetto IShellDispatch3 (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch3
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 501b1396bd08ad8fd06f25da9b7030d4ce28d1e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978007"
---
# <a name="ishelldispatch3-object"></a>Oggetto IShellDispatch3

Estende l'oggetto [**IShellDispatch2**](ishelldispatch2-object.md) . **IShellDispatch3** supporta un nuovo metodo, oltre alle proprietà e ai metodi supportati da **IShellDispatch2**.

> [!Note]  
> **IShellDispatch3** viene implementato e accessibile tramite l'oggetto [**Shell**](shell.md) .

 

## <a name="members"></a>Membri

L'oggetto **IShellDispatch3** dispone di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'oggetto **IShellDispatch3** dispone di questi metodi.



| Metodo                                             | Descrizione                                                  |
|:---------------------------------------------------|:-------------------------------------------------------------|
| [**AddToRecent**](ishelldispatch3-addtorecent.md) | Aggiunge un file all'elenco degli ultimi elementi usati (MRU).<br/> |



 

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
</dt> </dl>

 

 
