---
description: Crea un nuovo elemento figlio. Aggiunge oggetti IWiaItem2 all'albero IWiaItem2 di un dispositivo.
ms.assetid: 525ee788-3ff4-4def-ae71-4a405c04c6a3
title: 'Metodo IWiaItem2:: CreateChildItem (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.CreateChildItem
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 0002a6110894491a8d6efabb5a142b7c81adc820
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312394"
---
# <a name="iwiaitem2createchilditem-method"></a>Metodo IWiaItem2:: CreateChildItem

Crea un nuovo elemento figlio. Aggiunge oggetti [**IWiaItem2**](-wia-iwiaitem2.md) all'albero **IWiaItem2** di un dispositivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateChildItem(
  [in]  LONG      lItemFlags,
  [in]  LONG      lCreationFlags,
  [in]  BSTR      bstrItemName,
  [out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lItemFlags* \[ in\]
</dt> <dd>

Tipo: **Long**

Specifica il tipo di elemento WIA 2,0. Vedere i [**flag del tipo di elemento WIA**](-wia-wia-item-type-flags.md).

</dd> <dt>

*lCreationFlags* \[ in\]
</dt> <dd>

Tipo: **Long**

Specifica come creare il nuovo elemento.

<dt>

<span id="0"></span>

<span id="0"></span>**0** (0)


</dt> <dd>

Impostare i valori predefiniti per le proprietà dell'elemento figlio.

</dd> <dt>

<span id="COPY_PARENT_PROPERTY_VALUES"></span><span id="copy_parent_property_values"></span>

<span id="COPY_PARENT_PROPERTY_VALUES"></span><span id="copy_parent_property_values"></span>**Copia \_ di \_ \_ Valori delle proprietà padre** (0x40000000)


</dt> <dd>

Copiare i valori di tutte le proprietà di lettura/scrittura dall'elemento padre.

</dd> </dl> </dd> <dt>

*bstrItemName* \[ in\]
</dt> <dd>

Tipo: **BSTR**

Specifica il nome dell'elemento. Questo nome viene aggiunto alla fine del nome dell'elemento padre per generare il nome completo dell'elemento.

</dd> <dt>

*ppIWiaItem2* \[ out\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Riceve l'indirizzo di un puntatore all'interfaccia [**IWiaItem2**](-wia-iwiaitem2.md) che imposta il metodo **IWiaItem2:: CreateChildItem** .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Commenti

Alcuni dispositivi hardware WIA 2,0 consentono alle applicazioni di creare nuovi elementi nell'albero [**IWiaItem2**](-wia-iwiaitem2.md) che rappresenta il dispositivo. Le applicazioni devono testare i dispositivi per verificare se supportano questa funzionalità. Usare l' \_ interfaccia IEnumWIA dev \_ Caps per enumerare le funzionalità del dispositivo corrente.

Se il dispositivo consente la creazione di nuovi elementi nell'albero [**IWiaItem2**](-wia-iwiaitem2.md) , la chiamata a **IWiaItem2:: CreateChildItem** crea un nuovo oggetto **IWiaItem2** che è figlio del nodo corrente. Passa un puntatore al nuovo nodo all'applicazione tramite il parametro *ppIWiaItem2* . Le applicazioni devono chiamare il metodo [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sui puntatori di interfaccia ricevuti tramite il parametro *ppIWiaItem2* .

Se *lCreationFlags* è \_ la copia \_ dei valori della proprietà padre \_ e *lItemFlags* è zero, la funzione restituisce e \_ INVALIDARG.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                     |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                               |
| Intestazione<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
