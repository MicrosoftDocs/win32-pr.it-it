---
description: Il metodo LoadXML carica i dati delle proprietà espressi in Extensible Markup Language (XML).
ms.assetid: cc67e7e0-a6e0-43d1-b35d-5d64caf24e6e
title: 'Metodo IPropertySetter:: LoadXML (qedit. h)'
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
ms.openlocfilehash: 65127d313309ca7d670a99c912531db0657a9b51
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325476"
---
# <a name="ipropertysetterloadxml-method"></a>Metodo IPropertySetter:: LoadXML

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `LoadXML` metodo carica i dati delle proprietà espressi in Extensible Markup Language (XML).

## <a name="syntax"></a>Sintassi


```C++
HRESULT LoadXML(
  [in] IUnknown *pxml
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pXML* \[ in\]
</dt> <dd>

Puntatore all'interfaccia **IUnknown** di un elemento XML creato da Microsoft XML parser.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** . Di seguito sono indicati alcuni valori possibili.



| Codice restituito                                                                                                  | Descrizione                     |
|--------------------------------------------------------------------------------------------------------------|---------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>                      | Nessun dato della proprietà.<br/>    |
| <dl> <dt>**\_OK**</dt> </dl>                         | Esito positivo.<br/>             |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl>                | Memoria insufficiente.<br/> |
| <dl> <dt>**\_formato file VFW E \_ non valido \_ \_**</dt> </dl> | Formato non valido.<br/>      |



 

## <a name="remarks"></a>Commenti

In genere, le applicazioni non dovranno utilizzare questo metodo. DES lo usa internamente per caricare le proprietà dai file XTL.

Per usare questo metodo, creare un oggetto **IXMLDocument** e usarlo per analizzare un file XML. Usare quindi l'oggetto **IXMLDocument** per recuperare gli oggetti **IXMLElement** . Se l'oggetto dispone di proprietà, è possibile passare il puntatore **IXMLElement** al metodo **LoadXml** . Il metodo carica le proprietà nel setter della proprietà.

> [!Note]  
> Le interfacce **IXMLDocument** e **IXMLElement** sono implementate in Microsoft XML Core Services (MSXML) versione 1,0, ma non sono implementate nelle versioni più recenti di MSXML.

 

> [!Note]  
> Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPropertySetter**](ipropertysetter.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




