---
description: L'interfaccia IAMTimelineObj fornisce metodi per la modifica degli oggetti sequenza temporale in servizi di modifica DirectShow (DES).
ms.assetid: ae8a778d-00b3-4b88-98dd-16e0a8645127
title: Interfaccia IAMTimelineObj (qedit. h)
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
ms.openlocfilehash: e968ec01d937aeac9a5838b75462a6d23a632512
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326058"
---
# <a name="iamtimelineobj-interface"></a>Interfaccia IAMTimelineObj

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L' `IAMTimelineObj` interfaccia fornisce metodi per la modifica degli oggetti sequenza temporale in [servizi di modifica DirectShow](directshow-editing-services.md) (des). Tutti gli oggetti della sequenza temporale implementano questo metodo, inclusi gli oggetti Source, Effect, Transition, Track, Group e Composition. Creare un oggetto sequenza temporale chiamando il metodo [**IAMTimeline:: CreateEmptyNode**](iamtimeline-createemptynode.md) .

## <a name="members"></a>Membri

L'interfaccia **IAMTimelineObj** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IAMTimelineObj** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IAMTimelineObj** dispone di questi metodi.



| Metodo                                                          | Descrizione                                                                                                                            |
|:----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [**ClearDirty**](iamtimelineobj-cleardirty.md)                 | Non supportata.<br/>                                                                                                              |
| [**FixTimes**](iamtimelineobj-fixtimes.md)                     | Arrotonda gli orari di inizio e di fine specificati ai limiti del frame più vicini.<br/>                                                  |
| [**FixTimes2**](iamtimelineobj-fixtimes2.md)                   | Arrotonda le ore di inizio e di fine specificate, specificate come valori [**REFTIME**](reftime.md) , ai limiti del frame più vicini.<br/> |
| [**GetDirtyRange**](iamtimelineobj-getdirtyrange.md)           | Non supportata.<br/>                                                                                                              |
| [**GetDirtyRange2**](iamtimelineobj-getdirtyrange2.md)         | Non supportata.<br/>                                                                                                              |
| [**GetEmbedDepth**](iamtimelineobj-getembeddepth.md)           | Non supportata.<br/>                                                                                                              |
| [**Getgenid**](iamtimelineobj-getgenid.md)                     | Recupera l'identificatore generato dall'oggetto.<br/>                                                                                |
| [**GetGroupIBelongTo**](iamtimelineobj-getgroupibelongto.md)   | Non supportata.<br/>                                                                                                              |
| [**Getlocked**](iamtimelineobj-getlocked.md)                   | Recupera lo stato di modifica dell'oggetto (bloccato o sbloccato).<br/>                                                                  |
| [**Getmuted**](iamtimelineobj-getmuted.md)                     | Recupera lo stato di disattivazione dell'oggetto.<br/>                                                                                         |
| [**GetPropertySetter**](iamtimelineobj-getpropertysetter.md)   | Recupera il metodo di impostazione della proprietà dell'oggetto.<br/>                                                                                     |
| [**GetStartStop**](iamtimelineobj-getstartstop.md)             | Recupera l'ora di inizio e di fine dell'oggetto, relativa all'elemento padre dell'oggetto.<br/>                                               |
| [**GetStartStop2**](iamtimelineobj-getstartstop2.md)           | Recupera le ore di inizio e di fine dell'oggetto, come valori [**REFTIME**](reftime.md) .<br/>                                          |
| [**GetSubObject**](iamtimelineobj-getsubobject.md)             | Recupera l'oggetto SubObject associato a questo oggetto.<br/>                                                                        |
| [**GetSubObjectGUID**](iamtimelineobj-getsubobjectguid.md)     | Recupera il GUID dell'oggetto SubObject associato a questo oggetto sequenza temporale.<br/>                                                   |
| [**GetSubObjectGUIDB**](iamtimelineobj-getsubobjectguidb.md)   | Recupera il GUID dell'oggetto sotto forma di valore **BSTR** .<br/>                                                                    |
| [**GetSubObjectLoaded**](iamtimelineobj-getsubobjectloaded.md) | Determina se è stato impostato il puntatore al sottooggetto dell'oggetto.<br/>                                                             |
| [**GetTimelineNoRef**](iamtimelineobj-gettimelinenoref.md)     | Non supportata.<br/>                                                                                                              |
| [**GetTimelineType**](iamtimelineobj-gettimelinetype.md)       | Recupera il tipo dell'oggetto.<br/>                                                                                                |
| [**GetUserData**](iamtimelineobj-getuserdata.md)               | Recupera i dati persistenti definiti dall'applicazione.<br/>                                                                          |
| [**GetUserID**](iamtimelineobj-getuserid.md)                   | Recupera l'identificatore definito dall'applicazione dell'oggetto.<br/>                                                                      |
| [**GetUserName**](iamtimelineobj-getusername.md)               | Recupera il nome definito dall'applicazione dell'oggetto.<br/>                                                                            |
| [**Rimuovi**](iamtimelineobj-remove.md)                         | Rimuove questo oggetto dalla sequenza temporale, per il reinserimento altrove.<br/>                                                           |
| [**RemoveAll**](iamtimelineobj-removeall.md)                   | Rimuove in modo permanente questo oggetto dalla sequenza temporale, inclusi i sottooggetti e gli elementi figlio.<br/>                                       |
| [**SetDirtyRange**](iamtimelineobj-setdirtyrange.md)           | Non implementato.<br/>                                                                                                            |
| [**SetDirtyRange2**](iamtimelineobj-setdirtyrange2.md)         | Non implementato.<br/>                                                                                                            |
| [**Con blocco**](iamtimelineobj-setlocked.md)                   | Imposta lo stato di modifica dell'oggetto su bloccato o sbloccato.<br/>                                                                      |
| [**Con silenziamento**](iamtimelineobj-setmuted.md)                     | Imposta lo stato di disattivazione dell'oggetto.<br/>                                                                                              |
| [**SetPropertySetter**](iamtimelineobj-setpropertysetter.md)   | Imposta il metodo di impostazione della proprietà dell'oggetto.<br/>                                                                                          |
| [**SetStartStop**](iamtimelineobj-setstartstop.md)             | Imposta l'ora di inizio e di fine dell'oggetto, relativa alla sequenza temporale.<br/>                                                           |
| [**SetStartStop2**](iamtimelineobj-setstartstop2.md)           | Imposta l'ora di inizio e di fine dell'oggetto, come valori **REFTIME** .<br/>                                                              |
| [**SetSubObject**](iamtimelineobj-setsubobject.md)             | Non supportata.<br/>                                                                                                              |
| [**SetSubObjectGUID**](iamtimelineobj-setsubobjectguid.md)     | Specifica l'identificatore univoco globale (GUID) dell'oggetto SubObject associato a questo oggetto.<br/>                               |
| [**SetSubObjectGUIDB**](iamtimelineobj-setsubobjectguidb.md)   | Specifica il GUID dell'oggetto sotto forma di valore **BSTR** .<br/>                                                                    |
| [**SetTimelineType**](iamtimelineobj-settimelinetype.md)       | Non supportata.<br/>                                                                                                              |
| [**SetUserData**](iamtimelineobj-setuserdata.md)               | Imposta i dati persistenti definiti dall'applicazione.<br/>                                                                                   |
| [**SetUserID**](iamtimelineobj-setuserid.md)                   | Imposta un identificatore definito dall'applicazione per l'oggetto.<br/>                                                                      |
| [**SetUserName**](iamtimelineobj-setusername.md)               | Imposta un nome definito dall'applicazione per l'oggetto.<br/>                                                                            |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



 

 
