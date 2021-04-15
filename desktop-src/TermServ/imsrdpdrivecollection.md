---
title: Interfaccia IMsRdpDriveCollection
description: Rappresenta una raccolta di oggetti unità.
ms.assetid: 26926b85-021d-4678-845f-93ba62b2b4a3
ms.tgt_platform: multiple
keywords:
- Interfaccia IMsRdpDriveCollection Servizi Desktop remoto
- Interfaccia IMsRdpDriveCollection Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7b2588ddb0945ba1fcab8fbb4c5b9b078a1af9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477735"
---
# <a name="imsrdpdrivecollection-interface"></a>Interfaccia IMsRdpDriveCollection

Rappresenta una raccolta di oggetti unità.

## <a name="members"></a>Membri

L'interfaccia **IMsRdpDriveCollection** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IMsRdpDriveCollection** dispone anche di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'interfaccia **IMsRdpDriveCollection** dispone di questi metodi.



| Metodo                                                     | Descrizione                                                 |
|:-----------------------------------------------------------|:------------------------------------------------------------|
| [**RescanDrives**](imsrdpdrivecollection-rescandrives.md) | Aggiorna l'elenco di oggetti nella raccolta.<br/> |



 

### <a name="properties"></a>Proprietà

L'interfaccia **IMsRdpDriveCollection** ha queste proprietà.



| Proprietà                                                              | Tipo di accesso          | Descrizione                                                  |
|:----------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------|
| [**DriveByIndex**](imsrdpdrivecollection-drivebyindex.md)<br/> | Sola lettura<br/> | Recupera l'unità in corrispondenza dell'indice specificato.<br/>       |
| [**DriveCount**](imsrdpdrivecollection-drivecount.md)<br/>     | Sola lettura<br/> | Recupera il numero di oggetti nella raccolta.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                           |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IID \_ IMsRdpDriveCollection è definito come 7ff17599-da2c-4677-Ad35-f60c04fe1585<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Riferimento Connessione Web Desktop remoto](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsRdpDrive**](imsrdpdrive.md)
</dt> </dl>

 

