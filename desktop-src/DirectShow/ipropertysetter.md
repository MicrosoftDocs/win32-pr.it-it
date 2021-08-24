---
description: L'interfaccia IPropertySetter imposta le proprietà per un effetto o una transizione in DirectShow Editing Services (DES). Per usare questa interfaccia, creare un'istanza di un oggetto del setter di proprietà (CLSID PropertySetter) e associarla a un effetto o a una transizione chiamando il metodo \_ IAMTimelineObj::SetPropertySetter. Per altre informazioni, vedere Uso di effetti e transizioni. In genere un'applicazione deve chiamare solo il metodo IPropertySetter::ClearProps per cancellare le proprietà esistenti e il metodo IPropertySetter::AddProp per aggiungere nuove proprietà. Gli altri metodi in questa interfaccia vengono chiamati da altri componenti DES.
ms.assetid: bee2abf2-0abc-4890-b1f2-7d0011444fbd
title: Interfaccia IPropertySetter (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c6dc32c25c85893eeb2e9872bcf67be974489ec82fdd4d09c19a2341f6867ade
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831031"
---
# <a name="ipropertysetter-interface"></a>Interfaccia IPropertySetter

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

L'interfaccia imposta le proprietà su un effetto o una `IPropertySetter` transizione in DirectShow Editing [Services](directshow-editing-services.md) (DES).

Per usare questa interfaccia, creare un'istanza di un oggetto del setter di proprietà (CLSID PropertySetter) e associarla a un effetto o a una transizione chiamando il metodo \_ [**IAMTimelineObj::SetPropertySetter.**](iamtimelineobj-setpropertysetter.md) Per altre informazioni, vedere [Uso di effetti e transizioni.](working-with-effects-and-transitions.md)

In genere un'applicazione deve chiamare solo il metodo [**IPropertySetter::ClearProps**](ipropertysetter-clearprops.md) per cancellare le proprietà esistenti e il metodo [**IPropertySetter::AddProp**](ipropertysetter-addprop.md) per aggiungere nuove proprietà. Gli altri metodi in questa interfaccia vengono chiamati da altri componenti DES.

## <a name="members"></a>Membri

**L'interfaccia IPropertySetter** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IPropertySetter** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IPropertySetter** include questi metodi.



| Metodo                                               | Descrizione                                                                                                                                   |
|:-----------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddProp**](ipropertysetter-addprop.md)           | Aggiunge una proprietà al setter di proprietà, con una matrice di coppie tempo-valore che definiscono il valore della proprietà in un intervallo di tempo.<br/> |
| [**ClearProps**](ipropertysetter-clearprops.md)     | Cancella tutti i dati delle proprietà dal setter di proprietà.<br/>                                                                                 |
| [**CloneProps**](ipropertysetter-cloneprops.md)     | Clona un set di proprietà da questo setter di proprietà e le aggiunge a un nuovo setter di proprietà.<br/>                                       |
| [**FreeProps**](ipropertysetter-freeprops.md)       | Libera le risorse allocate dal [**metodo IPropertySetter::GetProps.**](ipropertysetter-getprops.md)<br/>                             |
| [**GetProps**](ipropertysetter-getprops.md)         | Recupera le proprietà impostate su questo oggetto , con i valori corrispondenti.<br/>                                                      |
| [**LoadFromBlob**](ipropertysetter-loadfromblob.md) | Carica i dati della proprietà da un formato di persistenza.<br/>                                                                                     |
| [**Loadxml**](ipropertysetter-loadxml.md)           | Carica i dati delle proprietà espressi in Extensible Markup Language (XML).<br/>                                                                 |
| [**PrintXML**](ipropertysetter-printxml.md)         | Converte i dati delle proprietà in una stringa XML.<br/>                                                                                         |
| [**SaveToBlob**](ipropertysetter-savetoblob.md)     | Salva i dati della proprietà in un formato di persistenza.<br/>                                                                                   |
| [**SetProps**](ipropertysetter-setprops.md)         | Imposta le proprietà dell'oggetto di destinazione sullo stato appropriato per l'ora specificata.<br/>                                          |



 

## <a name="remarks"></a>Commenti

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare [Microsoft Windows SDK Update per Windows Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



 

 
