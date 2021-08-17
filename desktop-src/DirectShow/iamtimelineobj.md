---
description: L'interfaccia IAMTimelineObj fornisce metodi per modificare gli oggetti sequenza temporale in DirectShow Editing Services (DES).
ms.assetid: ae8a778d-00b3-4b88-98dd-16e0a8645127
title: Interfaccia IAMTimelineObj (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4a987cfd0f08311a0e7a233ab479e5cdbe2fc649fd521ad4f4ed1b37b6df6d75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119428161"
---
# <a name="iamtimelineobj-interface"></a>Interfaccia IAMTimelineObj

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

L'interfaccia fornisce metodi per modificare gli oggetti sequenza temporale `IAMTimelineObj` in DirectShow Editing [Services](directshow-editing-services.md) (DES). Tutti gli oggetti sequenza temporale implementano questo metodo, inclusi gli oggetti origine, effetto, transizione, traccia, gruppo e composizione. Creare un oggetto sequenza temporale chiamando il [**metodo IAMTimeline::CreateEmptyNode.**](iamtimeline-createemptynode.md)

## <a name="members"></a>Membri

**L'interfaccia IAMTimelineObj** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IAMTimelineObj** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **IAMTimelineObj.**



| Metodo                                                          | Descrizione                                                                                                                            |
|:----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [**ClearDirty**](iamtimelineobj-cleardirty.md)                 | Non supportata.<br/>                                                                                                              |
| [**FixTimes**](iamtimelineobj-fixtimes.md)                     | Arrotonda i tempi di inizio e di arresto specificati ai limiti del frame più vicini.<br/>                                                  |
| [**FixTimes2**](iamtimelineobj-fixtimes2.md)                   | Arrotonda i tempi di inizio e di arresto specificati, specificati come [**valori REFTIME,**](reftime.md) ai limiti del frame più vicini.<br/> |
| [**GetDirtyRange**](iamtimelineobj-getdirtyrange.md)           | Non supportata.<br/>                                                                                                              |
| [**GetDirtyRange2**](iamtimelineobj-getdirtyrange2.md)         | Non supportata.<br/>                                                                                                              |
| [**GetEmbedDepth**](iamtimelineobj-getembeddepth.md)           | Non supportata.<br/>                                                                                                              |
| [**GetGenID**](iamtimelineobj-getgenid.md)                     | Recupera l'identificatore generato dell'oggetto.<br/>                                                                                |
| [**GetGroupIBelongTo**](iamtimelineobj-getgroupibelongto.md)   | Non supportata.<br/>                                                                                                              |
| [**GetLocked**](iamtimelineobj-getlocked.md)                   | Recupera lo stato di modifica dell'oggetto (bloccato o sbloccato).<br/>                                                                  |
| [**GetMuted**](iamtimelineobj-getmuted.md)                     | Recupera lo stato disattivato dell'oggetto.<br/>                                                                                         |
| [**GetPropertySetter**](iamtimelineobj-getpropertysetter.md)   | Recupera il setter di proprietà dell'oggetto.<br/>                                                                                     |
| [**GetStartStop**](iamtimelineobj-getstartstop.md)             | Recupera i tempi di inizio e arresto dell'oggetto, rispetto all'elemento padre dell'oggetto.<br/>                                               |
| [**GetStartStop2**](iamtimelineobj-getstartstop2.md)           | Recupera gli orari di inizio e di arresto dell'oggetto, come [**valori REFTIME.**](reftime.md)<br/>                                          |
| [**GetSubObject**](iamtimelineobj-getsubobject.md)             | Recupera il sottooggetto associato a questo oggetto.<br/>                                                                        |
| [**GetSubObjectGUID**](iamtimelineobj-getsubobjectguid.md)     | Recupera il GUID del sottooggetto associato a questo oggetto sequenza temporale.<br/>                                                   |
| [**GetSubObjectGUIDB**](iamtimelineobj-getsubobjectguidb.md)   | Recupera il GUID del sottooggetto come **valore BSTR.**<br/>                                                                    |
| [**GetSubObjectLoaded**](iamtimelineobj-getsubobjectloaded.md) | Determina se il puntatore del sottooggetto dell'oggetto è stato impostato.<br/>                                                             |
| [**GetTimelineNoRef**](iamtimelineobj-gettimelinenoref.md)     | Non supportata.<br/>                                                                                                              |
| [**GetTimelineType**](iamtimelineobj-gettimelinetype.md)       | Recupera il tipo dell'oggetto.<br/>                                                                                                |
| [**GetUserData**](iamtimelineobj-getuserdata.md)               | Recupera i dati persistenti definiti dall'applicazione.<br/>                                                                          |
| [**GetUserID**](iamtimelineobj-getuserid.md)                   | Recupera l'identificatore definito dall'applicazione dell'oggetto.<br/>                                                                      |
| [**GetUserName**](iamtimelineobj-getusername.md)               | Recupera il nome definito dall'applicazione dell'oggetto.<br/>                                                                            |
| [**Rimuovi**](iamtimelineobj-remove.md)                         | Rimuove questo oggetto dalla sequenza temporale, per la reinserzione altrove.<br/>                                                           |
| [**RemoveAll**](iamtimelineobj-removeall.md)                   | Rimuove definitivamente questo oggetto dalla sequenza temporale, inclusi gli oggetti secondari e gli elementi figlio.<br/>                                       |
| [**SetDirtyRange**](iamtimelineobj-setdirtyrange.md)           | Non implementato.<br/>                                                                                                            |
| [**SetDirtyRange2**](iamtimelineobj-setdirtyrange2.md)         | Non implementato.<br/>                                                                                                            |
| [**SetLocked**](iamtimelineobj-setlocked.md)                   | Imposta lo stato di modifica dell'oggetto su bloccato o sbloccato.<br/>                                                                      |
| [**SetMuted**](iamtimelineobj-setmuted.md)                     | Imposta lo stato disattivato dell'oggetto.<br/>                                                                                              |
| [**SetPropertySetter**](iamtimelineobj-setpropertysetter.md)   | Imposta il setter di proprietà dell'oggetto.<br/>                                                                                          |
| [**SetStartStop**](iamtimelineobj-setstartstop.md)             | Imposta i tempi di inizio e arresto dell'oggetto, rispetto alla sequenza temporale.<br/>                                                           |
| [**SetStartStop2**](iamtimelineobj-setstartstop2.md)           | Imposta gli orari di inizio e di arresto dell'oggetto, come **valori REFTIME.**<br/>                                                              |
| [**SetSubObject**](iamtimelineobj-setsubobject.md)             | Non supportata.<br/>                                                                                                              |
| [**SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md)     | Specifica l'identificatore univoco globale (GUID) del sottooggetto associato a questo oggetto.<br/>                               |
| [**SetSubObjectGUIDB**](iamtimelineobj-setsubobjectguidb.md)   | Specifica il GUID del sottooggetto come **valore BSTR.**<br/>                                                                    |
| [**SetTimelineType**](iamtimelineobj-settimelinetype.md)       | Non supportata.<br/>                                                                                                              |
| [**SetUserData**](iamtimelineobj-setuserdata.md)               | Imposta dati persistenti definiti dall'applicazione.<br/>                                                                                   |
| [**SetUserID**](iamtimelineobj-setuserid.md)                   | Imposta un identificatore definito dall'applicazione per l'oggetto .<br/>                                                                      |
| [**SetUserName**](iamtimelineobj-setusername.md)               | Imposta un nome definito dall'applicazione per l'oggetto .<br/>                                                                            |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare l'aggiornamento di Microsoft Windows SDK per Windows [Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



 

 
