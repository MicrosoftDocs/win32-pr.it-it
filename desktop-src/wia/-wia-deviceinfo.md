---
description: L'oggetto DeviceInfo fornisce l'accesso alle proprietà di Windows dispositivo hardware WIA (Image Acquisition).
ms.assetid: b3cf153b-76f8-4822-8d88-331ab91a1116
title: Oggetto DeviceInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 69b34a97483a8a6ce231890454148c7948f63e4e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467178"
---
# <a name="deviceinfo-object"></a>Oggetto DeviceInfo

**L'oggetto DeviceInfo** fornisce l'accesso alle proprietà di Windows dispositivo hardware WIA (Image Acquisition). Inoltre, tramite il metodo [**Create,**](-wia-iwiadeviceinfo-create.md) consente all'applicazione o allo script di connettersi al dispositivo e ottenere un [**oggetto Item**](-wia-item.md) che rappresenta il dispositivo. Usare il [**metodo Devices**](-wia-iwia-devices.md) per ottenere una raccolta di **oggetti DeviceInfo.**

## <a name="members"></a>Membri

**L'oggetto DeviceInfo** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto DeviceInfo** dispone di questi metodi.



| Metodo                                                 | Descrizione                                                                                                                                                                                                                                              |
|:-------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Creare**](-wia-iwiadeviceinfo-create.md)           | Il [**metodo Create**](-wia-iwiadeviceinfo-create.md) **dell'oggetto DeviceInfo** esegue una connessione al dispositivo WIA specificato dall'oggetto **DeviceInfo** e restituisce un [**oggetto Item**](-wia-item.md) che rappresenta il dispositivo.<br/> |
| [**GetPropById**](-wia-iwiadeviceinfo-getpropbyid.md) | Il [**metodo GetPropById**](-wia-iwiadeviceinfo-getpropbyid.md) dell'oggetto **DeviceInfo** usa l'ID di una proprietà del dispositivo per restituirne il valore.<br/>                                                                                               |



 

### <a name="properties"></a>Proprietà

**L'oggetto DeviceInfo** ha queste proprietà.




| Proprietà | Tipo di accesso | Descrizione | 
|----------|-------------|-------------|
| <a href="-wia-iwiadeviceinfo-id.md"><strong>Id</strong></a><br /> | Sola lettura<br /> | Recupera l'ID del dispositivo hardware WIA. <br /> | 
| <a href="-wia-iwiadeviceinfo-manufacturer.md"><strong>Produttore</strong></a><br /> | Sola lettura<br /> | Recupera il nome del produttore del dispositivo hardware.<br /> | 
| <a href="-wia-iwiadeviceinfo-name.md"><strong>Nome</strong></a><br /> | Sola lettura<br /> | Nome del dispositivo hardware WIA visualizzato nell'interfaccia utente.<br /> | 
| <a href="-wia-iwiadeviceinfo-port.md"><strong>Porta</strong></a><br /> | Sola lettura<br /> | Recupera la porta a cui è connesso il dispositivo hardware WIA.<br /> | 
| <a href="-wia-iwiadeviceinfo-type.md"><strong>Tipo</strong></a><br /> | Sola lettura<br /> | Recupera il tipo di dispositivo hardware WIA. I valori possibili sono: <br /><ul><li>DigitalCamera</li><li>Scanner</li><li>StreamingVideo</li><li>Predefinito</li></ul> | 
| <a href="-wia-iwiadeviceinfo-uiclsid.md"><strong>UIClsid</strong></a><br /> | Sola lettura<br /> | Recupera l'ID classe dell'interfaccia utente fornita dal produttore per questo dispositivo hardware WIA. Il valore è una rappresentazione di stringa di un GUID. <br /> | 




 

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app desktop XP \[\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (versione 4.90 o successiva)</dt> </dl> |



 

 




