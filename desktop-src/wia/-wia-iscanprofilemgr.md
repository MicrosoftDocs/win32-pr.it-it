---
description: L'interfaccia IScanProfileMgr fornisce metodi per la creazione, l'apertura, l'eliminazione e la gestione dei profili di analisi.
ms.assetid: f57a71b7-750c-42a8-be73-229f0145d9d5
title: Interfaccia IScanProfileMgr (Scanprofilemgr.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: d2d517143a55c2bd732bb8f9c642697a7d50151ddb72fcffd13d978caef597b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593091"
---
# <a name="iscanprofilemgr-interface"></a>Interfaccia IScanProfileMgr

**L'interfaccia IScanProfileMgr** fornisce metodi per la creazione, l'apertura, l'eliminazione e la gestione dei profili di analisi.

## <a name="members"></a>Membri

**L'interfaccia IScanProfileMgr** eredita dall'interfaccia [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IScanProfileMgr** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **IScanProfileMgr.**



| Metodo                                                                              | Descrizione                                                                                                            |
|:------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [**Creare un profilo**](-wia-iscanprofilemgr-createprofile.md)                         | Crea un profilo di analisi vuoto e lo associa a uno scanner o a un altro elemento WIA 2.0.<br/>                       |
| [**DeleteAllProfiles**](-wia-iscanprofilemgr-deleteallprofiles.md)                 | Elimina tutti i profili di analisi associati al dispositivo specificato.<br/>                                         |
| [**DeleteAllProfilesForUser**](-wia-iscanprofilemgr-deleteallprofilesforuser.md)   | Elimina tutti i profili di analisi disponibili per l'utente nel sistema in cui è in esecuzione l'applicazione. <br/> |
| [**DeleteProfile**](-wia-iscanprofilemgr-deleteprofile.md)                         | Elimina il profilo di analisi specificato.<br/>                                                                         |
| [**GetDefaultProfile**](-wia-iscanprofilemgr-getdefaultprofile.md)                 | Ottiene il profilo di analisi predefinito.<br/>                                                                              |
| [**GetNumProfiles**](-wia-iscanprofilemgr-getnumprofiles.md)                       | Ottiene il numero di profili di analisi creati per l'utente nel sistema in cui è in esecuzione l'applicazione.<br/> |
| [**GetNumProfilesforDeviceID**](-wia-iscanprofilemgr-getnumprofilesfordeviceid.md) | Ottiene il numero di profili di analisi per il dispositivo.<br/>                                                            |
| [**GetProfiles**](-wia-iscanprofilemgr-getprofiles.md)                             | Ottiene tutti i profili di analisi disponibili per l'utente nel sistema in cui è in esecuzione l'applicazione.<br/>     |
| [**GetProfilesforDeviceID**](-wia-iscanprofilemgr-getprofilesfordeviceid.md)       | Ottiene tutti i profili di analisi associati a un dispositivo.<br/>                                                        |
| [**OpenProfile**](-wia-iscanprofilemgr-openprofile.md)                             | Apre un profilo di analisi salvato su disco come file XML.<br/>                                            |
| [**Aggiorna**](-wia-iscanprofilemgr-refresh.md)                                     | Enumera nuovamente tutti i profili di analisi nel sistema.<br/>                                                          |
| [**SetDefault**](-wia-iscanprofilemgr-setdefault.md)                               | Imposta il profilo di analisi specificato come profilo predefinito.<br/>                                                     |



 

## <a name="remarks"></a>Commenti

Per creare un **oggetto IScanProfileMgr,** usare il [metodo CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con i parametri seguenti:

``` syntax
CoCreateInstance(CLSID_ScanProfileMgr, NULL, CLSCTX_LOCAL_SERVER, IID_IScanProfileMgr, ppv)
```

Se un profilo di analisi viene salvato usando il [**metodo IScanProfile::Save,**](-wia-iscanprofile-save.md) viene archiviato come file XML in %USERPROFILE% \\ Application Data Microsoft Document Center \\ \\ \\ UserScanProfiles.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                        |
| Intestazione<br/>                   | <dl> <dt>Scanprofilemgr.h</dt> </dl> |
| Idl<br/>                      | <dl> <dt>Scanprofiles.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Idispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Schema del profilo di analisi](-wia-scan-profile-schema.md)
</dt> </dl>

 

 
