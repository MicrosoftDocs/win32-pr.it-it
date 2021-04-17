---
title: Metodo IMsRdpClientNonScriptable SendKeys
description: Invia una serie di sequenze di tasti al controllo. Le sequenze di tasti sono nel formato del codice di analisi, ovvero i dati della tastiera delle chiavi fisiche effettive.
ms.assetid: 1f07a9cc-4795-43cb-ac99-4bb70b8b544a
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SendKeys
- Servizi Desktop remoto del metodo SendKeys, interfaccia IMsRdpClientNonScriptable
- Interfaccia IMsRdpClientNonScriptable Servizi Desktop remoto, metodo SendKeys
- Servizi Desktop remoto del metodo SendKeys, interfaccia IMsRdpClientNonScriptable2
- Interfaccia IMsRdpClientNonScriptable2 Servizi Desktop remoto, metodo SendKeys
- Servizi Desktop remoto del metodo SendKeys, interfaccia IMsRdpClientNonScriptable3
- Interfaccia IMsRdpClientNonScriptable3 Servizi Desktop remoto, metodo SendKeys
- Servizi Desktop remoto del metodo SendKeys, interfaccia IMsRdpClientNonScriptable4
- Interfaccia IMsRdpClientNonScriptable4 Servizi Desktop remoto, metodo SendKeys
- Servizi Desktop remoto del metodo SendKeys, interfaccia IMsRdpClientNonScriptable5
- Interfaccia IMsRdpClientNonScriptable5 Servizi Desktop remoto, metodo SendKeys
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable.SendKeys
- IMsRdpClientNonScriptable2.SendKeys
- IMsRdpClientNonScriptable3.SendKeys
- IMsRdpClientNonScriptable4.SendKeys
- IMsRdpClientNonScriptable5.SendKeys
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9effa3bbd40eb64df55914b9adbc07a03ea0c465
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477765"
---
# <a name="imsrdpclientnonscriptablesendkeys-method"></a>Metodo IMsRdpClientNonScriptable:: SendKeys

Invia una serie di sequenze di tasti al controllo. Le sequenze di tasti sono nel formato del codice di analisi, ovvero i dati della tastiera delle chiavi fisiche effettive.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SendKeys(
  [in] LONG         numKeys,
  [in] VARIANT_BOOL *pbArrayKeyUp,
  [in] LONG         *plKeyData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*numkeys* \[ in\]
</dt> <dd>

Numero di sequenze di tasti da inviare. Il numero massimo di chiavi che possono essere inviate in un'operazione è 20. Il metodo restituisce **E \_ INVALIDARG** se questo parametro è maggiore di 20. Per ulteriori informazioni, vedere la sezione Osservazioni successiva.

</dd> <dt>

*pbArrayKeyUp* \[ in\]
</dt> <dd>

Matrice la cui dimensione è uguale a *numkeys*. Un elemento è **true** se la chiave corrispondente è impostata su on e **false** se la chiave corrispondente è inattiva.

</dd> <dt>

*plKeyData* \[ in\]
</dt> <dd>

Matrice la cui dimensione è uguale a *numkeys*. La matrice contiene dati della sequenza di tasti e corrisponde al valore del parametro *lParam* del messaggio di [WM \_ KeyDown](../inputdev/wm-keydown.md) . I dati specificano il numero di ripetizioni, il codice di analisi, il flag di chiave estesa, il codice del contesto, il flag di stato di chiave precedente e il flag di stato di transizione. Per una descrizione dei bit in questa matrice, vedere [WM \_ KeyDown](../inputdev/wm-keydown.md).

L'elemento corrispondente in *pbArrayKeyUp* indica se la chiave è verso l'alto o verso il basso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione ha esito positivo, restituire **S \_ OK** .

## <a name="remarks"></a>Commenti

Il metodo **SendKeys** non combina le sequenze di tasti eseguite dall'utente locale con le sequenze di tasti inviate dal metodo. Tutte le sequenze di tasti passate al metodo vengono inviate alla sessione remota in un'unica sequenza atomica.

Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                     |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                               |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>       |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable è definito come 2f079c4c-87B2-4afd-97AB-20cdb43038ae<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[KeyDown di WM \_](../inputdev/wm-keydown.md)
</dt> </dl>

 

