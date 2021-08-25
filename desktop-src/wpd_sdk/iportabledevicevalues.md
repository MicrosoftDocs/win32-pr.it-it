---
description: L'interfaccia IPortableDeviceValues contiene una raccolta di coppie PROPERTYKEY/PROPVARIANT.
ms.assetid: a73cbb4e-15d2-4c8d-9267-aaec9a0fd09f
title: Interfaccia IPortableDeviceValues (PortableDeviceTypes.h)
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
ms.openlocfilehash: 7f7aaceff66cd817666dd05b92243239f860b2f59a993e4afca1831fc8085de0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930001"
---
# <a name="iportabledevicevalues-interface"></a>Interfaccia IPortableDeviceValues

**L'interfaccia IPortableDeviceValues** contiene una raccolta di **coppie PROPERTYKEY** / **PROPVARIANT.** Non è necessario che i valori nella raccolta siano uguali a VARTYPE.

I valori vengono archiviati come coppie chiave-valore. ogni chiave deve essere univoca nella raccolta. I client possono cercare elementi in base **a PROPERTYKEY** o all'indice in base zero. I valori dei dati vengono archiviati come strutture **PROPVARIANT.** È possibile aggiungere o recuperare valori di qualsiasi tipo usando i metodi generici **SetValue** e **GetValue** oppure aggiungere elementi usando il metodo specifico per il tipo di dati aggiunti.

I **metodi Get...** richiedono al chiamante di rilasciare i valori recuperati in modo appropriato. I **metodi Set...** copiano il valore nella raccolta.

Quando viene **rilasciata un'interfaccia IPortableDeviceValues,** chiama **Clear**, che libera la memoria allocata per tutti i relativi membri in modo appropriato.

Questa interfaccia può essere recuperata da un metodo o, se è necessario un nuovo oggetto, chiamare **CoCreate** con **CLSID \_ PortableDeviceValues.**

## <a name="members"></a>Membri

**L'interfaccia IPortableDeviceValues** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IPortableDeviceValues** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IPortableDeviceValues** include questi metodi.



