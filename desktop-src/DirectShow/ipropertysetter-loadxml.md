---
description: Il metodo LoadXML carica i dati delle proprietà espressi in Extensible Markup Language (XML).
ms.assetid: cc67e7e0-a6e0-43d1-b35d-5d64caf24e6e
title: Metodo IPropertySetter::LoadXML (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.LoadXML
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1779c6bcd37baad4bd423d0a46abd3741dd3a7939c1615a5871e6746729558c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952570"
---
# <a name="ipropertysetterloadxml-method"></a>Metodo IPropertySetter::LoadXML

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il `LoadXML` metodo carica i dati delle proprietà espressi in Extensible Markup Language (XML).

## <a name="syntax"></a>Sintassi


```C++
HRESULT LoadXML(
  [in] IUnknown *pxml
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pxml* \[ Pollici\]
</dt> <dd>

Puntatore **all'interfaccia IUnknown** di un elemento XML creato dal parser XML Microsoft.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.** Di seguito sono indicati alcuni valori possibili.



| Codice restituito                                                                                                  | Descrizione                     |
|--------------------------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>                      | Nessun dato di proprietà.<br/>    |
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Operazione completata.<br/>             |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>                | Memoria insufficiente.<br/> |
| <dl> <dt>**FORMATO DI FILE VFW \_ E \_ NON \_ \_ VALIDO**</dt> </dl> | Formato non valido.<br/>      |



 

## <a name="remarks"></a>Commenti

In genere, le applicazioni non dovranno usare questo metodo. DES lo usa internamente per caricare le proprietà dai file XTL.

Per usare questo metodo, creare un **oggetto IXMLDocument** e usarlo per analizzare un file XML. Usare quindi **l'oggetto IXMLDocument** per recuperare **oggetti IXMLElement.** Se l'oggetto dispone di proprietà, è possibile passare il **puntatore IXMLElement** al **metodo LoadXML.** Il metodo carica le proprietà nel setter di proprietà.

> [!Note]  
> Le **interfacce IXMLDocument** e **IXMLElement** vengono implementate in Microsoft XML Core Services (MSXML) versione 1.0, ma non nelle versioni più recenti di MSXML.

 

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare l'aggiornamento di Microsoft Windows SDK per Windows [Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPropertySetter**](ipropertysetter.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




