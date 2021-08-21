---
title: Interfaccia IMsRdpDrive
description: Contiene informazioni su un oggetto unità.
ms.assetid: 25e76657-a898-4581-a866-d66008540f50
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpDrive Servizi Desktop remoto
- Interfaccia IMsRdpDrive Servizi Desktop remoto , descritta
topic_type:
- apiref
api_name:
- IMsRdpDrive
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3efccf0459375e23375b3ac40067bcbd3965ed7f6c0b51ddb60f6362fb419688
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000731"
---
# <a name="imsrdpdrive-interface"></a>Interfaccia IMsRdpDrive

Contiene informazioni su un oggetto unità.

## <a name="members"></a>Membri

**L'interfaccia IMsRdpDrive** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IMsRdpDrive** include anche questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

Queste proprietà sono disponibili nell'interfaccia **IMsRdpDrive.**



| Proprietà                                                            | Tipo di accesso           | Descrizione                                              |
|:--------------------------------------------------------------------|:----------------------|:---------------------------------------------------------|
| [**Nome**](imsrdpdrive-name.md)<br/>                         | Sola lettura<br/>  | Recupera il nome dell'unità.<br/>              |
| [**RedirectionState**](imsrdpdrive-redirectionstate.md)<br/> | Lettura/Scrittura<br/> | Indica lo stato di reindirizzamento dell'unità.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IMsRdpDrive IID è definito come \_ d28b5458-f694-47a8-8e61-40356a767e46<br/>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Connessione Web Desktop remoto riferimento](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsRdpDriveCollection**](imsrdpdrivecollection.md)
</dt> </dl>

 