| Metodo                                                                                                                     | Descrizione                                                                                                            |
|:---------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [**Cancella**](iportabledevicevalues-clear.md)                                                                               | Elimina tutti gli elementi dalla raccolta.<br/>                                                                      |
| [**CopyValuesFromPropertyStore**](iportabledevicevalues-copyvaluesfrompropertystore.md)                                   | Copia il contenuto di un **oggetto IPropertyStore** nella raccolta.<br/>                                           |
| [**CopyValuesToPropertyStore**](iportabledevicevalues-copyvaluestopropertystore.md)                                       | Copia tutti i valori da una raccolta in **un'interfaccia IPropertyStore.**<br/>                               |
| [**GetAt**](iportabledevicevalues-getat.md)                                                                               | Recupera un valore dall'insieme utilizzando l'indice in base zero fornito.<br/>                                  |
| [**GetBoolValue**](iportabledevicevalues-getboolvalue.md)                                                                 | Recupera un **valore BOOL** (tipo VT \_ BOOL) specificato da una chiave.<br/>                                              |
| [**GetBufferValue**](iportabledevicevalues-getbuffervalue.md)                                                             | Recupera un valore di matrice di byte (tipo VT \_ VECTOR \| VT \_ UI1) specificato da una chiave.<br/>                               |
| [**GetCount**](iportabledevicevalues-getcount.md)                                                                         | Recupera il numero di elementi nella raccolta.<br/>                                                            |
| [**GetErrorValue**](iportabledevicevalues-geterrorvalue.md)                                                               | Recupera un **valore HRESULT** (tipo VT \_ ERROR) specificato da una chiave.<br/>                                         |
| [**GetFloatValue**](iportabledevicevalues-getfloatvalue.md)                                                               | Recupera un **valore FLOAT** (tipo VT \_ R4) specificato da una chiave.<br/>                                               |
| [**GetGuidValue**](iportabledevicevalues-getguidvalue.md)                                                                 | Recupera un **valore GUID** (tipo \_ CLSID VT) specificato da una chiave.<br/>                                             |
| [**GetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-getiportabledevicekeycollectionvalue.md)                 | Recupera un **valore IPortableDeviceKeyCollection** (tipo VT \_ UNKNOWN) specificato da una chiave.<br/>                  |
| [**GetIPortableDevicePropVariantCollectionValue**](iportabledevicevalues-getiportabledevicepropvariantcollectionvalue.md) | Recupera un **valore IPortableDevicePropVariantCollection** (tipo VT \_ UNKNOWN) specificato da una chiave.<br/>          |
| [**GetIPortableDeviceValuesCollectionValue**](iportabledevicevalues-getiportabledevicevaluescollectionvalue.md)           | Recupera un **valore IPortableDeviceValuesCollection** (tipo VT \_ UNKNOWN) specificato da una chiave.<br/>               |
| [**GetIPortableDeviceValuesValue**](iportabledevicevalues-getiportabledevicevaluesvalue.md)                               | Recupera un **valore IPortableDeviceValues** (tipo VT \_ UNKNOWN) specificato da una chiave.<br/>                         |
| [**GetIUnknownValue**](iportabledevicevalues-getiunknownvalue.md)                                                         | Recupera un **valore dell'interfaccia IUnknown** (tipo VT \_ UNKNOWN) specificato da una chiave.<br/>                            |
| [**GetKeyValue**](iportabledevicevalues-getkeyvalue.md)                                                                   | Recupera un **valore PROPERTYKEY** specificato da una chiave.<br/>                                                       |
| [**GetSignedIntegerValue**](iportabledevicevalues-getsignedintegervalue.md)                                               | Recupera un **valore LONG** (tipo VT \_ I4) specificato da una chiave.<br/>                                                |
| [**GetSignedLargeIntegerValue**](iportabledevicevalues-getsignedlargeintegervalue.md)                                     | Recupera un **valore LONGLONG** (tipo VT \_ I8) specificato da una chiave.<br/>                                            |
| [**GetStringValue**](iportabledevicevalues-getstringvalue.md)                                                             | Recupera un valore stringa (tipo VT \_ LPWSTR) specificato da una chiave.<br/>                                              |
| [**GetUnsignedIntegerValue**](iportabledevicevalues-getunsignedintegervalue.md)                                           | Recupera un **valore ULONG** (tipo VT \_ UI4) specificato da una chiave.<br/>                                              |
| [**GetUnsignedLargeIntegerValue**](iportabledevicevalues-getunsignedlargeintegervalue.md)                                 | Recupera un **valore ULONGLONG** (tipo VT \_ UI8) specificato da una chiave.<br/>                                          |
| [**Getvalue**](iportabledevicevalues-getvalue.md)                                                                         | Recupera un **valore PROPVARIANT** specificato da una chiave.<br/>                                                       |
| [**RemoveValue**](iportabledevicevalues-removevalue.md)                                                                   | Rimuove un elemento dalla raccolta.<br/>                                                                        |
| [**SetBoolValue**](iportabledevicevalues-setboolvalue.md)                                                                 | Aggiunge un nuovo **valore booleano** (tipo VT \_ BOOL) o ne sovrascrive uno esistente.<br/>                                 |
| [**SetBufferValue**](iportabledevicevalues-setbuffervalue.md)                                                             | Aggiunge un nuovo **valore BYTE** \* (tipo VT \_ VECTOR \| VT \_ UI1) o ne sovrascrive uno esistente.<br/>                     |
| [**SetErrorValue**](iportabledevicevalues-seterrorvalue.md)                                                               | Aggiunge un nuovo **valore HRESULT** (tipo VT \_ ERROR) o ne sovrascrive uno esistente.<br/>                                |
| [**SetFloatValue**](iportabledevicevalues-setfloatvalue.md)                                                               | Aggiunge un nuovo **valore FLOAT** (tipo VT \_ R4) o ne sovrascrive uno esistente.<br/>                                     |
| [**SetGuidValue**](iportabledevicevalues-setguidvalue.md)                                                                 | Aggiunge un nuovo **valore GUID** (tipo \_ CLSID VT) o ne sovrascrive uno esistente.<br/>                                   |
| [**SetIPortableDeviceKeyCollectionValue**](iportabledevicevalues-setiportabledevicekeycollectionvalue.md)                 | Aggiunge un nuovo **valore IPortableDeviceKeyCollectionValue** (tipo VT UNKNOWN) o \_ ne sovrascrive uno esistente.<br/>    |
| [**SetIPortableDevicePropVariantCollectionValue**](iportabledevicevalues-setiportabledevicepropvariantcollectionvalue.md) | Aggiunge un nuovo **valore IPortableDevicePropVariantCollection** (tipo VT UNKNOWN) o \_ ne sovrascrive uno esistente.<br/> |
| [**SetIPortableDeviceValuesCollectionValue**](iportabledevicevalues-setiportabledevicevaluescollectionvalue.md)           | Aggiunge un nuovo **valore IPortableDeviceValuesCollection** (tipo VT UNKNOWN) o \_ ne sovrascrive uno esistente.<br/>      |
| [**SetIPortableDeviceValuesValue**](iportabledevicevalues-setiportabledevicevaluesvalue.md)                               | Aggiunge un nuovo **valore IPortableDeviceValues** (tipo VT \_ UNKNOWN) o ne sovrascrive uno esistente.<br/>                |
| [**SetIUnknownValue**](iportabledevicevalues-setiunknownvalue.md)                                                         | Aggiunge un nuovo **valore IUnknown** (tipo VT \_ UNKNOWN) o ne sovrascrive uno esistente.<br/>                             |
| [**SetKeyValue**](iportabledevicevalues-setkeyvalue.md)                                                                   | Aggiunge un nuovo **valore PROPERTYKEY** (tipo VT \_ UNKNOWN) o ne sovrascrive uno esistente.<br/>                          |
| [**SetSignedIntegerValue**](iportabledevicevalues-setsignedintegervalue.md)                                               | Aggiunge un nuovo **valore LONG** (tipo VT \_ I4) o ne sovrascrive uno esistente.<br/>                                      |
| [**SetSignedLargeIntegerValue**](iportabledevicevalues-setsignedlargeintegervalue.md)                                     | Aggiunge un nuovo **valore LONGLONG** (tipo VT \_ I8) o ne sovrascrive uno esistente.<br/>                                  |
| [**SetStringValue**](iportabledevicevalues-setstringvalue.md)                                                             | Aggiunge un nuovo valore stringa (tipo VT \_ LPWSTR) o ne sovrascrive uno esistente.<br/>                                    |
| [**SetUnsignedIntegerValue**](iportabledevicevalues-setunsignedintegervalue.md)                                           | Aggiunge un nuovo **valore ULONG** (tipo VT \_ UI4) o ne sovrascrive uno esistente.<br/>                                    |
| [**SetUnsignedLargeIntegerValue**](iportabledevicevalues-setunsignedlargeintegervalue.md)                                 | Aggiunge un nuovo **valore ULONGLONG** (tipo VT \_ UI8) o ne sovrascrive uno esistente.<br/>                                |
| [**SetValue**](iportabledevicevalues-setvalue.md)                                                                         | Aggiunge un nuovo **valore PROPVARIANT** o ne sovrascrive uno esistente.<br/>                                             |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfacce di raccolta**](collection-interfaces.md)
</dt> </dl>

 

