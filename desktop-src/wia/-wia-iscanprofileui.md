---
description: L'interfaccia IScanProfileUI consente alle applicazioni di visualizzare una finestra di dialogo in modo che gli utenti possano creare, modificare ed eliminare i profili di analisi.
ms.assetid: d0c7edcc-00d8-49b2-a0f7-fe4bbba90bfb
title: Interfaccia IScanProfileUI (Scanprofileui. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileUI
api_type:
- COM
api_location:
- Scanprofileui.h
ms.openlocfilehash: c8791461db76c72de81216aef188886f63fde4f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308248"
---
# <a name="iscanprofileui-interface"></a>Interfaccia IScanProfileUI

L'interfaccia **IScanProfileUI** consente alle applicazioni di visualizzare una finestra di dialogo in modo che gli utenti possano creare, modificare ed eliminare i profili di analisi.

## <a name="members"></a>Membri

L'interfaccia **IScanProfileUI** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IScanProfileUI** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IScanProfileUI** dispone di questi metodi.



| Metodo                                                             | Descrizione                                                                                      |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) | Visualizza una finestra di dialogo che consente agli utenti di creare, modificare ed eliminare i profili di analisi.<br/> |



 

## <a name="remarks"></a>Commenti

La finestra di dialogo è modale. l'utente non può passare alla finestra padre fino alla chiusura della finestra di dialogo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>Scanprofileui. h</dt> </dl>  |
| IDL<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Schema del profilo di analisi](-wia-scan-profile-schema.md)
</dt> </dl>

 

 
