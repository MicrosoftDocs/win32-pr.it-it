---
description: "L'interfaccia IPropertySetter imposta le proprietà per un effetto o una transizione in servizi di modifica DirectShow (DES). Per usare questa interfaccia, creare un'istanza di un oggetto Setter di proprietà (CLSID \\_ PropertySetter) e associarla a un effetto o una transizione chiamando il metodo IAMTimelineObj:: SetPropertySetter. Per altre informazioni, vedere uso degli effetti e delle transizioni. in genere, un'applicazione deve chiamare solo il metodo IPropertySetter:: ClearProps per cancellare le proprietà esistenti e il metodo IPropertySetter:: AddProp per aggiungere nuove proprietà. Gli altri metodi di questa interfaccia vengono chiamati da altri componenti DES."
ms.assetid: bee2abf2-0abc-4890-b1f2-7d0011444fbd
title: Interfaccia IPropertySetter (qedit. h)
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
ms.openlocfilehash: 8f8aaadea2f0fb63287775294a7c61f01b3730df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329753"
---
# <a name="ipropertysetter-interface"></a>Interfaccia IPropertySetter

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

L' `IPropertySetter` interfaccia imposta le proprietà per un effetto o una transizione in [servizi di modifica DirectShow](directshow-editing-services.md) (des).

Per usare questa interfaccia, creare un'istanza di un oggetto Setter di proprietà (CLSID \_ PropertySetter) e associarla a un effetto o una transizione chiamando il metodo [**IAMTimelineObj:: SetPropertySetter**](iamtimelineobj-setpropertysetter.md) . Per ulteriori informazioni, vedere [utilizzo di effetti e transizioni](working-with-effects-and-transitions.md).

In genere, un'applicazione deve chiamare solo il metodo [**IPropertySetter:: ClearProps**](ipropertysetter-clearprops.md) per cancellare le proprietà esistenti e il metodo [**IPropertySetter:: AddProp**](ipropertysetter-addprop.md) per aggiungere nuove proprietà. Gli altri metodi di questa interfaccia vengono chiamati da altri componenti DES.

## <a name="members"></a>Membri

L'interfaccia **IPropertySetter** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IPropertySetter** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IPropertySetter** dispone di questi metodi.



| Metodo                                               | Descrizione                                                                                                                                   |
|:-----------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddProp**](ipropertysetter-addprop.md)           | Aggiunge una proprietà al setter della proprietà, con una matrice di coppie di valori temporali che definiscono il valore della proprietà in un intervallo di tempo.<br/> |
| [**ClearProps**](ipropertysetter-clearprops.md)     | Cancella tutti i dati della proprietà dal setter della proprietà.<br/>                                                                                 |
| [**CloneProps**](ipropertysetter-cloneprops.md)     | Clona un set di proprietà da questo Setter di proprietà e le aggiunge a un nuovo setter di proprietà.<br/>                                       |
| [**FreeProps**](ipropertysetter-freeprops.md)       | Libera le risorse allocate dal metodo [**IPropertySetter:: GetProps**](ipropertysetter-getprops.md) .<br/>                             |
| [**GetProps**](ipropertysetter-getprops.md)         | Recupera le proprietà impostate per questo oggetto con i valori corrispondenti.<br/>                                                      |
| [**LoadFromBlob**](ipropertysetter-loadfromblob.md) | Carica i dati della proprietà da un formato di persistenza.<br/>                                                                                     |
| [**LoadXML**](ipropertysetter-loadxml.md)           | Carica i dati delle proprietà espressi in Extensible Markup Language (XML).<br/>                                                                 |
| [**PrintXML**](ipropertysetter-printxml.md)         | Converte i dati della proprietà in una stringa XML.<br/>                                                                                         |
| [**SaveToBlob**](ipropertysetter-savetoblob.md)     | Salva i dati della proprietà in un formato di persistenza.<br/>                                                                                   |
| [**SetProps**](ipropertysetter-setprops.md)         | Imposta le proprietà dell'oggetto di destinazione sullo stato appropriato per l'ora specificata.<br/>                                          |



 

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



 

 
