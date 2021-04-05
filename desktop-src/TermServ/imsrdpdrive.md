---
title: Interfaccia IMsRdpDrive
description: Contiene informazioni su un oggetto unità.
ms.assetid: 25e76657-a898-4581-a866-d66008540f50
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpDrive Servizi Desktop remoto
- Interfaccia IMsRdpDrive Servizi Desktop remoto, descritta
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
ms.openlocfilehash: 032e62ca54d6adccce9b27c8f7e95160c800759b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739991"
---
# <a name="imsrdpdrive-interface"></a>Interfaccia IMsRdpDrive

Contiene informazioni su un oggetto unità.

## <a name="members"></a>Membri

L'interfaccia **IMsRdpDrive** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IMsRdpDrive** dispone anche di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'interfaccia **IMsRdpDrive** ha queste proprietà.



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
| IID<br/>                      | IID \_ IMsRdpDrive è definito come d28b5458-f694-47a8-8e61-40356a767e46<br/>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Riferimento Connessione Web Desktop remoto](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsRdpDriveCollection**](imsrdpdrivecollection.md)
</dt> </dl>

 

