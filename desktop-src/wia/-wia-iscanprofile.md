---
description: L'interfaccia IScanProfile rappresenta un singolo profilo di analisi e consente alle applicazioni di impostare e ottenere le proprietà del profilo.
ms.assetid: 5cd76256-d64e-4934-8cc2-0a467c7e34a9
title: Interfaccia IScanProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile
api_type:
- COM
api_location:
- Scanprofiles.idl
ms.openlocfilehash: 2e02352eef16a9b899e4c635f11c5d10b3ab5113
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312432"
---
# <a name="iscanprofile-interface"></a>Interfaccia IScanProfile

L'interfaccia **IScanProfile** rappresenta un singolo profilo di analisi e consente alle applicazioni di impostare e ottenere le proprietà del profilo.

## <a name="members"></a>Membri

L'interfaccia **IScanProfile** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IScanProfile** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IScanProfile** dispone di questi metodi.



| Metodo                                                     | Descrizione                                                                                                                                         |
|:-----------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetAllPropIDs**](-wia-iscanprofile-getallpropids.md)   | Ottiene tutti gli ID di proprietà disponibili in un profilo.<br/>                                                                                            |
| [**GetDeviceID**](-wia-iscanprofile-getdeviceid.md)       | Restituisce l'ID del dispositivo.<br/>                                                                                                            |
| [**GetGUID**](-wia-iscanprofile-getguid.md)               | Restituisce il GUID del profilo.<br/>                                                                                                         |
| [**GetItem**](-wia-iscanprofile-getitem.md)               | Ottiene il GUID della categoria dell'elemento WIA 2,0 a cui è associato il profilo.<br/>                                                   |
| [**GetName**](-wia-iscanprofile-getname.md)               | Ottiene il nome descrittivo del profilo.<br/>                                                                                                   |
| [**GetNumPropIDS**](-wia-iscanprofile-getnumpropids.md)   | Ottiene il numero di ID di proprietà in un profilo.<br/>                                                                                            |
| [**GetProperty**](-wia-iscanprofile-getproperty.md)       | Ottiene il valore delle proprietà figlio specificate nell' `<Properties>` elemento di un profilo di analisi.<br/>                                            |
| [**IsDefault**](-wia-iscanprofile-isdefault.md)           | Ottiene un valore che indica se il profilo è il profilo di analisi predefinito di un dispositivo [**IWiaItem2**](-wia-iwiaitem2.md) associato.<br/> |
| [**RemoveProperty**](-wia-iscanprofile-removeproperty.md) | Rimuove un elenco specificato di proprietà figlio nell' `<Properties>` elemento di un profilo di analisi.<br/>                                            |
| [**Salva**](-wia-iscanprofile-save.md)                     | Salva le modifiche apportate a un profilo su disco.<br/>                                                                                                      |
| [**SetItem**](-wia-iscanprofile-setitem.md)               | Imposta il GUID della categoria dell'elemento WIA 2,0 a cui è associato il profilo.<br/>                                                       |
| [**SetName**](-wia-iscanprofile-setname.md)               | Imposta il nome descrittivo del profilo.<br/>                                                                                                   |
| [**SetProperty**](-wia-iscanprofile-setproperty.md)       | Imposta il valore delle proprietà figlio specificate nell' `<Properties>` elemento di un profilo di analisi.<br/>                                            |



 

## <a name="remarks"></a>Commenti

Qualsiasi dispositivo [**IWiaItem2**](-wia-iwiaitem2.md) può avere un profilo di analisi. Tuttavia, gli elementi di **IWiaItem2** di tipo WIA \_ Category \_ finished \_ file e WIA \_ Category \_ root non possono avere profili.

Se un profilo di analisi viene salvato utilizzando il metodo [**IScanProfile:: Save**](-wia-iscanprofile-save.md) , viene archiviato come file XML in% UserProfile% \\ Application Data \\ Microsoft \\ Document Center \\ UserScanProfiles.

Per creare un'istanza di un oggetto **IScanProfile** , usare il metodo [**IScanProfileMgr:: CreateProfile**](-wia-iscanprofilemgr-createprofile.md) . Per ottenere un riferimento a un profilo di analisi che è già stato salvato su disco, usare il metodo [**IScanProfileMgr:: OpenProfile**](-wia-iscanprofilemgr-openprofile.md) .

Tutti i profili di analisi hanno gli elementi seguenti: `<ProfileGUID>, <DeviceID>, <ProfileName>, <WiaItem>` , e `<Properties>` . Il profilo predefinito di un dispositivo contiene anche un `<Default>` elemento.

Gli `<ProfileGUID>` `<DeviceID>` elementi e non possono essere modificati dopo la creazione del profilo. I valori dell' `<ProfileName>` elemento e dell' `<WiaItem>` elemento possono essere modificati dopo la creazione del profilo. L' `<Default>` elemento può essere aggiunto o eliminato. Questa operazione può essere eseguita a livello con i metodi [**IScanProfile:: Sename**](-wia-iscanprofile-setname.md), [**IScanProfile:: SetItem**](-wia-iscanprofile-setitem.md)e [**IScanProfileMgr:: sedefault**](-wia-iscanprofilemgr-setdefault.md) . Queste proprietà possono anche essere modificate dagli utenti tramite il metodo [**IScanProfileUI:: ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) .

L' `<Properties>` elemento contiene `<Property>` elementi figlio. Usare questi elementi per aggiungere qualsiasi proprietà dell'elemento o del dispositivo WIA 2,0 al profilo. È anche possibile sviluppare una propria immagine acquisizione `<Property>` Children. In questo modo lo schema del profilo di analisi diventa estendibile. Per ulteriori informazioni sull'estensione dello schema, vedere [definizione di proprietà personalizzate](-wia-defining-custom-properties.md), [**IScanProfile:: GetProperty**](-wia-iscanprofile-getproperty.md)e [**IScanProfile:: SetProperty**](-wia-iscanprofile-setproperty.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                        |
| IDL<br/>                      | <dl> <dt>Scanprofiles. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Schema del profilo di analisi](-wia-scan-profile-schema.md)
</dt> </dl>

 

 
