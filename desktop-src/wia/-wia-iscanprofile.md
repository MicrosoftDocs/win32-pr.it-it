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
ms.openlocfilehash: 1de80ac23ffa3e2687e2e6d0449f7a273067d5899204c479f9b62e8571190d61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119450831"
---
# <a name="iscanprofile-interface"></a>Interfaccia IScanProfile

**L'interfaccia IScanProfile** rappresenta un singolo profilo di analisi e consente alle applicazioni di impostare e ottenere le proprietà del profilo.

## <a name="members"></a>Membri

**L'interfaccia IScanProfile** eredita dall'interfaccia [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IScanProfile** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IScanProfile** include questi metodi.



| Metodo                                                     | Descrizione                                                                                                                                         |
|:-----------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetAllPropIDs**](-wia-iscanprofile-getallpropids.md)   | Ottiene tutti gli ID proprietà disponibili in un profilo.<br/>                                                                                            |
| [**GetDeviceID**](-wia-iscanprofile-getdeviceid.md)       | Restituisce l'ID del dispositivo.<br/>                                                                                                            |
| [**GetGUID**](-wia-iscanprofile-getguid.md)               | Restituisce il GUID del profilo.<br/>                                                                                                         |
| [**GetItem**](-wia-iscanprofile-getitem.md)               | Ottiene il GUID della categoria dell'elemento WIA 2.0 a cui è associato il profilo.<br/>                                                   |
| [**GetName**](-wia-iscanprofile-getname.md)               | Ottiene il nome descrittivo del profilo.<br/>                                                                                                   |
| [**GetNumPropIDS**](-wia-iscanprofile-getnumpropids.md)   | Ottiene il numero di ID proprietà in un profilo.<br/>                                                                                            |
| [**Getproperty**](-wia-iscanprofile-getproperty.md)       | Ottiene il valore delle proprietà figlio specificate `<Properties>` nell'elemento di un profilo di analisi.<br/>                                            |
| [**IsDefault**](-wia-iscanprofile-isdefault.md)           | Ottiene un valore che indica se il profilo è il profilo di analisi predefinito di un [**dispositivo IWiaItem2**](-wia-iwiaitem2.md) associato.<br/> |
| [**RemoveProperty**](-wia-iscanprofile-removeproperty.md) | Rimuove un elenco specificato di proprietà figlio `<Properties>` nell'elemento di un profilo di analisi.<br/>                                            |
| [**Salva**](-wia-iscanprofile-save.md)                     | Salva le modifiche apportate a un profilo su disco.<br/>                                                                                                      |
| [**SetItem**](-wia-iscanprofile-setitem.md)               | Imposta il GUID della categoria dell'elemento WIA 2.0 a cui è associato il profilo.<br/>                                                       |
| [**SetName**](-wia-iscanprofile-setname.md)               | Imposta il nome descrittivo del profilo.<br/>                                                                                                   |
| [**SetProperty**](-wia-iscanprofile-setproperty.md)       | Imposta il valore delle proprietà figlio specificate `<Properties>` nell'elemento di un profilo di analisi.<br/>                                            |



 

## <a name="remarks"></a>Commenti

Qualsiasi [**dispositivo IWiaItem2**](-wia-iwiaitem2.md) può avere un profilo di analisi. Tuttavia, **gli elementi IWiaItem2** di tipo WIA \_ CATEGORY FINISHED FILE e \_ \_ WIA CATEGORY \_ ROOT non possono \_ avere profili.

Se un profilo di analisi viene salvato usando il [**metodo IScanProfile::Save,**](-wia-iscanprofile-save.md) viene archiviato come file XML in %USERPROFILE% \\ Application Data Microsoft Document Center \\ \\ \\ UserScanProfiles.

Per creare un'istanza di **un oggetto IScanProfile,** usare il [**metodo IScanProfileMgr::CreateProfile.**](-wia-iscanprofilemgr-createprofile.md) Per ottenere un riferimento a un profilo di analisi già salvato su disco, usare il [**metodo IScanProfileMgr::OpenProfile.**](-wia-iscanprofilemgr-openprofile.md)

Tutti i profili di analisi hanno gli elementi seguenti: `<ProfileGUID>, <DeviceID>, <ProfileName>, <WiaItem>` e `<Properties>` . Anche il profilo predefinito di un dispositivo ha un `<Default>` elemento .

Gli `<ProfileGUID>` elementi e non possono essere modificati dopo la creazione del `<DeviceID>` profilo. I valori `<ProfileName>` dell'elemento e `<WiaItem>` dell'elemento possono essere modificati dopo la creazione del profilo. `<Default>`L'elemento può essere aggiunto o eliminato. Questa operazione può essere eseguita a livello di codice con i metodi [**IScanProfile::SetName**](-wia-iscanprofile-setname.md), [**IScanProfile::SetItem**](-wia-iscanprofile-setitem.md)e [**IScanProfileMgr::SetDefault.**](-wia-iscanprofilemgr-setdefault.md) Queste proprietà possono anche essere modificate dagli utenti tramite il [**metodo IScanProfileUI::ScanProfileDialog.**](-wia-iscanprofileui-scanprofiledialog.md)

`<Properties>`L'elemento contiene `<Property>` elementi figlio. Usare questi elementi per aggiungere qualsiasi elemento o proprietà del dispositivo WIA 2.0 al profilo. È anche possibile sviluppare un'immagine personalizzata per gli elementi `<Property>` figlio. In questo modo lo schema del profilo di analisi è estensibile. Per altre informazioni sull'estensione dello schema, vedere [Definizione di](-wia-defining-custom-properties.md)proprietà personalizzate, [**IScanProfile::GetProperty**](-wia-iscanprofile-getproperty.md)e [**IScanProfile::SetProperty.**](-wia-iscanprofile-setproperty.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                        |
| Idl<br/>                      | <dl> <dt>Scanprofiles.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Idispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Schema del profilo di analisi](-wia-scan-profile-schema.md)
</dt> </dl>

 

 
