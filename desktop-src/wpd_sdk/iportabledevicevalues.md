---
description: L'interfaccia IPortableDeviceValues include una raccolta di coppie PROPERTYKEY/PROPVARIANT.
ms.assetid: a73cbb4e-15d2-4c8d-9267-aaec9a0fd09f
title: Interfaccia IPortableDeviceValues (PortableDeviceTypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: ecdfd91c9ea4ab5202a72015f579d560b37fbffd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324514"
---
# <a name="iportabledevicevalues-interface"></a>Interfaccia IPortableDeviceValues

L'interfaccia **IPortableDeviceValues** include una raccolta di coppie **PropertyKey** / **PROPVARIANT** . I valori nella raccolta non devono essere uguali.

I valori vengono archiviati come coppie chiave-valore. ogni chiave deve essere univoca nella raccolta. I client possono cercare gli elementi in base a **PropertyKey** o all'indice in base zero. I valori dei dati vengono archiviati come strutture **PROPVARIANT** . Per aggiungere o recuperare valori di qualsiasi tipo, è possibile usare i metodi **SetValue** e **GetValue** oppure aggiungere elementi usando il metodo specifico del tipo di dati aggiunti.

I metodi **Get...** richiedono che il chiamante rilasci tutti i valori recuperati in modo appropriato. I metodi **set...** copiano il valore nella raccolta.

Quando viene rilasciata un'interfaccia **IPortableDeviceValues** , viene chiamato **Clear**, che libera la memoria allocata per tutti i membri in modo appropriato.

Questa interfaccia può essere recuperata da un metodo o, se è necessario un nuovo oggetto, chiamare **CoCreate** con **CLSID \_ PortableDeviceValues**.

## <a name="members"></a>Membri

L'interfaccia **IPortableDeviceValues** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IPortableDeviceValues** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IPortableDeviceValues** dispone di questi metodi.



| Metodo                                                                                                                     | Descrizione                                                                                                            |
|:---------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [**Deselezionare**](iportabledevicevalues-clear.md)                                                                               | Elimina tutti gli elementi dall'insieme.<br/>                                                                      |
| [**CopyValuesFromPropertyStore**](iportabledevicevalues-copyvaluesfrompropertystore.md)                                   | Copia il contenuto di un oggetto **IPropertyStore** nella raccolta.<br/>                                           |
| [**CopyValuesToPropertyStore**](iportabledevicevalues-copyvaluestopropertystore.md)                                       | Copia tutti i valori da una raccolta in un'interfaccia **IPropertyStore** .<br/>                               |
| [**GetAt**](iportabledevicevalues-getat.md)                                                                               | Recupera un valore dalla raccolta utilizzando l'indice in base zero fornito.<br/>                                  |
| [**GetBoolValue**](iportabledevicevalues-getboolvalue.md)                                                                 | Recupera un valore **bool** (tipo VT \_ bool) specificato da una chiave.<br/>                                              |
| [**GetBufferValue**](iportabledevicevalues-getbuffervalue.md)                                                             | Recupera un valore di matrice di byte (tipo VT \_ vector VT \| \_ Ui1) specificato da una chiave.<br/>                               |
| [**GetCount**](iportabledevicevalues-getcount.md)                                                                         | Recupera il numero di elementi nella raccolta.<br/>                                                            |
| [**GetErrorValue**](iportabledevicevalues-geterrorvalue.md)                                                               | Recupera un valore **HRESULT** (tipo \_ errore VT) specificato da una chiave.<br/>                                         |
| [**GetFloatValue**](iportabledevicevalues-getfloatvalue.md)                                                               | Recupera un valore **float** (tipo VT \_ R4) specificato da una chiave.<br/>                                               |
| [**GetGuidValue**](iportabledevicevalues-getguidvalue.md)                                                                 | Recupera un valore **GUID** (tipo VT \_ CLSID) specificato da una chiave.<br/>                                             |
| [**GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md)                 | Recupera un valore **IPortableDeviceKeyCollection** (tipo VT \_ sconosciuto) specificato da una chiave.<br/>                  |
| [**GetIPortableDevicePropVariantCollectionValue**](iportabledevicevalues-getiportabledevicepropvariantcollectionvalue.md) | Recupera un valore **IPortableDevicePropVariantCollection** (tipo VT \_ sconosciuto) specificato da una chiave.<br/>          |
| [**GetIPortableDeviceValuesCollectionValue**](iportabledevicevalues-getiportabledevicevaluescollectionvalue.md)           | Recupera un valore **IPortableDeviceValuesCollection** (tipo VT \_ sconosciuto) specificato da una chiave.<br/>               |
| [**GetIPortableDeviceValuesValue**](iportabledevicevalues-getiportabledevicevaluesvalue.md)                               | Recupera un valore **IPortableDeviceValues** (tipo VT \_ sconosciuto) specificato da una chiave.<br/>                         |
| [**GetIUnknownValue**](iportabledevicevalues-getiunknownvalue.md)                                                         | Recupera un valore di interfaccia **IUnknown** (tipo VT \_ sconosciuto) specificato da una chiave.<br/>                            |
| [**GetKeyValue**](iportabledevicevalues-getkeyvalue.md)                                                                   | Recupera un valore **PropertyKey** specificato da una chiave.<br/>                                                       |
| [**GetSignedIntegerValue**](iportabledevicevalues-getsignedintegervalue.md)                                               | Recupera un valore **Long** (tipo VT \_ I4) specificato da una chiave.<br/>                                                |
| [**GetSignedLargeIntegerValue**](iportabledevicevalues-getsignedlargeintegervalue.md)                                     | Recupera un valore **LONGLONG** (tipo VT \_ I8) specificato da una chiave.<br/>                                            |
| [**GetStringValue**](iportabledevicevalues-getstringvalue.md)                                                             | Recupera un valore stringa (tipo VT \_ LPWSTR) specificato da una chiave.<br/>                                              |
| [**GetUnsignedIntegerValue**](iportabledevicevalues-getunsignedintegervalue.md)                                           | Recupera un valore **ULONG** (Type VT \_ UI4) specificato da una chiave.<br/>                                              |
| [**GetUnsignedLargeIntegerValue**](iportabledevicevalues-getunsignedlargeintegervalue.md)                                 | Recupera un valore **ULONGLONG** (tipo VT \_ UI8) specificato da una chiave.<br/>                                          |
| [**GetValue**](iportabledevicevalues-getvalue.md)                                                                         | Recupera un valore **PROPVARIANT** specificato da una chiave.<br/>                                                       |
| [**RemoveValue**](iportabledevicevalues-removevalue.md)                                                                   | Rimuove un elemento dalla raccolta.<br/>                                                                        |
| [**SetBoolValue**](iportabledevicevalues-setboolvalue.md)                                                                 | Aggiunge un nuovo valore **booleano** (tipo VT \_ bool) o sovrascrive uno esistente.<br/>                                 |
| [**SetBufferValue**](iportabledevicevalues-setbuffervalue.md)                                                             | Aggiunge un nuovo valore **byte** \* (tipo VT \_ vector \| VT \_ Ui1) o sovrascrive uno esistente.<br/>                     |
| [**SetErrorValue**](iportabledevicevalues-seterrorvalue.md)                                                               | Aggiunge un nuovo valore **HRESULT** (tipo \_ errore VT) o sovrascrive uno esistente.<br/>                                |
| [**SetFloatValue**](iportabledevicevalues-setfloatvalue.md)                                                               | Aggiunge un nuovo valore **float** (tipo VT \_ R4) o sovrascrive uno esistente.<br/>                                     |
| [**SetGuidValue**](iportabledevicevalues-setguidvalue.md)                                                                 | Aggiunge un nuovo valore **GUID** (tipo VT \_ CLSID) o sovrascrive uno esistente.<br/>                                   |
| [**SetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-setiportabledevicekeycollectionvalue.md)                 | Aggiunge un nuovo valore **IPortableDeviceKeyCollectionValue** (tipo VT \_ sconosciuto) o sovrascrive uno esistente.<br/>    |
| [**SetIPortableDevicePropVariantCollectionValue**](iportabledevicevalues-setiportabledevicepropvariantcollectionvalue.md) | Aggiunge un nuovo valore **IPortableDevicePropVariantCollection** (tipo VT \_ sconosciuto) o sovrascrive uno esistente.<br/> |
| [**SetIPortableDeviceValuesCollectionValue**](iportabledevicevalues-setiportabledevicevaluescollectionvalue.md)           | Aggiunge un nuovo valore **IPortableDeviceValuesCollection** (tipo VT \_ sconosciuto) o sovrascrive uno esistente.<br/>      |
| [**SetIPortableDeviceValuesValue**](iportabledevicevalues-setiportabledevicevaluesvalue.md)                               | Aggiunge un nuovo valore **IPortableDeviceValues** (tipo VT \_ sconosciuto) o sovrascrive uno esistente.<br/>                |
| [**SetIUnknownValue**](iportabledevicevalues-setiunknownvalue.md)                                                         | Aggiunge un nuovo valore **IUnknown** (tipo VT \_ sconosciuto) o sovrascrive uno esistente.<br/>                             |
| [**SetKeyValue**](iportabledevicevalues-setkeyvalue.md)                                                                   | Aggiunge un nuovo valore **PropertyKey** (Type VT \_ Unknown) o ne sovrascrive uno esistente.<br/>                          |
| [**SetSignedIntegerValue**](iportabledevicevalues-setsignedintegervalue.md)                                               | Aggiunge un nuovo valore **Long** (tipo VT \_ I4) o sovrascrive uno esistente.<br/>                                      |
| [**SetSignedLargeIntegerValue**](iportabledevicevalues-setsignedlargeintegervalue.md)                                     | Aggiunge un nuovo valore **LONGLONG** (tipo VT \_ I8) o sovrascrive uno esistente.<br/>                                  |
| [**SetStringValue**](iportabledevicevalues-setstringvalue.md)                                                             | Aggiunge un nuovo valore stringa (digitare VT \_ LPWSTR) o sovrascrive uno esistente.<br/>                                    |
| [**SetUnsignedIntegerValue**](iportabledevicevalues-setunsignedintegervalue.md)                                           | Aggiunge un nuovo valore **ULONG** (Type VT \_ UI4) o ne sovrascrive uno esistente.<br/>                                    |
| [**SetUnsignedLargeIntegerValue**](iportabledevicevalues-setunsignedlargeintegervalue.md)                                 | Aggiunge un nuovo valore **ULONGLONG** (tipo VT \_ UI8) o sovrascrive uno esistente.<br/>                                |
| [**SetValue**](iportabledevicevalues-setvalue.md)                                                                         | Aggiunge un nuovo valore di **PROPVARIANT** o ne sovrascrive uno esistente.<br/>                                             |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce di raccolta**](collection-interfaces.md)
</dt> </dl>

 

